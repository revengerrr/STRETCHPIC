# STRETCHPIC

**Stretching your pic to the newest X pic new setting.**

A simple browser tool that stretches any image to the trending **1:10 ratio (500×5000px)** for Twitter/X — no server, no AI, no signup.

---

## What is this?

Twitter/X recently introduced a new image display setting that supports super tall images with a **500:5000px (1:10)** ratio. Posts using this format are going viral because they take up massive screen real estate on the timeline.

**STRETCHPIC** lets you convert any image to this ratio instantly — just drop your image and download the result.

## Features

- **Drag & drop** or click to upload
- **Stretch / distort** mode — your full image is visible, not cropped or zoomed
- **Custom output size** — default 500×5000, but you can change it
- **Multiple formats** — export as PNG, JPEG, or WebP
- **100% client-side** — nothing leaves your browser. Zero uploads, zero tracking
- **Single HTML file** — no build tools, no dependencies, no frameworks

## Demo

1. Open `stretchpic.html` in your browser
2. Drop an image
3. Preview the stretched result
4. Hit **Download**
5. Post it on X and watch the engagement

## Usage

### Option 1: Just open it
```
Double-click stretchpic.html → done
```

### Option 2: Deploy to Vercel
```bash
# Just drop the file in a folder and deploy
vercel --prod
```

### Option 3: GitHub Pages
Push to a repo → Settings → Pages → Select branch → your site is live.

## How it works

It uses the HTML Canvas API to redraw your image at the target dimensions:

```js
ctx.drawImage(img, 0, 0, originalW, originalH, 0, 0, 500, 5000);
```

That's it. The entire source image gets mapped to the new dimensions — stretched, not cropped. No AI upscaling, no smart fill, just pure pixel stretching.

## Tech

- Vanilla HTML/CSS/JS
- Canvas API for image processing
- Zero dependencies
- Single file (~400 lines)

## Why stretch and not crop?

Cropping cuts out parts of your image. Stretching keeps **everything visible** — it just distorts the proportions. For meme content and viral posts, the distortion IS the point.

## License

MIT — do whatever you want with it.

---

**Made for the timeline.** 🌊
