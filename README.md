# Patron Works Blog

A centralized, content-focused blog hub for publishing weekly articles, growing an email list, and collecting reader support. Built with technical clarity, authenticity, and scalability in mind.

## Features

- **Static Site Generation**: Built with Eleventy for speed and flexibility
- **Modern Design**: Custom CSS with carefully chosen color palette and Inter typography
- **Content Management**: Markdown-based with YAML front matter
- **Newsletter Integration**: Ready for ConvertKit, Mailchimp, or Buttondown
- **Support Integration**: Built-in Buy Me a Coffee and Ko-fi integration
- **SEO Optimized**: Open Graph tags, meta descriptions, and semantic HTML
- **Mathematical Notation**: KaTeX support for technical content
- **Syntax Highlighting**: Code blocks with proper highlighting
- **Responsive Design**: Mobile-first approach with modern CSS Grid and Flexbox
- **Performance Optimized**: Fast loading with efficient asset delivery

## Color Palette

### Primary Palette
- **Event Horizon Black** (#0B0B0B) - Deep matte black for immersive depth and foundation
- **Deep Space Blue** (#0A1A2F) - Cosmic intelligence for advanced tech themes
- **Ice White** (#DDE3E9) - Arctic clarity for clean UI and contrast
- **True Black** (#000000) - Absolute black for structural shadows

### Secondary Palette
- **Corsair Red** (#B02527) - Tactical red for alerts and highlights
- **Oxidized Gray** (#4B4F56) - Functional dark gray for panels and muted text
- **Airframe Steel** (#7C7F85) - Industrial steel for surface colors and containers

## Project Structure

```
patron-works-blog/
├── src/
│   ├── _data/
│   │   └── site.json          # Site configuration
│   ├── _includes/
│   │   ├── layouts/
│   │   │   ├── base.njk       # Base HTML template
│   │   │   ├── home.njk       # Homepage layout
│   │   │   ├── post.njk       # Blog post layout
│   │   │   └── page.njk       # Static page layout
│   │   └── partials/
│   │       ├── header.njk     # Site header
│   │       └── footer.njk     # Site footer
│   ├── assets/
│   │   ├── css/
│   │   │   └── main.css       # Main stylesheet
│   │   └── images/            # Image assets
│   ├── blog/
│   │   └── index.njk          # Blog listing page
│   ├── posts/                 # Blog posts directory
│   ├── about.md               # About page
│   ├── newsletter.md          # Newsletter page
│   ├── support.md             # Support page
│   ├── privacy.md             # Privacy policy
│   ├── terms.md               # Terms of service
│   └── index.njk              # Homepage
├── .eleventy.js               # Eleventy configuration
├── package.json               # Node.js dependencies
├── netlify.toml               # Netlify deployment config
└── README.md                  # This file
```

## Getting Started

### Prerequisites

- Node.js 18 or higher
- npm or yarn

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd patron-works-blog
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run serve
```

4. Visit `http://localhost:8080` to view the site

### Building for Production

```bash
npm run build
```

The built site will be in the `_site` directory.

## Content Creation

### Writing Blog Posts

1. Create a new Markdown file in `src/posts/` following the naming convention:
   ```
   YYYY-MM-DD-post-slug.md
   ```

2. Include YAML front matter:
   ```yaml
   ---
   title: "Your Post Title"
   date: 2025-01-07
   description: "Brief description for SEO and social sharing"
   tags: ["tag1", "tag2", "tag3"]
   layout: layouts/post.njk
   featured: false
   image: "/assets/images/posts/post-image.jpg"
   ---
   ```

3. Write your content in Markdown below the front matter

### Adding Images

Place images in `src/assets/images/` and reference them using absolute paths from the site root:
```markdown
![Alt text](/assets/images/your-image.jpg)
```

### Mathematical Notation

Use LaTeX syntax with KaTeX:
- Inline: `$equation$`
- Block: `$$equation$$`

### Code Blocks

Use triple backticks with language specification:
```javascript
// Your code here
```

## Deployment

### Netlify (Recommended)

1. Connect your repository to Netlify
2. Build settings are configured in `netlify.toml`
3. Deploy automatically on push to main branch

### Manual Deployment

1. Run `npm run build`
2. Upload the `_site` directory to your web server

## Configuration

### Site Settings

Edit `src/_data/site.json` to update:
- Site title and description
- Social media links
- Newsletter service URLs
- Support platform links

### Newsletter Integration

Replace the placeholder newsletter forms with your service's embed code:
- ConvertKit
- Mailchimp  
- Buttondown

### Support Integration

Update the support URLs in `src/_data/site.json` with your actual:
- Buy Me a Coffee profile
- Ko-fi profile
- Merchandise store

## Customization

### Styling

The CSS is organized into logical sections in `src/assets/css/main.css`:
- CSS Reset & Base Styles
- CSS Custom Properties (Design Tokens)
- Component Styles
- Layout Styles
- Responsive Design

### Color Scheme

All colors are defined as CSS custom properties in `:root`. Update these to customize the color scheme while maintaining consistency.

### Typography

The site uses Inter font loaded from Google Fonts. Update the font imports in the base layout to use different typography.

## Performance

- Static site generation for fast loading
- Optimized CSS with minimal JavaScript
- Responsive images with proper alt text
- Efficient font loading with `font-display: swap`
- Netlify CDN for global delivery

## SEO

- Semantic HTML structure
- Open Graph and Twitter Card meta tags
- Structured data for blog posts
- Optimized page titles and descriptions
- XML sitemap (auto-generated by Eleventy)

## Browser Support

- Modern browsers (Chrome, Firefox, Safari, Edge)
- Progressive enhancement approach
- Graceful degradation for older browsers

## Contributing

This is a personal blog, but feedback and suggestions are welcome:
- Open issues for bugs or suggestions
- Submit pull requests for improvements
- Connect through social media for discussions

## License

Content is copyrighted. Code is available under MIT license.

---

Built with ❤️ using [Eleventy](https://11ty.dev)
