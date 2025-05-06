# AI Tools Directory 🤖

> The ultimate directory of AI tools and resources for professionals and enthusiasts.

[![Netlify Status](https://api.netlify.com/api/v1/badges/your-badge-id/deploy-status)](https://app.netlify.com/sites/your-site/deploys)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
- [Directory Structure](#directory-structure)
- [Customization](#customization)
- [Deployment](#deployment)
- [Custom Domain Setup](#custom-domain-setup)
- [Troubleshooting](#troubleshooting)
- [Support & Resources](#support--resources)

## Overview

AI Tools is a comprehensive directory website showcasing various artificial intelligence tools and resources in a clean, responsive 3-column grid layout. The directory helps users discover and compare AI tools across different categories.

## Features

- 🎯 Responsive 3-column grid layout
- 🔍 Search functionality
- 🏷️ Category filtering
- 💨 Fast loading times
- 📱 Mobile-friendly design
- 🎨 Customizable styling
- 📊 SEO optimized

## Getting Started

### Prerequisites
- Node.js (v14 or higher)
- Git
- Basic knowledge of HTML/CSS

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/ai-tools-directory.git

# Navigate to project directory
cd ai-tools-directory

# Install dependencies
npm install

# Start development server
npm run dev
```

## Directory Structure

```
ai-tools-directory/
├── src/
│   ├── components/
│   │   ├── Card.js
│   │   ├── Grid.js
│   │   └── Hero.js
│   ├── data/
│   │   └── tools.json
│   ├── styles/
│   │   └── main.css
│   └── pages/
├── public/
│   └── images/
├── package.json
└── README.md
```

## Customization

### Adding Directory Items

Add new tools by editing `src/data/tools.json`:

```json
{
  "id": "tool-name",
  "title": "Tool Name",
  "description": "Tool description",
  "category": "category-name",
  "url": "https://toolurl.com",
  "image": "/images/tool-image.png"
}
```

### Modifying Categories

Edit categories in `src/data/categories.js`:

```javascript
export const categories = [
  {
    id: "category-1",
    name: "Category Name",
    description: "Category description"
  }
];
```

### Updating Hero Section

Modify the hero section in `src/components/Hero.js`:

```javascript
<div className="hero">
  <h1>Your New Title</h1>
  <p>Your new description</p>
</div>
```

### Customizing Colors

Edit the CSS variables in `src/styles/main.css`:

```css
:root {
  --primary-color: #007bff;
  --secondary-color: #6c757d;
  --background-color: #ffffff;
}
```

## Deployment

### Netlify Deployment

1. Create a Netlify account
2. Connect your GitHub repository
3. Configure build settings:
   - Build command: `npm run build`
   - Publish directory: `dist`
4. Click "Deploy"

### Vercel Deployment

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

## Custom Domain Setup

1. Purchase domain from preferred registrar
2. Add domain in deployment platform:
   ```
   Domain: yourdomain.com
   ```
3. Update DNS records:
   ```
   Type: A
   Name: @
   Value: [deployment platform IP]
   ```
4. Wait for DNS propagation (24-48 hours)

## Troubleshooting

### Common Issues

**Build Failures**
```bash
# Clear cache and node modules
rm -rf node_modules
rm -rf .cache
npm install
```

**Image Loading Issues**
- Ensure images are in the correct format (JPG, PNG, WebP)
- Check file paths in `tools.json`
- Verify image optimization settings

### Performance Optimization

1. Compress images using:
   ```bash
   npm run optimize-images
   ```
2. Enable caching in `netlify.toml`:
   ```toml
   [[headers]]
     for = "/*"
     [headers.values]
       Cache-Control = "public, max-age=31536000"
   ```

## Support & Resources

- 📚 [Documentation](https://docs.yoursite.com)
- 💬 [Discord Community](https://discord.gg/yourserver)
- 🐛 [Issue Tracker](https://github.com/yourusername/ai-tools-directory/issues)
- 📧 [Support Email](mailto:support@yoursite.com)

### Contributing

1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Open pull request

---

## License

MIT © [Your Name]

---

Made with ❤️ by [Your Name](https://yoursite.com)