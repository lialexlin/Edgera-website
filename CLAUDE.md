# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a minimalist static website for Edgera, an SME buyout firm with the mission "Own. Operate. Compound." The site is built with plain HTML/CSS/JavaScript for zero-cost hosting on Cloudflare Pages.

## Architecture

**Static Site Structure**: All pages share a common navigation and footer structure with individual page-specific content sections. Each HTML file includes inline styles for page-specific components while `style.css` contains global styles.

**Design System**:
- Typography: Mona Sans font loaded from Google Fonts with system font fallbacks
- Layout: CSS Grid and Flexbox for responsive design
- Color scheme: Monochrome (black text on white background)
- Mobile-first responsive approach

**Navigation**: Fixed header navigation with logo and 3-page structure (Home, About, Contact)

## Common Development Commands

**Local Development**:
```bash
python -m http.server 8000
```
Then visit http://localhost:8000

**File Structure**:
- `index.html` - Landing page with hero section, company overview, and investment criteria
- `about.html` - Investment philosophy, founder bio (Jett Huang), and selection criteria
- `contact.html` - Contact form (Web3Forms) and business process
- `style.css` - Global styles with responsive breakpoints

## Key Implementation Details

**Contact Form**: Uses Web3Forms integration (`https://api.web3forms.com/submit`) with:
- Access key required from web3forms.com (free, unlimited)
- Submissions sent to: `jett@edgerapartners.com`
- Honeypot spam protection included
- Replace `YOUR_ACCESS_KEY` in `contact.html:60` with actual key

**Founder Section**: Located in `about.html` after Investment Thesis section:
- Placeholder profile image (circular, shows "JH" initials)
- Bio with placeholder education details
- Contact links (email, LinkedIn)
- Replace placeholders with actual information

**Responsive Design**: Three breakpoints defined in CSS:
- Desktop: >768px
- Tablet: 480-768px
- Mobile: <480px

## Deployment

**Primary: Cloudflare Pages** (Recommended)
1. Push to GitHub repository
2. Connect Cloudflare Pages to GitHub repo
3. Framework preset: None (static site)
4. Build command: (empty)
5. Build output directory: `/`
6. Automatic deployments on git push

**Alternatives**:
- **GitHub Pages**: Enable in repo settings, configure DNS
- **Netlify**: Drag-and-drop or Git integration

## Required Configuration

1. **Web3Forms Access Key**: Create at web3forms.com and update `contact.html:60`
2. **Founder Details**: Update bio, education, LinkedIn in `about.html:58-82`
3. **Founder Photo**: Replace initials placeholder with actual headshot image