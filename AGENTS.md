# AGENTS.md - Blood Sugar Tracker

## Overview
A single-page Progressive Web App (PWA) for tracking blood glucose levels. Pure vanilla JavaScript with no build system.

## Commands
- **Run locally:** Open `blood-sugar-tracker.html` in a browser (no server required)
- **Deploy:** Push to GitHub and enable GitHub Pages
- **No build, lint, or test commands** - this is a static HTML/JS app

## Architecture
- `blood-sugar-tracker.html` - Main app (HTML, CSS, JS all inline, ~1760 lines)
- `manifest.json` - PWA manifest for installability
- `sw.js` - Service worker for offline caching
- **External deps:** Chart.js (CDN), Google Identity Services (CDN)
- **Storage:** localStorage for data, optional Google Drive sync

## Code Style
- Vanilla JavaScript (ES6+), no framework
- CSS custom properties for theming (light/dark mode)
- All code in single HTML file (embedded `<style>` and `<script>`)
- Use `var(--property)` for colors to support theme switching
- Inline event handlers in HTML templates, `addEventListener` for static elements
- Data stored as JSON object in `appData` (profile, readings, customTags, theme)
- Use `saveData()` after modifying `appData`, call `updateUI()` to refresh
