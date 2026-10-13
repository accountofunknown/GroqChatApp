[![Build APK](https://github.com/accountofunknown/GroqChatApp/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/accountofunknown/GroqChatApp/actions/workflows/build.yml)
# Groq Chat (Android)

Kotlin + Jetpack Compose client for the Groq API (OpenAI-compatible, https://api.groq.com/openai/v1).

## Chat
- Streaming replies, multi-chat history (rename, search, delete), edit-and-resend, regenerate, share / copy as Markdown
- Rich Markdown: tables, lists, quotes, links, images (tap to load), inline HTML subset, syntax-coloured code
- Math: real KaTeX typesetting for display formulas (downloaded and bundled by the Gradle build), text fallback otherwise
- Code and formula blocks scroll inside themselves and expand on tap
- Vision (images), speech-to-text (Whisper), text-to-speech (Orpheus), reasoning controls

## Tools
- Function tools: built-in device tools and your own (webhook / static / ask-me), with Auto / Off / Required / Specific modes
- Server tools: web browsing and code execution (gpt-oss), remote MCP servers and Google connectors

## Customisation
- Theme (system / light / dark), pure-black mode, Material You or 8 accent colours, serif / mono fonts, text size
- Compact mode, avatars, usage line, bubble roundness, haptics, Enter-to-send
- Personas (built-in + your own), quick-settings sheet, settings export / import (no secrets included)

## Build
Open in Android Studio and Run, or use the GitHub Actions workflow in `build.yml`.
First launch: paste your key from https://console.groq.com/keys in Settings.
The model you select is always the model that answers (only image requests may switch to the vision model, and the reply says so).
