# TAGJ Book Handoff Document — Summary

**Last updated: 2026-09-10**

This is Shaz Mirshahi's operational guide for managing the bilingual book *Think and Grow Joy* (Persian: *فکر کن و شادی بیافرین*) across EPUB, Word, and audiobook formats.

## Core Workflow Rules
- **No improvisation:** Add only exact content Shaz provides
- **No GitHub pushes:** Shaz uploads files manually
- **No alterations to existing content** without explicit instruction
- **Single-pass changes** with irreversible-action warnings
- English is the authoritative source; Farsi follows as translation

## Key Files
- **Farsi EPUB:** `TAGJ_v4_FA_corrected.epub`
- **English EPUB:** `TAGJ_v4_EN_corrected.epub`
- **Word master:** `TAGJ_v4_Jul2026.docx`
- **GitHub repo:** `Shaz010/eee-journal` (manual uploads only)

## Critical Farsi Standards
- **Address:** شما (formal) throughout—never تو
- **Terminology:** تکانه (momentum), پروردگار (God/divine source), قانون جذب (law of attraction)
- **Status:** Global شما replacement completed 2026-08-20 across all 9 chapters plus prologue

## Audiobook Status
- **English:** 14 MP3s complete (pre_WR_ prefix = AI placeholder)
- **Persian:** 11 MP3s complete using edge-tts
- **Persian M4B (Mac):** `TAGJ_FA_Books2.m4b` built 2026-09-10 — plays as ONE unified audiobook in Mac Books ✅
  - Built without faststart (mdat before moov — safe binary structure)
  - Chapter text track stripped (`-map 0:a` only); `chpl` atom injected from original
  - stik=2, title/album set to تفکر و شادی بزرگ via mutagen
  - 47MB, 3737s, 24kHz Mono AAC
- **iOS Books:** Transfer attempted 2026-09-10 — NOT YET RESOLVED ⚠️
  - Finder Audiobooks tab shows dangerous "erase and sync" warning — session cancelled
  - Safe transfer path still needed (Finder Books tab not appearing even with iCloud Books off)
  - Original `TAGJ_FA_Audiobook.m4b` has chapter text track → shows as individual items on iOS
- **Next step:** Record in Shaz's own voice via Logic Pro; optionally clone via ElevenLabs for scale
- **ElevenLabs API key:** stored in previous session notes — do not paste in chat

## Farsi Self-Editing Workflow (NEW — 2026-09-10)
Shaz requested ability to edit Farsi content himself without going through Claude for every correction:
- **Editable Word doc:** `TAGJ_FA_editable.docx` — delivered via Cowork (file_uuid: 834d57b2-86c0-4aba-bbf7-6ebf6c885eb8)
- **Plain text version:** `TAGJ_FA_editable.txt` — delivered via Cowork (file_uuid: 1da15069-8f27-46b3-8f3e-a2693af31e15)
- **Workflow:** Shaz edits Word doc → returns to Claude → Claude rebuilds EPUB with corrections
- **Dark mode note:** Pages stays white (paper-white design, no dark document mode). Word has true dark mode via View → Dark Mode (paid subscription required). Notes app is read-only for .docx.

## Pending Tasks (priority order)
1. **iOS Books chapter navigation** — Safe transfer path for TAGJ_FA_Books2.m4b to iOS Books with chapters still needed. Do NOT use Finder Audiobooks tab (dangerous erase warning).
2. **Farsi EPUB corrections** — Shaz has editable .docx; will return with corrections for EPUB rebuild
3. **ACX account** — Withdraw submission before account termination warning escalates
4. **Cover art** — Missing for both EPUBs (flagged across multiple sessions)
5. **WR recordings** — Shaz's own voice in Logic Pro
6. **Promotion** — WhatsApp/Telegram broadcast

## Corrections Log
| Date | File | What Changed |
|------|------|--------------|
| 2026-08-20 | FA EPUB | Global شما replacement (all 9 chapters + prologue) |
| 2026-09-10 | M4B (Persian) | Built TAGJ_FA_Books2.m4b — unified audiobook, no chapter text track, chpl atom retained |
| 2026-09-10 | Editable docs | Exported FA EPUB to .docx and .txt for Shaz's self-editing |

## Version Management
Update `dcterms:modified` in `content.opf` each repacking cycle. Current date format: `2026-08-20T00:00:00Z`.
