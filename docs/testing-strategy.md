# Testing Strategy (MVP)

This section outlines the basic approach to ensure the blog's quality and functionality.

## 1. Manual Functional Testing

After each major change or deployment, perform the following checks:

### 1.1 Homepage
- Loads correctly
- Hero section displays latest/featured post
- Mission statement and About Me snapshot are visible
- Newsletter sign-up forms are present and functional
- All external links (GitHub, YouTube, socials, Support button) work and direct to correct destinations

### 1.2 Blog Post Pages
- Individual post pages load
- Markdown rendering (headings, lists, bold/italic, links, images) is correct
- Code blocks display with syntax highlighting
- LaTeX/Math notation renders correctly
- Author info, tags, and share buttons are present
- "Support Me" button is present and functional in the footer

### 1.3 Navigation
- All top-menu items (Home, Blog, About, Newsletter, Support) link to the correct pages

### 1.4 Responsiveness
- Check layout and readability on various screen sizes (desktop, tablet, mobile)

### 1.5 Newsletter Sign-up
- Test the entire sign-up flow from the website

## 2. Automated Quality Checks (Recommended for future efficiency)

### 2.1 Markdown Linting
- Integrate a Markdown linter (e.g., `markdownlint` via npm script or Git hook) to enforce consistent Markdown style

### 2.2 Link Checker
- Utilize a command-line tool (e.g., `lychee`) or an online service to regularly scan the live site for broken internal and external links

### 2.3 Basic Performance Audits
- Periodically run Google Lighthouse or PageSpeed Insights on key pages to monitor performance, accessibility, and SEO scores

