# 🎬 ClipStudio

Turn a long video into a vertical **Short** (9:16) entirely in your browser. Load a video, find a good moment, reframe it to vertical, add hook text and captions, mix in background music, and export — no server, no uploads, no build step, no dependencies.

ClipStudio is a single `index.html` file. Open it in any modern browser (Chrome, Edge, Firefox, or Safari 14.1+) and it runs. Your video never leaves your device.

## Features

- **Local video loading** and a live 9:16 canvas preview.
- **Moment finder** — an *audio-energy heuristic* (not speech recognition) ranks up to eight non-overlapping candidate moments. See the honest limitations in-app and in `KNOWN_ISSUES.md`.
- **Timeline scrubbing** with start/end trim controls, plus a touch-friendly audio-energy waveform overview with draggable trim handles.
- **Reframing** — blurred background, fill (crop), or fit (black bars), plus zoom and pan.
- **Hook text** with an adjustable display duration, shown from the clip start in both preview and export.
- **Captions** — import SRT or WebVTT, or paste manual timestamps; styling, size, colour, timing offset, vertical position and presets.
- **Safe-area guides** for TikTok/Reels/Shorts overlays.
- **Audio** — background music, voice level, auto-ducking with adjustable strength/threshold, fade in/out, and a limiter to help prevent clipping.
- **Export** — single clip, or a batch queue (with per-item status and cancellation) of ticked moments. Exports MP4 or WebM depending on what the browser actually records (detected and reported automatically).
- **PNG thumbnail export** — scrub the timeline or step a frame to pick the exact frame.
- **YouTube helper** — copy title/description and open YouTube's upload page. The app cannot publish to YouTube for you.
- **Local settings** saved in `localStorage` (settings only, never media), with a reset option.

## Usage

1. Open `index.html` (or the GitHub Pages URL).
2. Load a video.
3. Optionally click **Find best moments**, pick one, and adjust the trim.
4. Set the reframe, hook, captions and music.
5. Click **Render & export video**, or use **Export ticked moments** for a batch.
6. Download the result and upload it wherever you like.

## Technical notes

- Plain HTML, CSS and JavaScript. No build step, no framework, no large dependency.
- All video and audio processing stays on the user's device; media is never uploaded.
- Export uses the browser's `MediaRecorder` + `canvas.captureStream()`. The container/codec (MP4/H.264 or WebM) is detected and reported.

## License

Provided as-is. You are responsible for the rights to any media you use.
