# Blockwall Insights - Newsletter Archive

A modern, Web3-styled static website for hosting Blockwall's crypto newsletter archive. Built for GitHub Pages with dark/light mode support.


## ✨ Features

- 🌙 **Dark/Light Mode** - Toggle between themes, preference saved locally
- 📱 **Fully Responsive** - Works on all devices
- ⚡ **Fast & Lightweight** - Pure HTML/CSS, no frameworks
- 🎨 **Modern Web3 Design** - Gradient accents, glass effects, smooth animations
- 📁 **Organized Structure** - Daily/Weekly/Monthly sections ready

---

## 📁 File Structure

```
blockwall-insights/
├── index.html                              # Homepage (Web3 style)
├── README.md                               # This file
├── assets/
│   └── css/
│       ├── archive.css                     # Styles for archive pages
│       └── newsletter.css                  # Styles for newsletter pages
├── daily/
│   ├── index.html                          # Daily archive grid
│   └── blockwall-daily-2026-01-30.html     # Newsletter (example)
├── weekly/
│   └── index.html                          # Coming soon placeholder
└── monthly/
    └── index.html                          # Coming soon placeholder
```

---

## 📝 Adding a New Daily Newsletter

### 1. Create the HTML File

Copy the template file and rename with the new date:
```
blockwall-daily-YYYY-MM-DD.html
```

Example: `blockwall-daily-2026-01-31.html`

### 2. Update Content in the New File

Edit these sections:
- `<title>` - Update date
- `.header-date` - Update date display
- `.stats` - Update source count, bullish/bearish numbers
- `.intro` - Write new intro paragraph
- `.story` blocks - Add each key story with:
  - Title
  - Image URL (use article's OG image when possible)
  - Source, author, category, score
  - **Summary: 3-4 sentences** (factual, contextual)
  - Link to original article
- `.other-list` - Update "Also Worth Reading" links
- `.linkedin-content` - Update LinkedIn post
- `.sources-list` - Update sources

### 3. Add Card to Archive Index

Edit `daily/index.html` and add a new card at the **TOP** of `.cards-grid`:

```html
<a href="blockwall-daily-2026-01-31.html" class="card">
  <div class="card-image">
    <img src="IMAGE_URL" alt="January 31, 2026">
    <div class="card-badge">Latest</div>
  </div>
  <div class="card-content">
    <time class="card-date">January 31, 2026</time>
    <h3 class="card-title">Your Headline Summary Here</h3>
    <div class="card-stats">
      <span class="stat">📊 XX sources</span>
      <span class="stat bullish">🟢 XX bullish</span>
      <span class="stat bearish">🔴 XX bearish</span>
    </div>
  </div>
</a>
```

**Important**: Remove the `<div class="card-badge">Latest</div>` from the previous day's card.

### 4. Commit and Push

```bash
git add .
git commit -m "Add daily newsletter for 2026-01-31"
git push origin main
```

GitHub Pages automatically rebuilds within 1-2 minutes.

---

## 🎨 Customization

### Changing Colors

Edit CSS variables in `assets/css/archive.css` and `assets/css/newsletter.css`:

```css
:root {
  --accent: #6366f1;        /* Primary accent (purple) */
  --accent-hover: #818cf8;  /* Hover state */
  --green: #22c55e;         /* Bullish color */
  --red: #ef4444;           /* Bearish color */
  /* ... */
}
```

### Adding Weekly/Monthly Content

1. Create newsletter files in `weekly/` or `monthly/` folders
2. Update the respective `index.html` to show cards
3. Remove "Coming Soon" placeholder
4. Remove `.soon` class from nav links

---


## 🔧 Troubleshooting

### Site not updating?
- GitHub Pages can take 1-3 minutes to rebuild
- Try hard refresh: `Ctrl+Shift+R` (Windows) or `Cmd+Shift+R` (Mac)
- Check repository → Actions tab for build status

### Images not loading?
- Ensure image URLs use `https://`
- Check that onerror fallback is set
- Verify the source website allows hotlinking

### Theme not saving?
- Make sure JavaScript is enabled
- localStorage must be allowed in browser

---

## 📞 Support

For questions or issues, contact the Blockwall team.

---

**Blockwall Capital** • Frankfurt, Germany  
*European Crypto Venture Capital*
