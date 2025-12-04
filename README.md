# Onelist Website

A minimal, classy landing page for Onelist - a productivity app that keeps all your todos, notes, and ideas in one text file.

## Features

- 🎨 Minimal and classy design matching the Onelist app aesthetic
- 📱 Fully responsive (mobile and desktop)
- ⚡ Fast and lightweight
- 🎯 Clear CTAs for both cloud and self-hosted options
- ✨ Smooth animations and interactions

## Deployment to Vercel

### Option 1: Deploy via Vercel CLI

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Deploy:
```bash
vercel
```

3. Follow the prompts to link your project

### Option 2: Deploy via Vercel Dashboard

1. Push this repository to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Click "New Project"
4. Import your GitHub repository
5. Click "Deploy"

## Customization

### Update Links

Before deploying, update the following placeholders in `index.html`:

- Replace `https://app.onelist.com/signup` with your actual signup URL
- Replace `https://github.com/yourusername/onelist` with your actual GitHub repository URL
- Update all GitHub links in the footer

### Update Colors

The color scheme is defined in CSS variables in `style.css`. You can customize:

```css
:root {
    --color-bg: #F5F1ED;
    --color-primary: #6B5D4F;
    /* ... other colors */
}
```

## Local Development

Simply open `index.html` in your browser, or use a local server:

```bash
# Using Python
python -m http.server 8000

# Using Node.js
npx serve
```

## License

Open source - feel free to use and modify as needed.
