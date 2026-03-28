<div align="center">

# 🖼️ STRETCHPIC

### **Stretching Your Pic to the Newest X Pic New Setting**

<p align="center">
  <strong>Instantly stretch any image to the viral 1:10 ratio (500×5000px) for Twitter/X</strong>
</p>

<p align="center">
  <a href="#"><img src="https://img.shields.io/badge/Demo-Live-brightgreen?style=for-the-badge&logo=vercel" alt="Live Demo"></a>
  <a href="#-quick-start"><img src="https://img.shields.io/badge/Quick-Start-blue?style=for-the-badge&logo=rocket" alt="Quick Start"></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" alt="License"></a>
  <a href="https://github.com/revengerrr/stretchpic/stargazers"><img src="https://img.shields.io/github/stars/revengerrr/stretchpic?style=for-the-badge&logo=github" alt="Stars"></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-Canvas_API-E34F26?style=flat-square&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/JavaScript-Vanilla-F7DF1E?style=flat-square&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/Zero-Dependencies-00C853?style=flat-square" alt="Zero Dependencies">
  <img src="https://img.shields.io/badge/100%25-Client--Side-0077CC?style=flat-square" alt="Client Side">
  <img src="https://img.shields.io/badge/File_Size-~8KB-9C27B0?style=flat-square" alt="File Size">
</p>

---

