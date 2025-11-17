# Edgera Website

Minimalist website for Edgera SME buyout strategy - "Own. Operate. Compound."

## Quick Start

1. Open `index.html` in your browser to preview locally
2. Or run a local server: `python -m http.server 8000`

## Deployment to Cloudflare Pages (Recommended - Zero Cost)

### Prerequisites
- GitHub account
- Cloudflare account (free)

### Step 1: Push to GitHub
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

### Step 2: Deploy to Cloudflare Pages
1. Log in to your Cloudflare dashboard
2. Go to **Workers & Pages** → **Create application** → **Pages**
3. Click **Connect to Git**
4. Select your GitHub repository
5. Configure build settings:
   - **Framework preset**: None
   - **Build command**: (leave empty - static site)
   - **Build output directory**: `/`
6. Click **Save and Deploy**

### Step 3: Configure Custom Domain (Optional)
1. In Cloudflare Pages, go to **Custom domains**
2. Click **Set up a custom domain**
3. Enter your domain name
4. Cloudflare will automatically configure DNS if domain is on Cloudflare
5. If domain is elsewhere, update DNS records as shown

### Automatic Deployments
Every push to the `main` branch will automatically trigger a new deployment.

## Alternative Deployment Options (Also Zero Cost)

### GitHub Pages
1. Go to repository Settings → Pages
2. Select "Deploy from a branch" → main branch
3. Configure DNS: Create CNAME record pointing to `yourusername.github.io`

### Netlify
1. Go to netlify.com
2. Drag and drop the website folder or connect to Git
3. Configure custom domain in site settings

## Contact Form Setup (Web3Forms - Zero Cost)

The contact form uses Web3Forms for unlimited free submissions:

1. Go to [web3forms.com](https://web3forms.com)
2. Click **Create Access Key**
3. Enter your email: `jett@edgerapartners.com`
4. Copy the access key
5. Replace `YOUR_ACCESS_KEY` in `contact.html` (line 60) with your actual key
6. Test the form - you'll receive submissions at `jett@edgerapartners.com`

**No signup required!** Just create an access key and start receiving emails.

## File Structure
```
/
├── index.html      # Landing page with hero and investment criteria
├── about.html      # Investment philosophy and founder bio
├── contact.html    # Contact form and business process
├── style.css       # Global styles and responsive design
└── README.md       # This file
```

## Customization

### Required Updates
1. **Web3Forms Access Key**: Get your key from web3forms.com and replace `YOUR_ACCESS_KEY` in `contact.html:60`
2. **Founder Details**: Update Jett's bio, education, and LinkedIn URL in `about.html:58-82`
3. **Founder Photo**: Replace the placeholder (initials "JH") with actual headshot image

### Optional Updates
- Update investment criteria ranges in `index.html`
- Customize the redirect URL after form submission in `contact.html:63`
- Add custom domain to Cloudflare Pages
- Update copyright year in footer across all pages

## Total Cost: $0/year
- Cloudflare Pages: Free hosting
- Web3Forms: Unlimited free email submissions
- (Excluding domain registration if you choose to use one)