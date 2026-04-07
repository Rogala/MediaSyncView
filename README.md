# MediaSyncView

**Compare AI images & videos with perfectly synchronized zoom and playback.**

A single HTML file. No installation, no server, no dependencies. Open it in a browser and start comparing.

Based on [MediaSyncer by WhatDreamsCost](https://github.com/WhatDreamsCost/MediaSyncer), GPL-3.0.

---

## What it does

Drop multiple images or videos into the window. Everything stays in sync — playback, scrubbing, zoom, and pan apply to all files at once. Useful for comparing AI model outputs, render iterations, or video takes side by side.

- Synchronized playback and frame-stepping across all loaded videos
- Synchronized zoom and pan — zoom in on one detail, all files follow
- Split View for two-file comparison with a draggable divider
- Grid layout from 1 to 4 rows, supports 2–16+ files simultaneously
- Playback speed control (0.1× to 2×), looping, per-video mute
- Offline-capable — works without internet if `p5.min.js` is placed alongside the HTML file
- Dark and light themes
- UI language auto-detected from browser settings

---

https://github.com/user-attachments/assets/bcd13bc7-c193-42d2-a133-2462f99c12b8

## How to use

**Online:** Download `MediaSyncView.html`, open it in any modern browser.

**Offline:** Place `p5.min.js` (v1.9.4) in the same folder as `MediaSyncView.html`. The player will use it automatically and work without internet access.

Download p5.min.js from the official CDN:
```
https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.9.4/p5.min.js
```

https://github.com/user-attachments/assets/b1ba0b5e-fc57-48ec-ac05-063f7ac86946

---

## Supported formats

**Images:** JPEG, PNG, WebP, AVIF, GIF (static), BMP, SVG, ICO, APNG

**Video containers:** MP4, WebM, Ogg, MKV, MOV (H.264)

**Video codecs:** H.264 (AVC), VP8, VP9, AV1, H.265 (HEVC — hardware support required)

**Audio codecs:** AAC, MP3, Opus, Vorbis, FLAC, PCM (WAV)

Browser support for specific codecs varies. MP4/H.264 and WebM/VP9 have the widest compatibility.

---

https://github.com/user-attachments/assets/3c3ec736-a75d-4366-97ba-30734cb4bfe8

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `Space` | Play / Pause all |
| `← →` | Step one frame |
| `1` `2` `3` `4` | Grid rows |
| `5` | Clear all |
| `6` | Loop |
| `7` | Playback speed |
| `8` | Zoom |
| `9` | Split View (2 files) |
| `0` | Mute / unmute |
| `F` / `F11` | Fullscreen |
| `P` | Toggle panel |
| `I` | Import files |
| `T` | Dark / light theme |
| `H` | Help |
| `Scroll` | Zoom |
| `Middle drag` | Pan |

---

## Localization

The UI language is detected automatically from the browser. Supported languages:

| Code | Language |
|------|----------|
| `en` | English |
| `uk` | Ukrainian |
| `de` | German |
| `fr` | French |
| `es` | Spanish |
| `it` | Italian |
| `pt` | Portuguese (including pt-BR) |
| `zh` | Chinese (Simplified) |
| `ja` | Japanese |

To add a new language: copy any block in the `I18N` object inside the HTML file, change the key (e.g. `ko`), translate the values.

---

## About p5.min.js

`p5.min.js` is the graphics engine that powers MediaSyncView. It handles canvas rendering, synchronized drawing, zoom, and pan.

- Developer: [Processing Foundation](https://p5js.org) (non-profit, USA)
- License: LGPL 2.1
- Size: ~800–1000 KB
- The library runs entirely in the browser — no data collection, no network access after load

MediaSyncView first looks for `p5.min.js` in the same folder. If not found, it loads from the official CDN automatically.

---

## License

GPL-3.0

Based on [MediaSyncer](https://github.com/WhatDreamsCost/MediaSyncer) by [WhatDreamsCost](https://github.com/WhatDreamsCost).
