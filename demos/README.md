# Demo Samples

All samples were generated on 22 March 2025 using the short Hebrew test text from `sample-text-short.md`.

## ElevenLabs

- **Generated:** 22 Mar 2025
- **Model:** `eleven_v3`
- **Language:** `he` (Hebrew) — must be set explicitly or output is unintelligible
- **API endpoint:** `POST /v1/text-to-speech/{voice_id}`
- **Voice settings:** stability 0.5, similarity_boost 0.75
- **Note:** Multilingual v2 (`eleven_multilingual_v2`) produces poor/unintelligible Hebrew output. v3 with `language_code: "he"` is required for usable results. Library voices require a paid plan for API access.

| File | Voice | Gender |
|------|-------|--------|
| `elevenlabs/rachel-v3-he.mp3` | Rachel | Female |
| `elevenlabs/adam-v3-he.mp3` | Adam | Male |
| `elevenlabs/bella-v3-he.mp3` | Bella | Female |

## Google Gemini

- **Generated:** 22 Mar 2025
- **Model:** Gemini 2.5 Flash Preview TTS
- **Interface:** Google AI Studio
- **Voices:** Puck, Zephyr

| File | Voice |
|------|-------|
| `gemini/puck.wav` | Puck |
| `gemini/zephyr.wav` | Zephyr |

## Resemble AI

- **Generated:** 22 Mar 2025
- **Stock voice engine:** Chatterbox (via Resemble AI web interface)
- **Custom voice engine:** Chatterbox Multilingual (via Replicate API, `language: "he"`)
- **Stock voice:** Avigail (Hebrew-language preset)
- **Custom voices:** Tested with cloned voices using Chatterbox Multilingual on Replicate with Hebrew language parameter. Results sounded generic and not noticeably customised — the voice cloning did not carry through well to Hebrew output.

| File | Voice | Type | Notes |
|------|-------|------|-------|
| `resemble/avigail.wav` | Avigail | Stock (Chatterbox) | Hebrew preset voice via Resemble web UI |
| `resemble/custom-voices/chatterbox/herman.wav` | Herman | Custom clone (Chatterbox Multilingual) | Via Replicate API with `language: "he"`; output sounded generic, not like the source voice |

## Voice Clone Source Audio

English voice samples for testing voice cloning are in `/voice-clone-samples/` at the repo root.

| File | Voice |
|------|-------|
| `corn-1min.mp3` | Corn |
| `daniel-1min.mp3` | Daniel |
| `herman-1min.mp3` | Herman |
