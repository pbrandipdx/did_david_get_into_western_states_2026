# Western States 2026 Waitlist Checker

A simple, beautiful single-page website that automatically checks if David Allamon got into the Western States 2026 race.

## Features

- 🔄 **Auto-refresh**: Automatically checks the waitlist when the page loads
- 🎆 **Fireworks animation**: Celebratory fireworks display if David got in
- 📊 **Waitlist position**: Shows current position if still on the waitlist
- 📱 **Responsive design**: Works beautifully on desktop and mobile
- ⚡ **No dependencies**: Pure HTML/CSS/JavaScript

## How It Works

The website fetches the official Western States 2026 waitlist from https://www.wser.org/2026-wait-list/ and:

1. Searches for David Allamon in the table
2. Checks if his status shows "Entered" (meaning he got in)
3. If YES: Displays animated fireworks and celebration message
4. If NO: Shows his current position on the waitlist with encouragement

## Deployment to GitHub Pages

### Option 1: Create a New Repository

1. Go to https://github.com and create a new repository
2. Name it something like `western-states-checker`
3. Make it public
4. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/YOUR-USERNAME/western-states-checker.git
   ```
5. Copy `index.html` into the repository folder
6. Commit and push:
   ```bash
   git add index.html
   git commit -m "Add Western States waitlist checker"
   git push origin main
   ```
7. Go to your repository settings on GitHub
8. Navigate to "Pages" in the left sidebar
9. Under "Source", select "main" branch and click "Save"
10. Your site will be live at: `https://YOUR-USERNAME.github.io/western-states-checker/`

### Option 2: Use an Existing Repository

1. Copy `index.html` to your existing repository
2. Commit and push the changes
3. Enable GitHub Pages in repository settings (if not already enabled)

## Local Testing

Simply open `index.html` in your web browser. Note that due to CORS restrictions, you may need to use a CORS proxy (already implemented in the code) or run a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve
```

Then visit `http://localhost:8000` in your browser.

## Technical Details

- **CORS Handling**: Uses `allorigins.win` as a CORS proxy to fetch the waitlist
- **HTML Parsing**: Uses DOMParser to extract table data
- **Canvas Animation**: Custom fireworks particle system using HTML5 Canvas
- **CSS Animations**: Smooth transitions and keyframe animations for text effects

## Historical Context

The website includes encouraging historical data:
- 2025: 65th runner got in on Thursday before the race
- 2024: 35th runner got in on Friday afternoon
- 2023: 56th position got in a couple days before
- 2022 & 2021: Entire waitlist was exhausted

## Browser Compatibility

Works in all modern browsers:
- Chrome/Edge (recommended)
- Firefox
- Safari
- Opera

Requires ES6+ support (all browsers from ~2017 onwards).

## License

Free to use and modify as needed.

## Support

If the waitlist page structure changes and the checker stops working, you may need to update the HTML parsing logic in the `parseWaitlist()` function.

