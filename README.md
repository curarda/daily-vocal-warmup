# Daily Vocal Warm-up

A small phone app for daily vocal practice. Choose a key and a tempo, listen to a chord, then sing the exercise pattern over it.

**Live app:** https://curarda.github.io/daily-vocal-warmup/

## Who it is for

- Singers doing a daily warm-up routine, with or without a teacher.
- Choir and band vocalists who need a quick, repeatable exercise.

## Why I built it

I sing in a band and wanted a warm-up tool that I could open on my phone in a few seconds, with no setup and no internet needed.

## What it does

- 5 scales: major, natural minor, Phrygian, melodic minor, harmonic minor.
- 11 exercise patterns: arpeggios, scales, long sustained notes and sirens.
- The chord plays at the chosen tempo (2, 4 or 8 beats) and the pattern starts on the next beat.
- Transposition: ascending, descending or up-and-down, in half or whole steps.
- Works offline; installs as a full-screen app.

## Install on iPhone

1. Open the live link in **Safari**.
2. Tap Share → **Add to Home Screen**.
3. Open it from the home screen icon for full-screen mode.

## Run locally

Open `index.html` in a browser, or serve the folder with any static file server.

## Tech

HTML, CSS and JavaScript, Web Audio API (all sounds are synthesized, no audio files), Web App Manifest, service worker.

The original Turkish documentation is in [README.tr.md](README.tr.md).
