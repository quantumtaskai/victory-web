## Standard Workflow
1. First think through the problem, read the codebase for relevant files, and write a plan to tasks/todo.md.
2. The plan should have a list of todo items that you can check off as you complete them
3. Before you begin working, check in with me and I will verify the plan.
4. Then, begin working on the todo items, marking them as complete as you go.
5. Please every step of the way just give me a high level explanation of what changes you made
6. Make every task and code change you do as simple as possible. We want to avoid making any massive or complex changes. Every change should impact as little code as possible. Everything is about simplicity.
7. Finally, add a review section to the todo.md file with a summary of the changes you made and any other relevant information.


# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website for Victory International Trading LLC, a Dubai-based international trading company specializing in FMCG distribution, commodity trading, and global logistics. The company has been operating for 45+ years across 5+ countries including UAE, India, Myanmar, and Indonesia.

## Architecture

### Technology Stack
- **Frontend**: Pure HTML5, CSS3, and vanilla JavaScript
- **Styling**: Tailwind CSS (via CDN)
- **Fonts**: Inter font family from Google Fonts
- **Structure**: Single-page application with multiple sections

### File Structure
- `index.html` - Main website with complete mobile-responsive design and advanced animations
- `test.html` - Simplified version of the website
- `test1.html` - Additional test version
- Static assets:
  - `victory_logo.png` & `victory_logo-tr.png` - Company logos
  - `shipping-port-sunset.png` - Hero section background
  - `global-network-map.png`, `logistics-network.png`, `container-ship.png` - Section images
  - `brand-partners-grid.png` - Brand partners showcase
  - `img/` folder - Additional images (001.png, numbered jpg files)

### Website Sections
1. **Navigation** - Fixed glass-effect navbar with mobile menu
2. **Hero Section** - Full-screen with shipping background, company stats, and CTA buttons
3. **Company Description** - Two-column layout with floating achievement cards
4. **Brand Partners** - Grid showcase with 1000+ brand logos and category highlights
5. **Services** - Worldwide delivery solutions with logistics network visualization
6. **Trusted Brand** - Industry focus and track record statistics
7. **Contact Form** - Modern form with container ship imagery
8. **Footer** - Complete contact information and social links

## Development Commands

This is a static website project with no build system or package manager. Development can be done by:

### Local Development
```bash
# Option 1: Simple HTTP server (Python)
python -m http.server 8000

# Option 2: Simple HTTP server (Node.js)
npx http-server .

# Option 3: Open directly in browser
open index.html
```

### File Editing
- Edit HTML directly in `index.html`
- CSS is embedded in `<style>` tags within the HTML
- JavaScript is embedded in `<script>` tags at the bottom
- No compilation or build process required

## Key Features

### Mobile Responsiveness
- Fully responsive design with mobile-first approach
- Touch-friendly hover effects with `@media (hover: hover)`
- Mobile-specific classes: `mobile-text-lg`, `mobile-p-4`, `mobile-mt-4`
- Optimized animations with `@media (prefers-reduced-motion: reduce)`

### Performance Optimizations
- CDN-loaded external resources (Tailwind CSS, Google Fonts)
- Optimized images and WebM video support
- CSS animations with hardware acceleration
- Proper meta viewport configuration

### Interactive Elements
- Smooth scroll navigation
- Mobile hamburger menu with overlay
- Dynamic navbar background on scroll
- Hover animations and glass effects
- Form validation (basic HTML5)

## Contact Information
- **Email**: info@victorydubai.com
- **Phone**: +971 50 646 2507
- **WhatsApp**: +971 58 198 4500
- **Address**: P O Box 33551, Dubai, UAE

## Content Guidelines

### Company Information
- Founded: 1988 (45+ years experience)
- Global presence: Dubai (HQ), India, Myanmar, Indonesia
- Products: 200-300 product range
- Industries: FMCG, Commodities, Tyres, Cars
- Key stats: 1000+ brands, 50+ categories, 24/7 support

### Brand Voice
- Professional yet approachable
- Focus on trust, reliability, and global reach
- Emphasis on experience and established partnerships
- Clean, modern design aesthetic

## Making Changes

When updating the website:
1. All changes are made directly to HTML files
2. Test across different screen sizes and devices
3. Ensure mobile menu functionality works properly
4. Verify all animations are smooth and accessible
5. Check that contact information remains accurate
6. Test form functionality if modified