# Edgera Website

Minimalist website for Edgera SME buyout strategy - "Own. Operate. Compound."

## Quick Start

1. Open `index.html` in your browser to preview locally
2. Or run a local server: `python -m http.server 8000`

## Deployment Options (Zero Cost)

### Option 1: GitHub Pages (Recommended)
1. Create a GitHub repository
2. Push all files to the repository
3. Go to repository Settings → Pages
4. Select "Deploy from a branch" → main branch
5. Point your domain DNS to GitHub Pages:
   - Create CNAME record: `your-domain.com` → `yourusername.github.io`
   - Or A records to GitHub's IPs: 185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153

### Option 2: Netlify
1. Go to netlify.com
2. Drag and drop the website folder
3. Configure custom domain in site settings
4. Update DNS records as provided by Netlify

## Contact Form Setup

The contact form uses Formspree. To activate:
1. Go to formspree.io
2. Create a free account
3. Get your form endpoint
4. Replace `your-form-id` in `contact.html` with your actual form ID

## File Structure
```
/
├── index.html      # Landing page
├── about.html      # Company story & philosophy  
├── portfolio.html  # Portfolio companies (placeholder)
├── contact.html    # Contact form & information
├── style.css       # Global styles
└── README.md       # This file
```

## Customization

- Update company details in all HTML files
- Replace placeholder portfolio companies in `portfolio.html`
- Customize colors by changing the CSS variables
- Add your actual email in `contact.html`
- Update form action URL with your Formspree endpoint

## Total Cost: $0/year
(Excluding domain registration you already own)