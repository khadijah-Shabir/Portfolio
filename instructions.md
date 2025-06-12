# Portfolio Website - Run & Deployment Instructions

This document provides comprehensive instructions for running and deploying your portfolio website tailored for the Devsinc Software Engineering Internship application.

## Table of Contents
1. [Local Setup & Viewing](#local-setup--viewing)
2. [Customizing Your Portfolio](#customizing-your-portfolio)
3. [Deployment Options](#deployment-options)
   - [GitHub Pages](#github-pages)
   - [Netlify](#netlify)
   - [Vercel](#vercel)
4. [Troubleshooting](#troubleshooting)

## Local Setup & Viewing

### Option 1: Direct Browser Opening (Simplest Method)
1. Extract the `portfolio_website.zip` file to a location on your computer
2. Navigate to the extracted folder
3. Double-click on `index.html` to open it directly in your default browser

### Option 2: Using a Local Server (Recommended for Development)
1. Extract the `portfolio_website.zip` file to a location on your computer
2. If you have Python installed:
   - Open a terminal/command prompt
   - Navigate to the extracted folder: `cd path/to/portfolio_website`
   - Run one of these commands:
     - Python 3: `python -m http.server 8000`
     - Python 2: `python -m SimpleHTTPServer 8000`
   - Open your browser and go to: `http://localhost:8000`

3. If you have Node.js installed:
   - Open a terminal/command prompt
   - Navigate to the extracted folder: `cd path/to/portfolio_website`
   - Install a simple server: `npm install -g serve`
   - Run the server: `serve`
   - Open your browser and go to the URL shown in the terminal (typically `http://localhost:5000`)

4. Using Visual Studio Code:
   - Open the folder in VS Code
   - Install the "Live Server" extension
   - Right-click on `index.html` and select "Open with Live Server"

## Customizing Your Portfolio

### Updating Personal Information
1. Open `index.html` in any text editor
2. Modify the following sections:
   - Header/navigation (lines 20-40)
   - Hero section (lines 43-78)
   - About section (lines 81-112)
   - Resume download link: Update the href attribute in line 62 to point to your resume file

### Updating Skills
1. Open `index.html` in any text editor
2. Navigate to the Skills section (around line 115)
3. Modify the skill percentages and names to match your expertise

### Updating Projects
1. Open `index.html` in any text editor
2. Navigate to the Projects section (around line 190)
3. Each project is contained in a `<div class="project-card">` element
4. Duplicate or modify these elements to showcase your projects
5. Update project links to point to your GitHub repositories or live demos

### Updating Experience & Education
1. Open `index.html` in any text editor
2. Navigate to the Experience section (around line 260) and Education section (around line 320)
3. Update the content to reflect your work history and educational background

### Changing Colors & Styling
1. Open `css/style.css` in any text editor
2. At the top of the file, you'll find CSS variables (around line 2):
   ```css
   :root {
     --primary-color: #4361ee;
     --secondary-color: #3a0ca3;
     /* other variables */
   }
   ```
3. Modify these variables to change the color scheme of your portfolio

## Deployment Options

### GitHub Pages
1. Create a GitHub account if you don't have one: [GitHub Sign Up](https://github.com/join)
2. Create a new repository named `username.github.io` (replace "username" with your GitHub username)
3. Upload your portfolio website files to this repository:
   ```
   git init
   git add .
   git commit -m "Initial portfolio website"
   git remote add origin https://github.com/username/username.github.io.git
   git push -u origin main
   ```
4. Your website will be available at `https://username.github.io`

### Netlify
1. Create a Netlify account: [Netlify Sign Up](https://app.netlify.com/signup)
2. Once logged in, click on "New site from Git" or go to the "Sites" tab and click "Import an existing project"
3. Connect your GitHub/GitLab/Bitbucket account
4. Select the repository containing your portfolio website
5. Configure build settings (not needed for static HTML/CSS/JS sites)
6. Click "Deploy site"
7. Your site will be deployed with a Netlify subdomain (e.g., `your-portfolio.netlify.app`)
8. You can set up a custom domain in the site settings if desired

### Vercel
1. Create a Vercel account: [Vercel Sign Up](https://vercel.com/signup)
2. Once logged in, click "Import Project"
3. Enter the repository URL or connect your GitHub/GitLab/Bitbucket account
4. Select the repository containing your portfolio website
5. Configure project settings (not needed for static HTML/CSS/JS sites)
6. Click "Deploy"
7. Your site will be deployed with a Vercel subdomain (e.g., `your-portfolio.vercel.app`)
8. You can set up a custom domain in the project settings if desired

### Direct Upload to Web Hosting
If you have web hosting service (like GoDaddy, Bluehost, etc.):
1. Access your hosting control panel
2. Navigate to the file manager or use FTP access
3. Upload all files from your portfolio website folder to the public_html or www directory
4. Your website will be available at your domain name

## Troubleshooting

### Images Not Loading
- Check that image paths are correct
- Ensure image files are in the correct directory (images/)
- Verify image file names match exactly (case-sensitive)

### Styling Issues
- Make sure the CSS file is properly linked in the HTML
- Clear your browser cache (Ctrl+F5 or Cmd+Shift+R)
- Check for any CSS syntax errors

### JavaScript Not Working
- Check the browser console for errors (F12 or right-click > Inspect > Console)
- Ensure the JavaScript file is properly linked in the HTML
- Verify that all referenced HTML elements exist

### Deployment Issues
- GitHub Pages: Make sure your repository is public and named correctly
- Netlify/Vercel: Check build logs for any errors
- Web Hosting: Ensure all files were uploaded to the correct directory

If you encounter any issues not covered here, please feel free to reach out for assistance.
