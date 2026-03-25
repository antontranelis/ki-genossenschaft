# Was ist möglich mit 8x H100?

8x NVIDIA H100 80GB SXM = 640 GB VRAM, verbunden über NVLink/NVSwitch.

Das ist die Grundausstattung eines gut finanzierten KI-Startups. Kein Spielzeug — produktionsfähige Infrastruktur.

## Inferenz: Welche Modelle laufen

| Modell | VRAM-Bedarf | GPUs | Gleichzeitige Nutzer | Tokens/Sekunde |
|---|---|---|---|---|
| Llama 3 70B (FP16) | ~140 GB | 2 | ~50–100 | ~30–50/Nutzer |
| Llama 3 70B (INT4) | ~40 GB | 1 | ~50–100 | ~40–80/Nutzer |
| Llama 3 405B (INT4) | ~200 GB | 3–4 | ~20–50 | ~15–25/Nutzer |
| Mixtral 8x22B | ~90 GB | 2 | ~50–100 | ~25–40/Nutzer |
| Llama 3 8B (FP16) | ~16 GB | 1 | ~200+ | ~100+/Nutzer |
| Whisper Large (Audio) | ~10 GB | 1 | parallel | Echtzeit+ |
| Stable Diffusion XL | ~8 GB | 1 | parallel | ~5s/Bild |
| Code-Modelle (Qwen 72B) | ~140 GB | 2 | ~50–100 | ~30–50/Nutzer |

## Realistisches Setup: Alle 8 GPUs gleichzeitig

```
GPU 1–2:  Llama 3 70B (FP16) — Haupt-Sprachmodell, beste Qualität
GPU 3:    Llama 3 70B (INT4) — Zweite Instanz für Lastspitzen
GPU 4:    Llama 3 8B — schnelle Aufgaben, Agents, Zusammenfassungen
GPU 5:    Code-Modell (Qwen 32B oder DeepSeek Coder)
GPU 6:    Embedding-Modell + Whisper (Audio-Transkription)
GPU 7:    Stable Diffusion / Bildgenerierung
GPU 8:    Reserve / Burst / Fine-Tuning
```

Bedient locker **500–1000 Mitglieder** im normalen Nutzungsbetrieb.

## Training & Fine-Tuning

| Aufgabe | Machbar? | Details |
|---|---|---|
| LoRA Fine-Tuning 70B | Ja | 1–2 GPUs, paar Stunden |
| Full Fine-Tune 7–13B | Ja | 2–4 GPUs |
| Full Fine-Tune 70B | Ja | Alle 8 GPUs, Tage |
| Training from Scratch <1B | Ja | Gut machbar |
| Training from Scratch 7B | Möglich | Wochen |

## Was Mitglieder konkret bekommen

### Privatpersonen / Communities

- Chat mit Llama 70B / 405B — vergleichbar mit ChatGPT, auf eigener Infrastruktur
- Audio-Transkription (Whisper)
- Bildgenerierung
- Code-Assistenz
- Alles DSGVO-konform, keine Logs

### Startups / Unternehmen

- API-Zugang zu gehosteten Modellen (OpenAI-kompatibel)
- Rohe GPU-Stunden für eigenes Training
- Fine-Tuning-Service auf eigenen Daten
- Dedizierte GPU-Slots bei Bedarf

### Forschung

- Training eigener Modelle
- Zugang zu High-End-Hardware ohne Warteliste
- Reproduzierbare Umgebungen
