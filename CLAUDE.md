# CLAUDE.md - Personal Website Documentation

## Overview

This is a minimalist personal website for Jacob (Yinsheng) Zhou built with pure HTML, CSS, and minimal JavaScript. The site follows a philosophy of simplicity and performance - no frameworks, no build tools, just clean static files.

## Architecture & Tech Stack

### Core Technologies
- **HTML5** - Pure semantic HTML with no preprocessing
- **CSS3** - Custom CSS with responsive design and CSS Grid
- **Vanilla JavaScript** - Minimal JS for blog routing and interactions
- **Static Assets** - Images and SVG icons in the Assets directory

### Design Philosophy
- Zero frameworks - inspired by the "motherfuckingwebsite" philosophy
- Mobile-first responsive design
- Clean, minimal aesthetic inspired by Andrej Karpathy's website
- Performance-focused with minimal HTTP requests

## Project Structure

```
PersonalWebsite/
├── Index.html          # Main homepage with personal info and timeline
├── blog.html           # Blog page with single-page app routing
├── style.css           # Main stylesheet with responsive design
├── Assets/             # Static assets directory
│   ├── me.jpeg         # Profile photo
│   ├── amazon.png      # Company logos
│   ├── ucla.png        
│   ├── cemail.svg      # Social media icons
│   ├── cgithub.svg     
│   ├── ctwitter.svg    
│   ├── linkedin.svg    
│   └── IMG_0132.jpeg   # Additional images
└── CLAUDE.md          # This documentation file
```

## Key Features

### Homepage (Index.html)
- Personal introduction with profile photo
- Professional timeline with company logos
- Social media links (Twitter, GitHub, LinkedIn, email)
- Responsive grid layout that stacks on mobile
- Interactive email reveal functionality

### Blog (blog.html)
- Single-page application with client-side routing
- Embedded CSS and JavaScript (no external dependencies)
- Clean typography optimized for reading
- Individual blog posts embedded in the same HTML file
- Browser history support for direct linking to posts

### Responsive Design
- CSS Grid-based layout system
- Mobile-first approach with media queries
- Breakpoints: 768px, 992px
- Flexible image sizing and typography scaling

## Development Workflow

### Local Development
Since this is a static website, you can:
1. Open files directly in browser for testing
2. Use any local web server for development:
   ```bash
   # Python 3
   python -m http.server 8000
   
   # Python 2
   python -m SimpleHTTPServer 8000
   
   # Node.js
   npx http-server
   
   # PHP
   php -S localhost:8000
   ```

### File Editing
- **Index.html**: Main content, timeline entries, personal info
- **blog.html**: Blog posts are embedded as `<article>` elements
- **style.css**: All styling including responsive breakpoints
- **Assets/**: Add new images and icons here

### Adding Blog Posts
1. Add new blog entry to the blog list (around line 261 in blog.html)
2. Add corresponding `<article>` element with unique ID
3. Update the JavaScript routing to handle the new post

## Common Tasks

### Updating Personal Information
- Edit the `<h1>` and `<h2>` tags in Index.html
- Update timeline entries in the `#history` section
- Replace profile photo in Assets/ and update src in Index.html

### Adding New Timeline Entry
```html
<div class="entry row">
    <div class="timespan">YYYY - YYYY</div>
    <div class="ico">
        <div class="entry-dot"></div>
        <img src="assets/company-logo.png" />
    </div>
    <div class="desc">
        Your description here.
    </div>
</div>
```

### Styling Customization
- Color scheme: Primarily grayscale with blue accents (#0066cc)
- Typography: System font stack (sans-serif)
- Spacing: Consistent 20px grid system
- Breakpoints: 768px and 992px for responsive design

## Performance Characteristics

### Optimization Features
- Minimal HTTP requests (3 files + assets)
- No external dependencies or CDN requests
- Optimized images with appropriate sizing
- CSS and JS are minified inline in blog.html
- Semantic HTML for better accessibility

### File Sizes
- Index.html: ~3KB
- blog.html: ~13KB (includes embedded CSS/JS)
- style.css: ~4KB
- Total core files: ~20KB

## Browser Compatibility

### Supported Features
- CSS Grid (IE11+ with prefixes)
- Flexbox (IE10+)
- HTML5 semantic elements
- ES6 JavaScript features (modern browsers)

### Graceful Degradation
- Works without JavaScript (except blog routing)
- Responsive images with fallbacks
- Progressive enhancement approach

## Deployment

### Static Hosting Options
- GitHub Pages
- Netlify
- Vercel
- AWS S3 + CloudFront
- Any static file hosting service

### Build Process
No build process required - files are ready for deployment as-is.

## Maintenance Notes

### Regular Updates
- Keep social media links current
- Update timeline with new positions/education
- Add new blog posts as needed
- Refresh profile photo periodically

### Asset Management
- Optimize images before adding to Assets/
- Use SVG for icons when possible
- Maintain consistent naming conventions
- Consider lazy loading for many images

## Code Quality

### HTML Structure
- Semantic HTML5 elements
- Proper heading hierarchy
- Accessible image alt texts
- Clean, indented markup

### CSS Organization
- Logical property grouping
- Consistent naming conventions
- Mobile-first media queries
- Modular component styles

### JavaScript Practices
- Vanilla JS with modern APIs
- Event delegation where appropriate
- No external dependencies
- Progressive enhancement

## Future Enhancements

### Potential Additions
- Dark mode toggle
- Blog RSS feed generation
- Search functionality for blog posts
- Contact form with backend integration
- Analytics integration
- Performance monitoring

### Technical Improvements
- Service worker for offline functionality
- Image lazy loading
- CSS/JS minification pipeline
- Automated asset optimization
- SEO meta tags optimization

## Troubleshooting

### Common Issues
1. **Images not loading**: Check file paths and case sensitivity
2. **CSS not applying**: Verify CSS syntax and media query conditions
3. **Blog routing broken**: Check JavaScript console for errors
4. **Mobile layout issues**: Test responsive breakpoints

### Debug Tools
- Browser developer tools
- HTML/CSS validators
- Lighthouse for performance auditing
- Mobile device testing

## Contact & Links

- **Owner**: Jacob (Yinsheng) Zhou
- **LinkedIn**: https://www.linkedin.com/in/yinsheng-jacob-zhou-107226139/
- **GitHub**: https://github.com/jacobergzhou
- **Current Role**: Software Engineer at Amazon

---

This documentation is designed to help future Claude Code instances understand the codebase structure and common development tasks for this personal website.