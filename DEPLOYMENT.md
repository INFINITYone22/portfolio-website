# 🚀 Deployment Guide - GitHub Pages

## 📋 Pre-Deployment Checklist

### ✅ Repository Setup
- [x] Repository name: `portfolio-website`
- [x] Repository URL: `https://github.com/INFINITYone22/portfolio-website`
- [x] All files are in the root directory
- [x] README.md is comprehensive
- [x] .gitignore is configured

### ✅ File Structure
```
portfolio-website/
├── index.html              ✅ Main homepage
├── projects.html           ✅ Projects page
├── styles.css              ✅ Stylesheet
├── script.js               ✅ JavaScript
├── assets/
│   └── resume/
│       ├── README.md       ✅ Instructions
│       └── rohith_garapati_resume.tex ✅ LaTeX source
├── README.md               ✅ Documentation
├── _config.yml             ✅ Jekyll config
├── .gitignore              ✅ Git ignore
└── DEPLOYMENT.md           ✅ This file
```

## 🛠️ GitHub Pages Setup Steps

### 1. Repository Configuration
1. **Create Repository** (if not done):
   ```bash
   git init
   git add .
   git commit -m "Initial commit: Portfolio website"
   git branch -M main
   git remote add origin https://github.com/INFINITYone22/portfolio-website.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**:
   - Go to repository Settings
   - Scroll to "Pages" section
   - Source: "Deploy from a branch"
   - Branch: "main"
   - Folder: "/ (root)"
   - Click "Save"

### 2. DNS and Domain (Optional)
If using a custom domain:
1. Create `CNAME` file in root with your domain
2. Configure DNS records with your domain provider
3. Wait for DNS propagation (24-48 hours)

### 3. Post-Deployment Steps

#### ✅ Immediate Verification
- [ ] Site loads at: `https://infinityone22.github.io/portfolio-website`
- [ ] Navigation works between pages
- [ ] All links are functional
- [ ] Responsive design works on mobile
- [ ] Glitch effect animates properly
- [ ] Resume link works (after adding PDF)

#### ✅ SEO and Performance
- [ ] Google Search Console setup
- [ ] Meta tags are correctly configured
- [ ] Site speed is optimized
- [ ] Mobile-friendly test passes

## 📝 Adding Your Resume

### Step 1: Generate PDF from LaTeX
```bash
# Navigate to assets/resume/
cd assets/resume/

# Compile LaTeX to PDF (requires LaTeX installation)
pdflatex rohith_garapati_resume.tex

# Or use online LaTeX editors like Overleaf
```

### Step 2: Upload Resume
1. Place `rohith_garapati_resume.pdf` in `assets/resume/`
2. Commit and push:
   ```bash
   git add assets/resume/rohith_garapati_resume.pdf
   git commit -m "Add resume PDF"
   git push
   ```

## 🔄 Update Workflow

### For Content Updates:
```bash
# 1. Make changes to files
# 2. Test locally
python -m http.server 8000  # Visit localhost:8000

# 3. Commit and push
git add .
git commit -m "Update: description of changes"
git push
```

### For Major Updates:
1. Create a new branch for testing
2. Make changes and test thoroughly
3. Create pull request
4. Merge to main after review

## 🐛 Troubleshooting

### Common Issues:

**Site not updating?**
- Check GitHub Actions tab for build status
- Clear browser cache (Ctrl+F5)
- Wait 5-10 minutes for GitHub Pages to rebuild

**404 errors?**
- Verify file paths are correct
- Ensure file names match exactly (case-sensitive)
- Check that all links use relative paths

**CSS/JS not loading?**
- Verify file paths in HTML
- Check browser console for errors
- Ensure MIME types are correct

**Resume link broken?**
- Verify PDF file exists in `assets/resume/`
- Check file name matches the link in HTML
- Ensure file size is under GitHub's limits

## 📊 Analytics and Monitoring

### Google Analytics (Optional)
Add tracking code to `<head>` section:
```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Performance Monitoring
- Use Google PageSpeed Insights
- Monitor Core Web Vitals
- Check mobile responsiveness regularly

## 🎯 Production Checklist

### Before Going Live:
- [ ] All personal information is updated
- [ ] Contact details are correct
- [ ] Social media links work
- [ ] All projects have proper descriptions
- [ ] Resume is current and accessible
- [ ] Website is mobile-responsive
- [ ] All animations work smoothly
- [ ] Cross-browser testing completed
- [ ] SEO meta tags are optimized

### Security Considerations:
- [ ] No sensitive information in code
- [ ] HTTPS is enabled (GitHub Pages default)
- [ ] No hardcoded credentials
- [ ] External links open in new tabs

## 🚀 Live Site Information

**Primary URL**: `https://infinityone22.github.io/portfolio-website`  
**Repository**: `https://github.com/INFINITYone22/portfolio-website`  
**Build Status**: Check GitHub Actions tab  
**Last Deployed**: Auto-deploys on push to main  

---

**Need help?** Check GitHub Pages documentation or create an issue in the repository.