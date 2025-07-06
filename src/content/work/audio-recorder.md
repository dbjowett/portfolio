---
title: Audio Recorder
publishDate: 2025-07-06 00:00:00
img: /assets/audio-recorder.png
img_alt: Screenshot of a browser-based audio recorder interface with transcript and summary
description: |
  A Next.js audio recorder that runs entirely in the browser. It captures
  microphone input, transcribes the speech, and attempts to summarize it—
  all client-side using browser-native APIs and WebAssembly models.
tags:
  - Frontend
  - Next.js
  - Web API
  - AI
  - IndexedDB
---

**Audio Recorder** is a fully client-side application built with Next.js that explores in-browser audio recording, transcription, and summarization. It uses the Web Audio API to capture voice input and stores all recordings locally using **IndexedDB** for offline persistence.

Once a recording is complete, the app generates a transcript and then a summary using the `@huggingface/transformers` package, specifically leveraging the `pipeline("summarization")` function running entirely in the browser via WebAssembly.

⚠️ **Note:** The transcription and summarization functionalities are **experimental and unstable**. Processing is fully local and may be slow or fail, depending on the device's resources.

🧱 **Tech Stack**

- **Framework:** Next.js
- **Audio:** Web Audio API
- **Storage:** IndexedDB (local database)
- **ML Inference:** `@huggingface/transformers` running in-browser (WASM)

🚀 **Features**

- Record audio directly in the browser using Web Audio API
- Store recordings locally in IndexedDB
- Generate transcripts from audio (experimental)
- Summarize transcripts using Hugging Face Transformers (unstable, no API calls)
- Fully private: no server, no network requests, all data stays on-device
