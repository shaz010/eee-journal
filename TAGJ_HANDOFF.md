# TAGJ Book Handoff Summary

**Last updated: 2026-09-10 (session 3)**

## Core Mission
Maintain **Think and Grow Joy** (فکر کن و شادی بیافرین) as a bilingual EPUB project with strict non-negotiable rules: never improvise, never push to GitHub directly, never alter existing content without explicit instruction, and always warn before irreversible changes.

## Key Operational Rules
- **English is master; Farsi is translation.** All corrections must verify the English original first.
- **Address reader as شما (formal) throughout Farsi.** Never use تو (colloquial).
- **One clean pass only.** Batch all changes, deliver the file, done.
- **New content tagged `new-v4` with amber styling** for version tracking.

## Current File Status
- **Farsi EPUB:** `TAGJ_v4_FA_corrected.epub` (9 chapters + prologue + closing, all شما-converted)
- **English EPUB:** `TAGJ_v4_EN_corrected.epub` (parallel updates complete)
- **Master .docx:** `TAGJ_v4_Jul2026.docx` (editable in session workspace)
- **GitHub:** Shaz uploads manually via website only

## Critical Farsi Terminology
| Term | Translation |
|------|-------------|
| Momentum | تکانه (never شتاب) |
| God/Divine Source | پروردگار (when spiritual) |
| Law of Attraction | قانون جذب |
| Consciousness | آگاهی |

## Audiobook Status
- **English (pre_WR_EN):** 14 MP3s complete, voice "Gem" at 0.78 speed
- **Farsi (pre_WR_FA):** 11 MP3s complete, FaridNeural Tehran accent
- Both are AI placeholders until Shaz records in Logic Pro

## Next Actions (TAGJ)
1. Record own voice in Logic Pro (EN + FA)
2. Upload latest EPUBs to GitHub
3. Begin promotion (WhatsApp/Telegram first)
4. Optional: ElevenLabs voice cloning for scale regeneration

---

## 🎮 UE5 — LvL_Persia Feature #8 (Active)

**Project:** Your Salon Pro / MGM Studio (Unreal Engine 5)
**Task:** Add OnActorBeginOverlap + OnActorEndOverlap event nodes for CuneiformTrigger_1–7 in LvL_Persia Level Blueprint, wire to GlowOn (Begin) / GlowOff (End) macros, compile, Cmd+S save.

### Progress as of 2026-09-10

| Trigger | BeginOverlap | EndOverlap |
|---------|-------------|------------|
| CT_1 | ✅ Done (prev session) | ✅ Done (prev session) |
| CT_2 | ✅ Done (this session) | ✅ Done (this session) |
| CT_3 | ✅ Done (this session) | ✅ Done (this session) |
| CT_4 | ✅ Done (this session) | ✅ Done (this session) |
| CT_5 | ✅ Done (this session) | ✅ Done (this session) |
| CT_6 | ✅ Done (session 2) | ✅ Done (session 3) |
| CT_7 | ✅ Done (session 2) | ✅ Done (session 2) |

**✅ Feature #8 COMPLETE** — All 14 event nodes placed AND wired (7 BeginOverlap → GlowOn, 7 EndOverlap → GlowOff). Compiled ("Good to go"). Saved ("All Saved"). 2026-09-10 session 3.

### Critical UE5 Rules (NEVER ask Shaz to repeat)

- **ALWAYS minimize Window 335** (main UE5 3D viewport "SHAHZAD - Unreal Editor") BEFORE Blueprint wiring work — reduces Mac heat
- **Window 999** (LvL_Persia Level Blueprint) = IS_MAIN, keep open
- **Python REPL tab:** x≈530, y≈825 on screen. DO NOT click x≈120 (Content Drawer — breaks UE5 focus)
- **Output Log:** x≈162; Python REPL tab: x≈250; REPL input: x≈530
- **0.5-scale screenshot coords:** ALL visual positions must be ×2 to get real screen coords. Zoom region coords ARE already full screen.
- **Right-click on empty canvas:** canvas is at Zoom -12 (very zoomed out). Nodes are scattered. If right-click gives "Delete/Cut/Copy/Duplicate" menu = hit a node → Escape and try different position.
- **Search bar position pattern:** appears ~34px below and ~140px right of right-click position
- **Enter key** works to confirm highlighted menu item (preferred over clicking when item is blue-highlighted)
- **Actor selection:** `get_actor_label()` NOT `get_name()` to match "CuneiformTrigger_N" labels
- **CT actors:** TriggerSphere class — no Events tab in Details panel — must use canvas right-click method

### Other Pending Features
- Feature #9: niagara_torches.py → flames on BP_TorchFlicker
- LvL_Persepolis: Fix 7 BP_ApadanaColumns Scale Z: 1 → 20
- Farsi Font: Import Vazirmatn/IRANSans .ttf for WBP_LanguageToggle
- Portal_Faravahar Texture — need image from Shaz
- WAV Import — blocked (Apogee adapter)

---

*GitHub: github.com/Shaz010/eee-journal | Repo: eee-journal | Branch: main*
