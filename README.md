# ElevenStudio Android (Kotlin + Jetpack Compose)

A native Android application modeled after the official [ElevenLabs Android App (`io.elevenlabs.coreapp`)](https://play.google.com/store/apps/details?id=io.elevenlabs.coreapp&hl=en) and integrated with the [ElevenLabs v1 REST API (`https://api.elevenlabs.io`)](https://elevenlabs.io/docs/api-reference/text-to-speech/convert).

## Included Features
1. **Text-to-Speech (TTS) Studio**: Supports [Eleven v4 (`eleven_v4`), Eleven v4 Turbo (`eleven_v4_turbo`), Eleven v3 (`eleven_v3`), Eleven Multilingual v2 (`eleven_multilingual_v2`), and Eleven Flash v2.5 (`eleven_flash_v2_5`)](https://elevenlabs.io/docs/overview/capabilities/text-to-speech) with expressive audio tags (`[whispering]`, `[excited]`, `[warmly]`), Stability, Similarity Boost, and Style Exaggeration sliders.
2. **Voice Library**: Browse, search, preview, and favorite voices (including canonical voice IDs such as `JBFqnCBsd6RMkjVDRZzb`).
3. **Voice Lab**:
   - **Instant Voice Cloning (IVC)** via `POST /v1/voices/add`
   - **Voice Changer (Speech-to-Speech)** via [`POST /v1/speech-to-speech/{voice_id}`](https://elevenlabs.io/docs/api-reference/speech-to-speech/convert)
   - **Voice Isolator** via `POST /v1/audio-isolation`
4. **ElevenReader Mode**: Sentence-synced document and article narration with adjustable speed and Android `TextToSpeech` offline fallback.

## How to Open & Run in Android Studio
1. Extract `elevenlabs_android_project.zip` and open the folder in **Android Studio Ladybug (2024.2.1)+**.
2. Add your ElevenLabs API key (`xi-api-key`) in the in-app Settings dialog or `local.properties` (`ELEVENLABS_API_KEY=your_key`). Without an API key, the app automatically falls back to Android's native `android.speech.tts.TextToSpeech` engine so all features remain testable offline.
