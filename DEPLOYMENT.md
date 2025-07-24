# 🚀 GitHub Pages Deployment Guide

This guide provides step-by-step instructions for deploying your portfolio website to GitHub Pages.

## Prerequisites

- GitHub account
- Git installed on your computer
- Portfolio website files ready

## Method 1: GitHub Web Interface (Easiest)

### Step 1: Create Repository
1. Go to [GitHub.com](https://github.com) and sign in
2. Click the "+" icon in the top right corner
3. Select "New repository"
4. Name your repository:
   - For personal site: `your-username.github.io`
   - For project site: `portfolio-website` or any name you prefer
5. Make sure it's set to "Public"
6. Check "Add a README file"
7. Click "Create repository"

### Step 2: Upload Files
1. In your new repository, click "uploading an existing file"
2. Drag and drop all your portfolio files OR click "choose your files"
3. Select all files: `index.html`, `css/`, `js/`, `images/`, etc.
4. Add a commit message: "Initial portfolio upload"
5. Click "Commit changes"

### Step 3: Enable GitHub Pages
1. Go to your repository's "Settings" tab
2. Scroll down to "Pages" in the left sidebar
3. Under "Source", select "Deploy from a branch"
4. Choose "main" branch and "/ (root)" folder
5. Click "Save"
6. Your site will be available at:
   - Personal site: `https://your-username.github.io`
   - Project site: `https://your-username.github.io/repository-name`

## Method 2: Git Command Line

### Step 1: Initialize Local Repository
```bash
# Navigate to your portfolio folder
cd path/to/your/portfolio-website

# Initialize Git repository
git init

# Add all files
git add .

# Make initial commit
git commit -m "Initial portfolio website"
```

### Step 2: Create GitHub Repository
1. Go to GitHub and create a new repository (don't initialize with README)
2. Copy the repository URL

### Step 3: Connect and Push
```bash
# Add remote repository
git remote add origin https://github.com/your-username/repository-name.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 4: Enable GitHub Pages
Follow Step 3 from Method 1 above.

## Method 3: GitHub Desktop (GUI)

### Step 1: Install GitHub Desktop
1. Download from [desktop.github.com](https://desktop.github.com)
2. Install and sign in with your GitHub account

### Step 2: Create Repository
1. Click "Create a New Repository on your hard drive"
2. Choose your portfolio folder
3. Name your repository
4. Click "Create Repository"

### Step 3: Publish to GitHub
1. Click "Publish repository"
2. Uncheck "Keep this code private"
3. Click "Publish Repository"

### Step 4: Enable GitHub Pages
Follow Step 3 from Method 1 above.

## Custom Domain Setup (Optional)

### Step 1: Purchase Domain
Buy a domain from providers like:
- Namecheap
- GoDaddy
- Google Domains
- Cloudflare

### Step 2: Configure DNS
Add these DNS records at your domain provider:

**For apex domain (example.com):**
```
Type: A
Name: @
Value: 185.199.108.153
Value: 185.199.109.153
Value: 185.199.110.153
Value: 185.199.111.153
```

**For www subdomain:**
```
Type: CNAME
Name: www
Value: your-username.github.io
```

### Step 3: Configure GitHub Pages
1. In repository settings → Pages
2. Under "Custom domain", enter your domain
3. Check "Enforce HTTPS"
4. Create a `CNAME` file in your repository root with your domain name

## Updating Your Site

### Web Interface
1. Go to your repository on GitHub
2. Navigate to the file you want to edit
3. Click the pencil icon to edit
4. Make changes and commit

### Git Command Line
```bash
# Make changes to your files
# Add changes
git add .

# Commit changes
git commit -m "Update portfolio content"

# Push to GitHub
git push origin main
```

### GitHub Desktop
1. Make changes to your files
2. Review changes in GitHub Desktop
3. Add commit message
4. Click "Commit to main"
5. Click "Push origin"

## Troubleshooting

### Site Not Loading
- Wait 5-10 minutes after enabling GitHub Pages
- Check that `index.html` is in the root directory
- Verify repository is public
- Check GitHub Pages settings

### Images Not Displaying
- Ensure image paths use relative URLs: `./images/photo.jpg`
- Check image file names match exactly (case-sensitive)
- Verify images are in the repository

### Custom Domain Issues
- DNS changes can take 24-48 hours to propagate
- Use DNS checker tools to verify records
- Ensure CNAME file contains only your domain name

### HTTPS Certificate Issues
- Wait 24 hours after setting up custom domain
- Try disabling and re-enabling "Enforce HTTPS"
- Contact GitHub Support if issues persist

## Performance Tips

### Optimize Images
- Compress images before uploading
- Use appropriate formats (JPEG for photos, PNG for graphics)
- Consider WebP format for better compression

### Minimize Files
- Minify CSS and JavaScript for production
- Remove unnecessary comments and whitespace
- Use CDN for external libraries when possible

### Monitor Performance
- Use Google PageSpeed Insights
- Check Core Web Vitals
- Monitor loading times regularly

## Security Best Practices

### Repository Security
- Never commit sensitive information (API keys, passwords)
- Use environment variables for sensitive data
- Review commits before pushing

### Contact Form Security
- Use Formspree or similar services for form handling
- Implement CAPTCHA for spam protection
- Validate all form inputs

## Analytics Setup

### Google Analytics
1. Create Google Analytics account
2. Get tracking ID
3. Add tracking code to `index.html`:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_TRACKING_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_TRACKING_ID');
</script>
```

### GitHub Pages Analytics
- View traffic in repository Insights → Traffic
- Monitor popular pages and referrers
- Track visitor statistics

## Maintenance

### Regular Updates
- Update content regularly
- Check for broken links
- Update project information
- Refresh skills and experience

### Backup Strategy
- Keep local copies of all files
- Consider multiple Git remotes
- Export analytics data periodically

### Version Control
- Use meaningful commit messages
- Create branches for major changes
- Tag releases for important updates

## Support Resources

- **GitHub Pages Documentation**: [docs.github.com/pages](https://docs.github.com/pages)
- **GitHub Community**: [github.community](https://github.community)
- **Git Documentation**: [git-scm.com/doc](https://git-scm.com/doc)

---

**Need Help?** Create an issue in your repository or contact support through GitHub.

*Last updated: July 2024*

