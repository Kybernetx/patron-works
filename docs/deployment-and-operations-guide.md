# 1. Deployment & Operations Guide

This guide provides step-by-step instructions for setting up the development environment, deploying the blog, and ongoing management.

## 1.1 Local Development Setup

- **Install Git**: [Link to Git installation instructions for OS]
- **Install Node.js (for Eleventy) / Ruby (for Jekyll) / Go (for Hugo)**: [Link to respective installation instructions]
- **Install SSG**:
  - Eleventy: `npm install -g @11ty/eleventy`
  - Jekyll: `gem install jekyll bundler`
  - Hugo: [Link to Hugo installation instructions]
- **Clone Repository**: `git clone [your-github-repo-url]`
- **Navigate to Project**: `cd [your-repo-name]`
- **Install Project Dependencies (if applicable)**:
  - Eleventy: `npm install` (if package.json exists)
  - Jekyll: `bundle install` (if Gemfile exists)
- **Run Local Server**:
  - Eleventy: `npx @11ty/eleventy --serve` (usually at http://localhost:8080)
  - Jekyll: `bundle exec jekyll serve` (usually at http://127.0.0.1:4000)
  - Hugo: `hugo server` (usually at http://localhost:1313)

## 1.2 Git Workflow for Content & Code Updates

- **Branching Strategy (Simple)**: All development on the main branch for MVP
- **Add/Commit Changes**:
  - `git add .` (stages all changes)
  - `git commit -m "feat: New blog post title"` (use descriptive, concise messages)
- **Push to Remote**: `git push origin main` (triggers auto-deployment)

## 1.3 Hosting & Domain Configuration

- **Repository Host**: GitHub (github.com/[your-username]/[your-repo-name])
- **Deployment Host**: [Decision: GitHub Pages / Netlify]

### GitHub Pages:
- Go to GitHub repo Settings > Pages
- Select main branch as the source and /root as the folder
- Enter your custom domain

### Netlify:
- Connect GitHub account and select your repository
- Build Command: [e.g., hugo, npx @11ty/eleventy, bundle exec jekyll build]
- Publish Directory: [e.g., public for Hugo, _site for Eleventy/Jekyll]

### Custom Domain (DNS) Setup:
- **Purchase Domain**: [Details of domain registrar used, e.g., Namecheap, Cloudflare Registrar]
- **DNS Records**:
  - For GitHub Pages:
    - Add a CNAME record with www pointing to yourusername.github.io
    - Add A records pointing to GitHub Pages IP addresses
  - For Netlify:
    - Follow Netlify's guided DNS setup (typically setting CNAME for www and an A record for the apex domain)
- **SSL/HTTPS**: Free SSL will be automatically provisioned and managed by [GitHub Pages / Netlify]

## 1.4 Routine Operations

- **Publishing a New Post**: Follow Git workflow (1.2)
- **Newsletter Sending**: Log into your chosen newsletter service (ConvertKit/Mailchimp/Buttondown) and send weekly emails
- **Monitoring Donations**: Regularly check your Buy Me a Coffee/Ko-fi/Stripe dashboard for support activity
