# 🚗 Yellow Car!

A voice-activated yellow car spotting game, built as a Progressive Web App (PWA). Designed for road trips — install it once and it works fully offline.

**Live app:** https://pretend-maintenance.github.io/yellow-car/

---

## How to play

Yellow Car is a classic road trip game where players shout "Yellow Car!" whenever they spot one. First to a target score wins.

1. Open the app in Chrome on Android
2. Tap **Start Listening**
3. Say **"Yellow Car"** when you spot one — the app will ping and flash yellow
4. Say the player's name (**Daddy** or **Ben**) to award the point
5. Scores, confetti, and a history log update automatically

---

## Features

- 🎤 **Continuous voice recognition** — listens in the background, no button mashing
- 🟡 **Wake word detection** — triggers on "Yellow Car", then listens for the player name
- 🔊 **Audio feedback** — ping on wake word, fanfare on score
- 📳 **Haptic feedback** — vibration on score
- 📋 **History log** — timestamped list of every car spotted with gap timer between sightings
- 👑 **Leading indicator** — crown shown on the current leader
- ✏️ **Editable names** — tap the pencil icon on each scorecard
- 💾 **Names saved** — player names persist across sessions via localStorage
- 📴 **Works offline** — service worker caches everything after first load

---

## Installing as a PWA (Android)

1. Open https://pretend-maintenance.github.io/yellow-car/ in **Chrome**
2. Tap the three-dot menu → **Add to Home Screen**
3. Allow microphone permission when prompted
4. Launch from your home screen — runs fullscreen like a native app

After installation the app works with no internet connection.

---

## Voice recognition tips

- Speak clearly after the yellow flash/ping — you have 5 seconds
- If a name is missed, the status bar shows exactly what was heard
- Short names like **Ben** have an expanded phonetic mishear table to improve accuracy
- Manual **+1** buttons are always available as a fallback

---

## Tech stack

- Vanilla HTML/CSS/JS — no framework, no build step
- Web Speech API (`webkitSpeechRecognition`) for voice
- Web Audio API for sounds
- Service Worker for offline caching
- Hosted on GitHub Pages
