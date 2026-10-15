[![Build APK](https://github.com/accountofunknown/GroqChatApp/actions/workflows/build.yml/badge.svg?branch=main)](https://github.com/accountofunknown/GroqChatApp/actions/workflows/build.yml)
# Groq Chat (Android)

Kotlin + Jetpack Compose client for the Groq API (OpenAI-compatible, https://api.groq.com/openai/v1).

## Chat
- Streaming replies, multi-chat history (pin, rename, delete, automatic titles), edit-and-resend, regenerate, share / copy as Markdown
- Search: across all chats (titles and message text) from the drawer, and "Find in chat" with next/previous match
- Rich Markdown: tables, lists, quotes, links, images (tap to load), inline HTML subset, syntax-coloured code
- Math: real KaTeX typesetting for display formulas (downloaded and bundled by the Gradle build), text fallback otherwise
- Code and formula blocks scroll inside themselves and expand on tap
- Vision (images), speech-to-text (Whisper), text-to-speech (Orpheus), reasoning controls

## Chat features
- Per-chat settings (model, persona, creativity, reasoning) with "use as default" / reset
- Regenerate keeps earlier versions you can flip between; "answer again with another model" compares models
- Context meter, and summarise-older-messages (manual or automatic); summarised messages stay visible but aren't sent
- Attach photos, camera shots, PDFs, Word and text files; prompt templates with {{variables}}
- Hands-free voice mode (listen, answer, read aloud); read-aloud starts with the first sentence
- Usage dashboard: tokens, speed and remaining rate limit per model

## Tools
- Function tools: built-in device tools and your own (webhook / static / ask-me), with Auto / Off / Required / Specific modes
- Server tools: web browsing and code execution (gpt-oss), remote MCP servers and Google connectors

## Customisation
- Theme (system / light / dark), pure-black mode, Material You or 8 accent colours, serif / mono fonts, text size
- Compact mode, avatars, usage line, bubble roundness, haptics, Enter-to-send
- Personas (built-in + your own), quick-settings sheet, settings export / import (no secrets included)

## Privacy and storage
- Chats live in an SQLite database; titles, folders, tags and every message are AES-256-GCM encrypted, images are separate encrypted files
- The encryption key is protected by the Android Keystore; API keys, MCP servers and custom tools are stored encrypted too
- Optional app lock (fingerprint / face / device PIN) with a grace period, and "hide in recent apps" (blocks screenshots)
- Folders, tags, archive, multi-select, and delete with undo; old chats are migrated automatically on first start

## Build
Open in Android Studio and Run, or use the GitHub Actions workflow in `build.yml`.
First launch: paste your key from https://console.groq.com/keys in Settings.
The model you select is always the model that answers (only image requests may switch to the vision model, and the reply says so).
