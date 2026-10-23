# Pulse

**A browser-based music visualizer and audio-to-art studio.** Pulse turns local audio into reactive visuals, analyzes a track's sonic characteristics, and creates a downloadable poster—all without uploading the audio to a server.

## Features

- **Six visual styles:** Orbit, Ribbon, Bars, Tunnel, Ridges and Grid (keys 1–6).
- **Multiple audio sources:** local audio files, drag-and-drop, demo beat, microphone, browser-tab audio capture, and Audius search.
- **Song DNA analysis:** estimates energy, spectral brightness, bass share, dynamic range, and tempo from local audio. Includes a loudness timeline and a descriptive audio profile.
- **Song poster studio:** creates a high-resolution 1600 × 2000 PNG with a circular track fingerprint, loudness variation, brightness-based color, duration, and loudest moment.
- **Mood-aware visuals:** audio features can influence visualization style and palette.
- **Auto mode:** cycle styles on a timer or let mood mode choose a style.
- **Interaction:** touch and mouse particle interaction, swipe-to-change style, auto-hiding controls, keyboard synth, and keyboard shortcuts.
- **Share and record:** screenshots, WebM recording with audio where supported, fullscreen, and shareable visual settings links.
- **Color options:** built-in palettes, artist-inspired palettes, and album-art color extraction where supported.
- **Privacy-first:** local audio analysis happens in the browser; Pulse does not upload local audio files.
- **No build step or dependencies required.**

## Run locally

Open `index.html` in a modern browser, or serve the folder (recommended for browser APIs):

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Using Song DNA and posters

1. Choose **Open a song** and select a local audio file.
2. Open **Settings**.
3. Select **Song DNA** to see the track metrics and sampled loudness timeline, or **Make a poster** to generate a visual fingerprint.
4. Download the poster as a PNG.

Metrics are estimates derived from signal processing, not professional mastering measurements or guaranteed music-structure detection. Tempo is an estimate and can be ambiguous for tracks with sparse percussion, unusual timing, or half-time/double-time rhythms. Browser memory and processing time depend on the length and format of the audio file.

## Browser support and limitations

- Visualization, demo beat, and local playback work in modern browsers.
- Microphone and tab capture require browser permission; tab-audio capture is best supported in desktop Chromium browsers.
- Recording depends on MediaRecorder and supported output formats.
- Some remote music streams do not permit audio analysis; Song DNA and poster generation are designed for local files.
- Album-art extraction depends on the image source permitting browser access.

## Project roadmap

- [x] Auto mode, auto-hide controls, touch/mouse interaction, and shareable settings.
- [x] Local Song DNA dashboard and loudness timeline.
- [x] High-resolution circular song poster export.
- [ ] Additional poster layouts (linear fingerprint, minimal cover, waveform).
- [ ] Save/load named presets.
- [ ] More robust beat and musical-section estimation.
- [ ] Automated browser testing and performance profiling on long tracks.

## Git workflow

Keep each meaningful feature in its own commit so progress is easy to explain in a portfolio or interview:

```bash
git status
git add index.html README.md CHANGELOG.md
git commit -m "Add Song DNA analysis and poster studio"
git push
```

If your repository already has a remote configured, `git push` sends the commit to that remote. Check `git remote -v` before pushing if you're unsure which repository is connected.

## Credits

Pulse uses the Web Audio API and Canvas 2D. Music search is powered by the Audius API. Artist-inspired palettes are personal color impressions, not official brand colors.
