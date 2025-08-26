# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimalist static website for Edgera, an SME buyout firm with the mission "Own. Operate. Compound." The site is built with plain HTML/CSS/JavaScript for zero-cost hosting on GitHub Pages or Netlify.

## Architecture

**Static Site Structure**: All pages share a common navigation and footer structure with individual page-specific content sections. Each HTML file includes inline styles for page-specific components while `style.css` contains global styles.

**Design System**: 
- Typography: Mona Sans font loaded from Google Fonts with system font fallbacks
- Layout: CSS Grid and Flexbox for responsive design
- Color scheme: Monochrome (black text on white background)
- Mobile-first responsive approach

**Navigation**: Fixed header navigation with logo and 4-page structure (Home, About, Portfolio, Contact)

## Common Development Commands

**Local Development**:
```bash
python -m http.server 8000
```
Then visit http://localhost:8000

**File Structure**:
- `index.html` - Landing page with hero section and company overview
- `about.html` - Investment philosophy and criteria  
- `portfolio.html` - Portfolio showcase (uses placeholder companies)
- `contact.html` - Contact form and business process
- `style.css` - Global styles with responsive breakpoints

## Key Implementation Details

**Contact Form**: Uses Formspree integration (`https://formspree.io/f/your-form-id`) - requires updating the form action URL with actual Formspree endpoint ID.

**Responsive Design**: Three breakpoints defined in CSS:
- Desktop: >768px 
- Tablet: 480-768px
- Mobile: <480px

**Content Management**: Portfolio companies in `portfolio.html` are currently placeholders that need to be replaced with actual company information.

## Deployment

The site is designed for zero-cost static hosting:
- **GitHub Pages**: Push to repo, enable Pages, configure DNS
- **Netlify**: Drag-and-drop deployment with automatic SSL

Domain DNS configuration required to point to chosen hosting provider.