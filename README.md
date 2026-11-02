# Laptop-Search-1126

Laptop search, November 2026: ideal requirements for replacing a ThinkPad E15, then market research and a budget number.

## Voice notes

| File | What |
|---|---|
| `voice-notes/2026-11-02_laptop.mp3` | Source recording (17m 32s), 2026-11-02 |
| `voice-notes/2026-11-02_laptop.raw.md` | Raw transcript, verbatim as the model returned it |
| `voice-notes/2026-11-02_laptop.cleaned.md` | Fillers and false starts removed, nothing else changed |
| `voice-notes/2026-11-02_laptop.dev-prompt.md` | Brief for an agent doing the research |
| `voice-notes/2026-11-02_laptop.transcript.json` | Run metadata: backend, model, duration, cost |

### How the transcripts were made (2026-11-02)

1. Preprocess: `Transcription-Pipeline/scripts/preprocess.py --preset gemini` (mono Opus 24 kbps, conservative VAD). 8.4 MB to 3.2 MB; VAD trimmed 0.01 s because the recording has no long pauses.
2. Transcribe: `Transcription-Router-Plugin/scripts/tr.py transcribe --model lite --rewrite-model google/gemini-3.5-flash-lite --outputs set`, via OpenRouter.
3. Cost: $0.017 transcription + $0.013 rewrites = $0.031 for 17.5 minutes. The earlier default (`google/gemini-3.8-flash` for both steps) cost $0.075 for a 4.4-minute note.
