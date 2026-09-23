# TAGJ — Session Handoff
Last updated: 2026-09-21

---

## TAGJ FA Audiobook — Logic Pro Status

### Current State
- TAGJ_FA_MERGED_01-13.wav imported onto Track 4 in Logic Pro Library.logicx
  - File: ~/Downloads/TAGJ_FA_MERGED_01-13.wav (1h18m33s, 44.1kHz, 24-bit, Mono, 623.5MB)
  - Flex Mode: Off | Smart Tempo: Keep Project Tempo
  - Track 1 deleted (Don't Erase) — Track 4 now independent
- FA editing complete (Shaz confirmed 2026-09-21)
- EN editing complete (Shaz confirmed 2026-09-21)

### Track Layout (Logic Pro Library.logicx)
| Track | Name | Content | Status |
|-------|------|---------|--------|
| 1 | TAGJ_FA_01_0 | DELETED (Don't Erase) | — |
| 2 | TAGJ_FA_01-1 | Empty | Muted |
| 3 | TAGJ_FA_01-1 | Empty | Muted |
| 4 | TAGJ_FA_01_1 | TAGJ_FA_MERGED_01-13_1 | Unmuted |
| 5 | TAGJ_FA_01-1 | Original messy audio | Muted |

---

## Audio Analysis Results (2026-09-21)

| Metric | EN | FA | ACX Target |
|--------|----|----|------------|
| Integrated | -26.4 LUFS | -26.2 LUFS | -18 to -23 dBFS |
| True Peak | +0.13 dBTP CLIPS | +0.22 dBTP CLIPS | -3 dBFS max |
| Noise floor | ~-49 dBFS | ~-49 dBFS | -60 dBFS or lower |

### Logic Pro fixes (both tracks)
1. Gain plugin at TOP of chain: EN +4.5 dB / FA +4.0 dB
2. Noise Gate: Threshold -40 dBFS | Attack 5ms | Release 300ms | Hold 50ms
3. Channel EQ (HP): 120Hz to 160Hz | Slope 24 dB/oct
4. Limiter (end): Output -3.5 dBFS | True Peak ON | Lookahead 1.0ms

### Next Steps
- Apply above settings in both Logic projects
- Export FA chapters (ACX WAV 44.1kHz 16-bit mono -3dBFS peak)
- Export EN chapters (same spec)

---

## TAGJ File Locations
| File | Location |
|------|----------|
| FA EPUB | https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_FA_corrected.epub |
| EN EPUB | https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_EN_corrected.epub |
| Logic FA | ~/Music/Logic/Logic Pro Library.logicx |
| Logic EN | ~/Music/Logic/TAGJ_EN_BABY_0917_MASTER_BACKUP.logicx |
| FA WAV | ~/Downloads/TAGJ_FA_MERGED_01-13.wav |
| EN WAV | ~/Downloads/TAGJ_EN_MERGED_01-09.wav |
| Handoff | https://raw.githubusercontent.com/Shaz010/eee-journal/main/TAGJ_HANDOFF.md |

---

## Session Log
- 2026-09-21: Audio analysis done. Both tracks too quiet (-26 LUFS), peaks clip, noise floor -49 dBFS. Logic Pro fix settings delivered.
- 2026-09-19: FA merged WAV imported Track 4. Track 1 deleted (Don't Erase). FA and EN editing confirmed done.
- Earlier: TAGJ_FA_MERGED_01-13.wav created (chapters 1-13 merged, 1h18m33s)

---

## Key Rules
- Farsi address: شما throughout (NEVER تو) — classical literary Persian
- English is master/source — Farsi is the translation
- New content in .epub = amber gold class `new-v4`
- No ElevenLabs — ACX rejects ElevenLabs audio
- GitHub = Terminal commands only (never ask Shaz to use the GitHub website)
- Never delete files without explicit calm confirmation
