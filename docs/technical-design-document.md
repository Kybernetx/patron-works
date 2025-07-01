# Patron Works Blog: Core Development Documentation

This document outlines essential development-focused documentation, crucial for building a robust, maintainable, and scalable foundation for the Patron Works blog. These documents complement the Product Requirements Document (PRD) and Architecture & Scalability Analysis by detailing the "how" of implementation, operations, quality assurance, and coding conventions.

## 1. Technical Design Document (TDD) / Low-Level Design (LLD)

This document translates the high-level requirements from the PRD into specific technical choices and implementation details, guiding the actual development process.

### 1.1 Static Site Generator (SSG) Choice & Configuration

**Chosen SSG:** [Decision: Hugo / Eleventy / Jekyll - To be filled in by you]  
**Version:** [e.g., Hugo v0.120.4, Eleventy v3.0.0, Jekyll v4.2.2]

**Key Configuration Files:**
- **Hugo:** `config.toml` (or `hugo.toml`) – details of site title, base URL, permalinks, languages, build settings, etc.
- **Eleventy:** `.eleventy.js` – defines input/output directories, template languages, passthrough copy files, custom collections, etc.
- **Jekyll:** `_config.yml` – site-wide variables, permalinks, plugins, build settings, etc.

**Rationale for SSG Choice:** [Brief explanation of why this SSG was chosen over others, considering specific Patron Works needs (e.g., speed, templating comfort, GitHub Pages integration).]

### 1.2 Content Structure & Front Matter Conventions

**Content Format:** All written content will be in Markdown (`.md`).

**File Naming Convention:**
- **Blog Posts:** `YYYY-MM-DD-slug-of-post.md` (e.g., `2025-06-20-first-ai-startup-log.md`)
- **Static Pages (About, Support):** `about.md`, `support.md`, etc. (or specific SSG conventions)

**YAML Front Matter:** All Markdown files will begin with YAML Front Matter, enclosed by `---`.

**Mandatory Fields for Blog Posts:**
```yaml
title: "Your Post Title"
date: YYYY-MM-DD HH:MM:SS +/-ZZZZ (e.g., 2025-06-20 10:00:00 -0500)
description: "A short summary for SEO and social sharing."
tags: [tag1, tag2, tag3] (lowercase, hyphenated)
layout: post (or specific template name)
```

**Optional Fields:**
```yaml
image: /assets/images/post-hero.jpg (for hero image)
featured: true (for homepage hero slot)
categories: [category1, category2]
```

**Asset Storage:** All images, diagrams, and other static assets will be stored in a dedicated `assets/` or `static/` directory within the project, organized by type or post (e.g., `assets/images/posts/post-slug/image.jpg`).

### 1.3 Templating & Layout Design

**Main Layouts:**
- **default / base:** Provides the fundamental HTML structure (`<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`), including global CSS and JavaScript links.
- **post:** Defines the layout for individual blog posts, injecting content, front matter fields (title, date, tags), and potentially comments/share buttons.
- **page:** Defines the layout for static pages (About, Support, Newsletter).

**Reusable Components (`_includes` or similar):**
- **Header:** Contains logo, site title, main navigation.
- **Footer:** Contains copyright, privacy policy link, social media links.
- **Newsletter Sign-up Form:** Embed code for the selected newsletter service.
- **Donation Button:** Embed code/link for Buy Me a Coffee / Ko-fi / Stripe Checkout.
- **Social Share Buttons:** Links to share current post on Twitter, LinkedIn, etc.

**Styling Approach:**
- [Decision: Pure CSS / Tailwind CSS (preferred for clean utility-first approach) / Custom CSS framework]
- **Typography:** Inter font will be the primary typeface for body text and headings for a clean, modern look.
- **Color Palette:** [Define primary, secondary, accent colors, and text/background colors for both light and potential dark mode.]
- **Responsiveness:** Implementation details for mobile-first design using media queries (for pure CSS) or responsive utility classes (for Tailwind CSS).

### 1.4 JavaScript & Third-Party Integrations

**Newsletter Integration:**
- **Provider:** [ConvertKit / Mailchimp / Buttondown]
- **Implementation:** Embed provided HTML/JS form code directly into relevant template includes (e.g., footer, newsletter page).

**Donation Integration:**
- **Provider:** [Buy Me a Coffee / Ko-fi / Stripe Checkout]
- **Implementation:** Embed provided HTML/JS button/widget code into homepage and post footer templates.

**Merch Store Link:** Simple `<a>` tag link to the external Redbubble/Printful store.

**Technical Content Rendering:**
- **LaTeX/Math Notation:** Integration of [MathJax / KaTeX] library.
  - **Configuration:** How the library is loaded (e.g., via CDN in `<head>`) and how it's instructed to parse specific delimiters (e.g., `$` for inline, `$$` for block equations).
  - **Implementation:** Markdown content will include LaTeX directly within these delimiters.
- **Code Highlighting:** SSG's built-in code highlighting feature (e.g., Rouge for Jekyll, Chroma for Hugo, Prism.js for Eleventy). Specify supported languages.

**SEO Tools:**
- **Open Graph Tags:** Implementation in `_includes/head.html` (or equivalent) using Liquid/Go Templates/Nunjucks to dynamically populate `og:title`, `og:description`, `og:image`, `og:url` from post front matter.
- **Meta Descriptions:** Dynamically generated from post description field.