# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML/CSS resume website for Wang Zichen (王梓晨), a Robotics Engineering student. The resume is designed as a single-page responsive document optimized for both web viewing and PDF printing.

## Project Structure

```
.
├── index.html      # Main resume content (HTML structure)
├── style.css       # All styling, responsive design, and print styles
├── favicon.png     # Website icon
├── codeswing.json  # CodeSwing extension configuration (empty)
└── README.md       # Brief project description
```

## Development

### Viewing the Resume

Open `index.html` directly in a browser, or use the CodeSwing VS Code extension with `codeswing.json`.

### Print to PDF

The resume is optimized for A4 PDF output:
- Open `index.html` in a browser
- Use Ctrl+P (or Cmd+P on Mac)
- Select "Save as PDF" as the destination
- Ensure "Background graphics" is enabled for proper color rendering

## Architecture Notes

### Layout

- Two-column grid layout: sidebar (32%) + main content (68%)
- Responsive: collapses to single column on mobile (< 768px)
- Print-specific styles in `@media print` ensure proper A4 formatting

### CSS Variables

Defined in `:root` at `style.css:1-7`:
- `--primary-color`: #2c3e50 (headings)
- `--accent-color`: #3498db (links, highlights)
- `--text-color`: #333 (body text)
- `--light-gray`: #f8f9fa (skill tags background)
- `--border-color`: #e9ecef (borders)

### Key Sections (index.html)

- **Header** (lines 31-35): Name, pinyin, title, subtitle
- **Contact** (lines 39-52): Email, GitHub, Bilibili links with Font Awesome icons
- **Skills** (lines 54-82): Categorized skill tags (Hardware, Software, Tools)
- **Education** (lines 84-91): University, degree, dates
- **Experience** (lines 119-161): Project and work history with detailed bullet points

### External Dependencies

- Font Awesome 6.4.0 for icons (loaded from CDN in `index.html:9`)
- System font stack with Chinese font support (PingFang SC, Microsoft YaHei, etc.)

## Content Guidelines

When editing the resume:
- Use semantic HTML elements (`<section>`, `<article>`, `<aside>`)
- Maintain the two-column structure for print compatibility
- Keep experience items in reverse chronological order (newest first)
- Use `.skill-tag` spans for skills, `.experience-item` divs for work/projects
