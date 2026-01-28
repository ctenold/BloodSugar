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

## Brand Values
- **Faith-Grounded Peace**: Rooted in Christian faith - God is our rock and the source of true peace. Users should feel calm and trust, not anxiety or fear.
- **Peaceful & Calming**: This is mindful health journaling, not a clinical medical device. Approach wellness with gratitude and stewardship of the body God gave us.
- **Botanical & Natural**: Use organic, nature-inspired imagery (leaves, growth, sprouts). Avoid blood/medical imagery. Nature reflects God's creation.
- **Green Dominant**: Sage green (#7c9885) is the primary brand color. Avoid red tones. Green symbolizes life, growth, and restoration.
- **Journal Focus**: Emphasize the personal journaling/logging aspect - a treasured record of wellness, not scary data.
- **Premium Wellness Aesthetic**: Soft gradients, rounded organic shapes, gentle shadows. Clean and nurturing.

## Color Palette
- Primary sage: #7c9885
- Dark sage: #5d7a66
- Light sage: #a8c5b0
- Cream accents: #f5f0e8, #faf9f7
- Warning (amber): #d4a574
- Danger (muted coral): #c47f7f
- Blush accent: #e8d5d0
