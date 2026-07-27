# Tamil Live Transcribe

A free webpage for live Tamil speech-to-text with optional AI spelling/grammar correction. Just open it in a browser — nothing to install.

## How it works

- **Live transcription** uses your browser's built-in speech recognition (Web Speech API), set to Tamil (`ta-IN`). This is free and needs no API key — it just needs an internet connection while you're speaking.
- **AI Correct** button cleans up spelling, word breaks, and punctuation using Google's free Gemini API. You provide your own free API key (see below) — it's stored only in your browser and sent directly to Google, nowhere else.
- **Copy** and **Download .txt** buttons let you grab the transcript any time, mid-session or after.
- Your transcript and settings are saved in the browser automatically (so a refresh won't lose your text).

## Browser requirement

Live speech recognition currently only works reliably in **Chrome** or **Edge** (desktop or Android). Safari and Firefox don't support the underlying API well yet. Typing/pasting, AI correction, copy, and download still work everywhere.

## How to open it

**Simplest — just double-click `index.html`.** It'll open in your default browser. If it's not Chrome or Edge, right-click the file → "Open with" → choose Chrome or Edge.

That's it for everyday use on one computer.

**If you want the same link on your phone too** (optional), you need it hosted somewhere, since phones can't open a file straight off your laptop. Any free static host works, e.g.:

- Go to https://app.netlify.com/drop and drag this folder onto the page — you'll instantly get a live `https://...netlify.app` link you can open on any device.

No account or install needed either way.

## Get a free Gemini API key (for AI Correct)

1. Go to https://aistudio.google.com/apikey
2. Sign in with a Google account (no credit card needed).
3. Create an API key and copy it.
4. In the app, tap the gear icon (top right) → paste the key → Save.

The free tier is limited to a modest number of requests per day, which is plenty for personal transcription use.

## Files

```
index.html      the whole app — open this file directly in Chrome or Edge
README.md       this file
```

## Notes & limits

- Speech recognition sends short audio snippets to your browser vendor's speech service in the background (this is how Web Speech API works everywhere, not specific to this app) — it needs internet.
- AI correction quality depends on Gemini's free-tier model and can occasionally over-correct proper nouns; you can always edit the transcript directly (it's editable text) before copying or downloading.
- If Chrome stops listening after a long silence, the app automatically restarts it — you shouldn't need to tap the mic again mid-session.
