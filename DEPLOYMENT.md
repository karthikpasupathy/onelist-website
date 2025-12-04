# Onelist Website - Deployment Guide

## Quick Deployment to Vercel

### Prerequisites
- A Vercel account (sign up at https://vercel.com)
- Git installed on your machine

### Step 1: Update Links (IMPORTANT!)

Before deploying, open `index.html` and update these placeholder URLs:

1. **Cloud signup URL** (line ~75):
   - Find: `https://app.onelist.com/signup`
   - Replace with your actual app URL

2. **GitHub repository URLs** (multiple locations):
   - Find: `https://github.com/yourusername/onelist`
   - Replace with your actual GitHub repo URL

### Step 2: Initialize Git Repository

```bash
cd d:\Qoder\Onelist-website
git init
git add .
git commit -m "Initial commit: Onelist landing page"
```

### Step 3: Push to GitHub

1. Create a new repository on GitHub (https://github.com/new)
2. Name it something like `onelist-website`
3. Don't initialize with README (we already have one)
4. Run these commands:

```bash
git remote add origin https://github.com/YOUR_USERNAME/onelist-website.git
git branch -M main
git push -u origin main
```

### Step 4: Deploy to Vercel

#### Option A: Using Vercel Dashboard (Recommended)

1. Go to https://vercel.com
2. Click "New Project"
3. Import your GitHub repository
4. Vercel will auto-detect the settings
5. Click "Deploy"
6. Done! Your site will be live in ~30 seconds

#### Option B: Using Vercel CLI

```bash
# Install Vercel CLI globally
npm i -g vercel

# Login to Vercel
vercel login

# Deploy
vercel

# Follow the prompts:
# - Set up and deploy? Yes
# - Which scope? (select your account)
# - Link to existing project? No
# - What's your project's name? onelist-website
# - In which directory is your code located? ./
# - Want to override settings? No

# For production deployment
vercel --prod
```

### Step 5: Custom Domain (Optional)

1. In Vercel dashboard, go to your project
2. Click "Settings" → "Domains"
3. Add your custom domain
4. Update DNS records as instructed by Vercel

## Local Testing

Before deploying, test locally:

```bash
# Option 1: Using Python
python -m http.server 8000

# Option 2: Using Node.js
npx serve

# Option 3: Using VS Code Live Server extension
# Right-click index.html → "Open with Live Server"
```

Then visit: http://localhost:8000

## Customization Checklist

- [ ] Update all GitHub URLs in `index.html`
- [ ] Update cloud signup URL in `index.html`
- [ ] Update footer links
- [ ] Add your actual app screenshots (optional)
- [ ] Update meta description for SEO
- [ ] Add favicon (create `favicon.ico` in root)
- [ ] Add Open Graph images for social sharing

## Environment Variables (if needed)

If you need to use environment variables in the future:

1. In Vercel dashboard → Settings → Environment Variables
2. Add your variables
3. Redeploy

## Troubleshooting

**Issue**: Links not working
- **Solution**: Make sure all URLs are updated from placeholders

**Issue**: Styles not loading
- **Solution**: Check that `style.css` and `script.js` are in the same directory as `index.html`

**Issue**: Vercel deployment fails
- **Solution**: Check `vercel.json` is present and valid JSON

## Next Steps

1. Set up analytics (Google Analytics, Plausible, etc.)
2. Add a favicon
3. Create Open Graph images for better social sharing
4. Set up a contact form or support email
5. Add a blog section (optional)

## Support

For Vercel-specific issues, check:
- https://vercel.com/docs
- https://vercel.com/support
