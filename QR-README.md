# Social QR Code Generator

A mobile-friendly web page for sharing social media profiles and contact information via QR codes at networking events.

![Mobile First Design](https://img.shields.io/badge/Mobile-First-orange)
![No Dependencies](https://img.shields.io/badge/Dependencies-QRCode.js%20only-green)
![License](https://img.shields.io/badge/License-MIT-blue)

## Features

- 📱 Mobile-optimized interface
- 🎨 Clean, professional design
- 🔄 Dynamic QR code generation
- 📇 vCard support for contact sharing
- 🌐 Works offline once loaded
- 🎯 Deep linking for social media apps
- 💤 Screen wake lock to keep display on

## Demo

Perfect for:
- Networking events
- Conferences
- Business cards replacement
- Content creators
- Sales professionals

## Quick Start

1. Download `qr-template.html`
2. Open in a text editor
3. Find the `CONFIG` section (around line 302)
4. Update your information:

```javascript
const CONFIG = {
    name: 'YOUR NAME',

    tiktok: 'https://www.tiktok.com/@yourusername',
    youtube: 'https://www.youtube.com/@YourChannel',
    instagram: 'https://www.instagram.com/yourusername',

    contact: {
        fullName: 'Your Full Name',
        phone: '+1234567890',
        email: 'your.email@example.com',
        company: 'Your Company',
        jobTitle: 'Your Job Title',
        website: 'https://yourwebsite.com',
        howWeMet: 'Met at networking event'
    }
};
```

5. Save and open in your browser
6. Add to your phone's home screen for quick access

## Customization

### Adding More Social Platforms

1. Add a button in the HTML:

```html
<button class="qr-button" onclick="showQR('twitter')">
    <div style="display: flex; align-items: center; flex: 1;">
        <div class="icon">🐦</div>
        <div class="content">
            <div>Twitter</div>
            <div class="subtitle">@yourusername</div>
        </div>
    </div>
    <div class="arrow">→</div>
</button>
```

2. Add the URL to CONFIG:

```javascript
const CONFIG = {
    // ... existing config
    twitter: 'https://twitter.com/yourusername',
};
```

3. Add to qrData object:

```javascript
const qrData = {
    // ... existing data
    twitter: {
        title: 'Twitter',
        subtitle: 'Follow on Twitter',
        url: CONFIG.twitter
    }
};
```

### Changing Colors

The template uses an orange/cream theme. To customize:

**Primary Accent Color:**
Find and replace `#d97706` (orange) with your color

**Secondary Accent:**
Find and replace `#f59e0b` (light orange) with your color

**Background:**
Update the gradient in `body`:
```css
background: linear-gradient(to bottom, #faf9f7 0%, #ffffff 100%);
```

### Custom Icons

Replace emoji icons with:
- Other emojis
- SVG icons
- Icon fonts (Font Awesome, etc.)

## How It Works

1. **Menu View**: Displays buttons for each social platform
2. **QR Generation**: Clicking a button generates a QR code using QRCode.js
3. **Full Screen Display**: QR code shows full-screen for easy scanning
4. **vCard Format**: Contact info uses industry-standard vCard 3.0

## Browser Support

- ✅ iOS 12+ (Safari)
- ✅ Android 8+ (Chrome)
- ✅ All modern desktop browsers

## vCard Fields Supported

- Full Name (FN, N)
- Phone Number (TEL)
- Email (EMAIL)
- Company (ORG)
- Job Title (TITLE)
- Website (URL)
- Custom Note (NOTE)

## Deep Linking

The template supports deep linking for:
- Instagram: Opens app if installed, web otherwise
- TikTok: Opens app if installed, web otherwise
- YouTube: Opens app if installed, web otherwise

URLs automatically handle fallbacks to web versions.

## Mobile Web App

To add to home screen:

**iOS:**
1. Open in Safari
2. Tap share button
3. Select "Add to Home Screen"

**Android:**
1. Open in Chrome
2. Tap menu (⋮)
3. Select "Add to Home Screen"

## Deployment

### GitHub Pages

1. Create a new repository
2. Upload `qr-template.html` (rename to `index.html`)
3. Enable GitHub Pages in settings
4. Access at `https://yourusername.github.io/repo-name`

### Other Hosting

Upload to any static hosting:
- Netlify
- Vercel
- AWS S3
- Your own web server

## Dependencies

- [QRCode.js](https://github.com/davidshimjs/qrcodejs) - QR code generation library (loaded from CDN)

## Privacy & Security

- No tracking or analytics
- No data collected
- Runs entirely client-side
- No server requests after initial load
- Works offline

## License

MIT License - feel free to use for personal or commercial projects

## Contributing

Contributions welcome! Please feel free to submit a Pull Request.

## Support

If you found this useful, consider:
- ⭐ Starring the repository
- 🐛 Reporting bugs
- 💡 Suggesting features

## Credits

Created for networking professionals and content creators who want a modern, mobile-first solution for sharing contact information.

---

**Need help?** Open an issue on GitHub
