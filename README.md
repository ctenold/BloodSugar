# Blood Sugar Tracker 🩸

A Progressive Web App (PWA) for tracking blood glucose levels throughout the day with personalized ranges, trend visualization, and cloud sync.

## Features

✅ **Profile-Based Ranges**
- Male/Female (Standard ranges)
- Pregnant Female (Gestational diabetes monitoring with stricter ranges)

✅ **Comprehensive Tracking**
- Morning Fasting
- Pre-Lunch / Pre-Dinner
- Post-Meal readings (1hr and 2hr)
- Custom tags with custom ranges

✅ **Visual Insights**
- Interactive trend chart with multi-tag visualization
- Color-coded readings (green/yellow/red)
- Time-in-range percentage
- Average, high, and low readings

✅ **Daily Encouragement**
- Bible verse of the day (ESV) focused on hope and endurance

✅ **Data Management**
- Local storage (works offline)
- Download/Upload JSON backups
- Google Drive sync (optional)

✅ **Mobile-First Design**
- Touch-friendly interface
- Dark/Light theme
- Installable as native app
- Works offline after first visit

## Setup for GitHub Pages

1. **Create Icons**
   You'll need to create two icon files:
   - `icon-192.png` (192x192 pixels)
   - `icon-512.png` (512x512 pixels)
   
   Use a medical/health-related icon (blood drop, chart, medical cross, etc.)

2. **Upload Files**
   Upload these files to your GitHub repository:
   - `blood-sugar-tracker.html` (rename to `index.html` if you want it as the main page)
   - `manifest.json`
   - `sw.js`
   - `icon-192.png`
   - `icon-512.png`

3. **Enable GitHub Pages**
   - Go to repository Settings → Pages
   - Select branch (usually `main` or `gh-pages`)
   - Save and wait for deployment

4. **Google Drive Sync Setup**
   The app uses a Google OAuth client ID. To set up your own:
   - Go to [Google Cloud Console](https://console.cloud.google.com)
   - Create a new project
   - Enable Google Drive API
   - Create OAuth 2.0 credentials
   - Add your GitHub Pages URL to authorized origins
   - Replace the client_id in the HTML file (line ~1447 and ~1452)

## Usage

### First Time Setup
1. Open the app
2. Select your profile (Male, Female, or Pregnant Female)
3. Start logging readings!

### Adding a Reading
1. Click "Add Reading" button
2. Time is auto-set (can be edited)
3. Select tag (or create custom tag)
4. Enter blood sugar reading (mg/dL)
5. Add optional notes
6. Submit

### Custom Tags
- Select "Add Custom Tag" from dropdown
- Enter tag name (e.g., "Evening Snack")
- Set target range
- Tag will be saved for future use

### Viewing Trends
- Chart shows readings over time
- Toggle different time ranges (7d, 14d, 30d, 90d)
- Click legend items to show/hide specific tags
- Each tag has a unique color

### Data Backup
**Download:**
- Settings → Download Data (JSON)
- Saves complete history to your device

**Upload:**
- Settings → Upload Data
- Restore from previous backup

**Google Drive Sync:**
- Settings → Sync with Google Drive
- Sign in with Google account
- Syncs automatically across devices
- Uses conflict resolution (newest wins)

## Blood Sugar Ranges

### Standard (Male & Female Non-Pregnant)
- **Morning Fasting:** 70-100 mg/dL (normal), 100-125 (prediabetic), >125 (diabetic)
- **Pre-Meal:** 70-130 mg/dL
- **Post-Meal (1hr):** <180 mg/dL
- **Post-Meal (2hr):** <140 mg/dL

### Pregnant Female (Gestational Diabetes)
- **Morning Fasting:** <95 mg/dL
- **Pre-Meal:** <100 mg/dL
- **Post-Meal (1hr):** <140 mg/dL
- **Post-Meal (2hr):** <120 mg/dL

*Note: These are general guidelines. Always consult with your healthcare provider for personalized targets.*

## Privacy

- All data is stored locally in your browser by default
- Google Drive sync is optional and requires explicit sign-in
- No data is sent to any other servers
- No tracking or analytics
- You own your data completely

## Technical Details

- **Framework:** Vanilla JavaScript (no dependencies except Chart.js)
- **Storage:** localStorage for offline-first functionality
- **Charts:** Chart.js for trend visualization
- **Auth:** Google Identity Services for Drive sync
- **PWA:** Service Worker for offline support and installability

## Browser Compatibility

Works on all modern browsers:
- Chrome/Edge (Desktop & Mobile)
- Safari (Desktop & Mobile)
- Firefox (Desktop & Mobile)

For best experience on iOS: Add to Home Screen from Safari

## Contributing

Feel free to fork and customize for your needs. Some ideas:
- Add insulin tracking
- Meal/carb logging
- HbA1c calculator
- Export to PDF reports
- Medication reminders

## License

Free to use and modify. No attribution required.

## Medical Disclaimer

This app is for tracking purposes only and is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of your physician or other qualified health provider with any questions you may have regarding a medical condition.

---

Made with ❤️ for better health management