**[🌐 Live Demo](#)** | **[📖 How It Works](#-how-it-works)** | **[🚀 Deploy Your Own](#-deployment)** | **[💖 Donate](#-support--donate)**

---

</div>

## 🎯 **What is STRETCHPIC?**

STRETCHPIC is a **free, browser-based tool** that stretches any image to the trending **1:10 ratio (500×5000px)** format that's currently going viral on Twitter/X. No servers, no AI, no signups — just pure client-side image processing.

### **The Trend**

Twitter/X now supports super-tall images in the timeline. Posts with a **500×5000px (1:10 ratio)** image take up massive vertical screen space, making them impossible to scroll past. Content creators and meme accounts are using this format to **dominate the timeline**.

### **The Problem**

- ❌ **Photoshop is overkill** — You don't need a $20/mo app to resize an image
- ❌ **Online tools upload your data** — Most image tools send your files to their servers
- ❌ **Cropping loses content** — Center-cropping cuts out parts of your image
- ❌ **Manual resizing is tedious** — Setting exact pixel dimensions every time gets old fast

### **The Solution**

STRETCHPIC does **one thing perfectly**: stretches your entire image to the 1:10 ratio.

- ✅ **Full image preserved** — Everything stays visible, just distorted/stretched
- ✅ **100% private** — Nothing leaves your browser. Ever.
- ✅ **Instant** — Drop image → Download result. Two clicks.
- ✅ **Zero cost** — Free forever, no ads, no premium tier

---

## ✨ **Features**

<table>
<tr>
<td width="50%">

### 🖱️ **Drag & Drop Upload**
Drop any image directly onto the page. Supports PNG, JPG, and WebP formats.

### 📐 **Custom Dimensions**
Default is 500×5000px but you can set any custom width and height.

### 🔄 **Real-Time Preview**
Side-by-side comparison of original vs. stretched result before downloading.

</td>
<td width="50%">

### 📦 **Multiple Export Formats**
Export as PNG (lossless), JPEG (smaller file), or WebP (modern format).

### 🔒 **100% Client-Side**
All processing happens in your browser using the HTML Canvas API. Zero server calls.

### ⚡ **Single HTML File**
No build tools, no npm, no frameworks. One file, works anywhere.

</td>
</tr>
</table>

---

## 🚀 **Quick Start**

### **Method 1: Just Open It** (Fastest)

```
Download index.html → Double-click → Done
```

### **Method 2: Deploy to Vercel**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/revengerrr/stretchpic)

```bash
# Or manually
git clone https://github.com/revengerrr/stretchpic.git
cd stretchpic
vercel --prod
```

### **Method 3: GitHub Pages**

1. Fork this repo
2. Go to **Settings** → **Pages**
3. Select **main** branch → **Save**
4. Your site is live at `https://yourusername.github.io/stretchpic`

---

## 🎨 **How It Works**

### **The Stretch Algorithm**

It's beautifully simple. The HTML Canvas API's `drawImage` method maps the entire source image to new dimensions:

```javascript
// Source: full original image
// Destination: 500×5000 canvas
ctx.drawImage(
  image,
  0, 0, originalWidth, originalHeight,  // source rectangle (full image)
  0, 0, 500, 5000                       // destination rectangle (stretched)
);
```

### **Why Stretch Instead of Crop?**

| Method | What Happens | Result |
|--------|-------------|--------|
| **Center Crop** | Cuts edges, keeps center | Loses content |
| **Fit + Letterbox** | Adds black bars | Wastes space |
| **AI Upscale** | Generates fake pixels | Slow, needs server |
| **Stretch (STRETCHPIC)** | Maps all pixels to new size | Full image, distorted proportions |

For viral/meme content on X, the distortion **IS** the aesthetic. That's the whole point of the trend.

### **Processing Flow**

```
┌──────────────┐     ┌──────────────┐     ┌──────────────┐
│  User drops   │────▶│ Canvas API   │────▶│  Download    │
│  image file   │     │ drawImage()  │     │  stretched   │
│  (any size)   │     │ 500 × 5000   │     │  result      │
└──────────────┘     └──────────────┘     └──────────────┘
       PNG                                    PNG/JPG/WebP
       JPG               Browser only          Your choice
       WebP              No upload
```

---

## 🛠️ **Tech Stack**

| Component | Technology | Why |
|-----------|-----------|-----|
| **UI** | HTML + CSS | Zero dependencies, instant load |
| **Fonts** | Outfit + DM Sans | Clean, modern, not generic |
| **Processing** | Canvas API | Native browser image manipulation |
| **Styling** | CSS Variables | Consistent ocean-blue theme |
| **Hosting** | Vercel / GitHub Pages / Anywhere | Static file, works everywhere |

### **File Structure**

```
stretchpic/
├── index.html          # The entire app (single file)
├── README.md           # You're reading this
└── LICENSE             # MIT License
```

Yes, that's it. The entire application is **one HTML file** under 10KB.

---

## 📊 **Browser Support**

| Browser | Supported | Notes |
|---------|-----------|-------|
| Chrome 60+ | ✅ | Full support |
| Firefox 55+ | ✅ | Full support |
| Safari 11+ | ✅ | Full support |
| Edge 79+ | ✅ | Full support |
| Mobile Chrome | ✅ | Touch drag & drop |
| Mobile Safari | ✅ | File picker fallback |

---

## 🔐 **Privacy**

STRETCHPIC takes your privacy seriously by doing **absolutely nothing** with your data:

- ✅ **No server uploads** — Your images never leave your device
- ✅ **No cookies** — Nothing is tracked or stored
- ✅ **No analytics** — No Google Analytics, no Mixpanel, nothing
- ✅ **No accounts** — No signup, no login, no email collection
- ✅ **No ads** — Clean interface, zero monetization
- ✅ **Fully offline capable** — Works without internet after first load

---

## 🗺️ **Roadmap**

### **v1.0 — Core** ✅ (Current)
- [x] Drag & drop image upload
- [x] Stretch to 1:10 ratio (500×5000px)
- [x] Custom output dimensions
- [x] PNG / JPEG / WebP export
- [x] Side-by-side preview
- [x] Mobile responsive

### **v1.1 — Enhancements** 🚧 (Planned)
- [ ] Batch processing (multiple images)
- [ ] Preset ratios (1:10, 1:5, 1:3, 9:16)
- [ ] Quality slider for JPEG/WebP
- [ ] Dark mode toggle

### **v2.0 — Power Features** 🔮 (Future)
- [ ] Before/after slider preview
- [ ] Image filters (brightness, contrast, saturation)
- [ ] Watermark overlay option
- [ ] Share directly to X/Twitter
- [ ] PWA (installable app)

---

## 💖 **Support & Donate**

STRETCHPIC is **free and open source**. If this tool saved you time or you just want to support the development, consider buying me a coffee (or a whole meal):

### **Crypto Donations**

| Network | Address |
|---------|---------|
| **Bitcoin (BTC)** | `bc1qs6al7mcvyaejz8knfgg5gc90nr7eumknm26x7x` |
| **Ethereum (ETH)** | `0xc24a66C4428E8d4a6b6A771bf170EBA86c6f3Cc` |
| **Solana (SOL)** | `4vyomkhcqdp66vzbq8gHcc3mPiRW2Mm8uFT7NVq88EH4` |

Every donation helps keep this project alive and ad-free. Thank you! 🙏

---

## 🤝 **Contributing**

Contributions are welcome! Here's how:

### **Ways to Contribute**

- 🐛 **Report Bugs** — Open an issue with steps to reproduce
- 💡 **Suggest Features** — Share ideas in discussions
- 📝 **Improve Docs** — Fix typos, add examples
- 💻 **Submit PRs** — Code improvements welcome

### **Development**

```bash
# 1. Fork the repo
# 2. Clone your fork
git clone https://github.com/YOUR_USERNAME/stretchpic.git

# 3. Make changes (it's just one HTML file!)
# 4. Open index.html in browser to test
# 5. Commit and push
git commit -m "Add cool feature"
git push origin main

# 6. Open a Pull Request
```

---

## 📄 **License**

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

```
MIT License - Copyright (c) 2026 revengerrr

Permission is hereby granted, free of charge, to use, copy, modify, merge,
publish, distribute, sublicense, and/or sell copies of the Software.
```

---

## 📞 **Links**

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-revengerrr-black?style=for-the-badge&logo=github)](https://github.com/revengerrr)
[![Twitter](https://img.shields.io/badge/X-@revengerlabs-000000?style=for-the-badge&logo=x)](https://x.com/revengerlabs)
[![Issues](https://img.shields.io/badge/Issues-Report_Bug-red?style=for-the-badge&logo=github)](https://github.com/revengerrr/stretchpic/issues)

</div>

---

<div align="center">

### **Made with 🌊 by [@revengerlabs](https://x.com/revengerlabs)**

**[⭐ Star this repo](https://github.com/revengerrr/stretchpic)** if you find it useful!

---

**[🌐 Live Demo](#)** • **[🐛 Report Bug](https://github.com/revengerrr/stretchpic/issues)** • **[💡 Request Feature](https://github.com/revengerrr/stretchpic/issues)** • **[💖 Donate](#-support--donate)**

</div>
