# Product Requirements Document: Patron Works (MVP)

## 1. Purpose
This MVP PRD defines the minimal features required to launch **Patron Works** — a centralized, content-focused blog hub for publishing weekly articles, growing an email list, and collecting reader support. It emphasizes technical clarity, authenticity, and scalability without feature bloat, serving as a working log of invention, reflection, and learning in real-time. The goal is to ship ideas, inspire builders, and leave a legacy of useful, documented thought.

## 2. Core Goals (6–12 Months)
- **Content Consistency**: Publish 1 high-quality blog post per week.
- **Audience Engagement**: Grow an email list to 100+ newsletter subscribers by Month 6.
- **Reader Support**: Receive direct financial support from at least 10 readers within the first 3 months.
- **Brand Centralization**: Serve as a central personal brand hub linking to other platforms.

## 3. Target Audience
- Technologists, STEM learners, builders, and intellectually curious readers.
- Audiences seeking technical depth, transparency, and personal growth narratives.
- Aspiring founders and early-career professionals looking for real-time documentation of an entrepreneurial journey.

## 4. Minimal Feature Set

### 4.1 Blog
- **Markdown-based posts**: Support for one new post per week.
- **Clean, readable design**: Minimalist aesthetics, legible fonts, optimal line spacing.
- **Code formatting and image support**: Syntax highlighting and alt-text enabled images.
- **Metadata support**: YAML front matter with title, description, and tags.
- **Simple SEO optimization**: Open Graph tags and basic meta descriptions.

### 4.2 Homepage
- **Hero Section**: Highlight the featured or latest blog post.
- **Mission/Value Statement**: Brief, compelling explanation of Patron Works' purpose.
- **About Me snapshot**: Short introduction with photo and link to full bio.
- **Email newsletter sign-up**: Forms at both top and bottom of page.
- **External links**: GitHub, YouTube, and social platforms.
- **Call to Action**: Prominent "Support My Work" button or link.

### 4.3 Newsletter
- **Email sign-up form**: Integrated with ConvertKit, Mailchimp, or Buttondown.
- **Content delivery**: Static template or tool-based email distribution.
- **Archive (optional)**: Optional past issues archive.

### 4.4 Support / Monetization
- **Donation integration**: Buy Me a Coffee, Ko-fi, or Stripe Checkout.
- **Button placement**: Visible on homepage and footer of blog posts.
- **Merch store link**: Optional external print-on-demand store (e.g., Redbubble).

### 4.5 Navigation (Top Menu)
- Home
- Blog
- About
- Newsletter
- Support

## 5. Technical Stack
- **Static Site Generator**: Hugo, Eleventy, or Jekyll.
- **Hosting**: GitHub Pages (Jekyll) or Netlify (Hugo/Eleventy).
- **Content Management**: Markdown (`.md`) with YAML front matter.
- **Newsletter Service**: Mailchimp, ConvertKit, or Buttondown.
- **Support Integration**: Embedded donation platform scripts.
- **Domain & SSL**: Custom domain + HTTPS via Cloudflare or Netlify SSL.

## 6. Workflow
- **Content Creation**: Write posts locally in Markdown.
- **Version Control**: Use Git for content/code tracking.
- **Deployment**: Git push triggers deployment via GitHub/Netlify.
- **Newsletter Management**: Send via selected provider.
- **Monetization Monitoring**: Check donation platform activity regularly.

## 7. Success Metrics
- **Content Production**: ✍️ 1 blog post/week (tracked via Git or log).
- **Newsletter Engagement**: 📧 30%+ open rate.
- **Financial Support**: 💵 10 supporters in first 3 months.
- **Subscriber Growth**: 🚀 100+ subscribers by Month 6.
- **Traffic Growth**: 📈 Google Analytics (Phase 2).

## 8. Deferred Features (Phase 2)
- Project build logs and technical portfolios.
- Commenting system (Disqus or Firestore).
- Advanced on-site search.
- Dark mode toggle.
- Deeper analytics and feedback tools.
- On-site merchandise checkout.
- Community layer (e.g., Discord, forums).
