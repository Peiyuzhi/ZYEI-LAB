# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

ZYEI LAB is a static landing page website for the Zhongyuan Embodied Intelligence Laboratory (中豫具身智能实验室). It is a single-page website built with vanilla HTML, CSS, and JavaScript—no frameworks or build tools.

## Development Commands

**Deploy to Vercel:**
```bash
vercel deploy
```

There is no build process, test suite, or linting configured. The site is served directly as static files.

## Architecture

The entire website is contained in a single `index.html` file (~6000 lines) with embedded CSS and JavaScript.

### Page Sections
Hero → Stats → News → Research → About → Team → Achievements → Publications → Product Details → Industry Applications → Careers → Cooperation → Contact

### Key JavaScript Features
- Mobile hamburger menu with smooth animations
- Auto-playing hero image carousel
- Smooth scroll navigation
- Scroll-triggered animations and parallax effects
- Image lazy loading via IntersectionObserver
- Scroll progress bar and back-to-top button
- Form handling for contact/visit requests
- Throttled scroll events for performance

### CSS Design System
- Dark theme (#0A0E1A background)
- Tech blue primary (#0066FF), cyan accent (#00FFFF), red accent (#FF3366)
- CSS custom properties for theming
- Mobile-first responsive design with hamburger menu

### Internationalization
Bilingual support (Chinese/English) via data attributes for i18n on text elements.

## Deployment

Hosted on Vercel. Configuration in `vercel.json` specifies no build command—files are served from root directory.

SEO assets: `robots.txt`, `sitemap.xml`, Open Graph meta tags, JSON-LD schema markup.
