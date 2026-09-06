# SHAHZAD GAME — HANDOFF
Last updated: 2026-09-06

---

## IMMUTABLE SECURITY RULES
- ❌ NEVER Arabic script on any weapon, armour, or surface
- ❌ NEVER Islamic calligraphy — this is pre-Islamic Persia
- ✅ Script on surfaces = Ancient Old Persian cuneiform (خط میخی) OR Avestan Zoroastrian script ONLY

## IMMUTABLE CLAUDE BEHAVIOUR RULES
- Every 10 min: deliver updated handoff MD automatically
- All commands: always in a copyable code block — never inline text
- Terminal commands go in Terminal. UE5 commands go in UE5 Output Log Cmd. Never mix.
- Never ask Shaz to repeat context — read the handoff first every session
- After compaction: fetch this handoff from GitHub BEFORE doing any work
- Files to T7B: device_bash writes via $HOME/mnt/T7B/
- Handoff updates: ALWAYS write to ALL 3 — T7B/SHAHZAD/, T7B/Claude outputs/, AND give git Terminal commands
- GitHub: give Terminal commands only — Shaz runs them, Claude never pushes
- Short replies — eye strain. One action at a time.
- Blueprint instructions: ALWAYS give the FULL step in every message — never assume Shaz remembers a previous step. If he asks a question mid-step, restate the complete instruction with the question answered. Never make him scroll up. Every step names: which node, which side (left/right), which pin label.

---

## COMPLETED THIS SESSION

### Battle Scene Animation ✅ COMPLETE (2026-09-04)
- Script: /Volumes/T7B/battle_scene.py
- Run: py /Volumes/T7B/battle_scene.py
- 8-phase sequence (~12s total):
  - Phase 0: Hide all, Shahzad revealed on hero side (Y=-800)
  - Phase 1 (2s): Ahriman emerges (Y=1200)
  - Phase 2 (1.5s): AhrimanLight ignites
  - Phase 3 (2s): ShahzadWeapon billboards appear
  - Phase 4 (1.5s): Shahzad charges (Y=-200)
  - Phase 5 (1s): CLASH — AhrimanAttack flare, Ahriman moves to Y=800
  - Phase 6 (1.5s): AhrimanAttack hidden, Ahriman recoils to Y=1600
  - Phase 7 (1s): Victory — weapons fan out, AhrimanLight off
- All 8 phases confirmed COMPLETE in Output Log ✅

### Actor Tags Applied ✅ COMPLETE (2026-09-04)
- Script: /Volumes/T7B/tag_battle_actors.py
- Tagged: Persia_Shahzad_Hero → Shahzad
- Tagged: Persia_Shahzad_v1 → Shahzad
- Tagged: Persia_Ahriman_Full → Ahriman
- Tagged: Persia_AhrimanLight (untagged duplicate) → AhrimanLight
- Tagged: Enemy_1/2/3 → Enemy
- Level saved to LvL_Persia ✅

### Language Toggle Widget ✅ COMPLETE (2026-09-04)
- Asset: /Game/UI/WBP_LanguageToggle
- Gold button (amber R=1.0 G=0.72 B=0.0) with text "EN | فا"
- Compiled and saved
- ⚠️ Farsi glyph warning: UE5 default font lacks Arabic/Persian chars
  - U+641 (ف) and U+627 (ا) show as fallback boxes in-engine
  - Fix later: import a Farsi-compatible .ttf font asset

### Ahriman Attack Sequence ✅ COMPLETE (2026-09-04)
- Script: /Volumes/T7B/ahriman_attack_sequence.py
- Sequence: reveal Ahriman+light → 3s → attack flare → 1.5s → Ahriman lunges Y=800

### Shahzad Weapon Billboards ✅ COMPLETE (2026-09-04)
- Shahzad_Weapon_Pistol: (200, -600, 250) tag=ShahzadWeapon
- Shahzad_Weapon_Swords: (200, 600, 250) tag=ShahzadWeapon
- Shahzad_Weapon_SwordsCrossed: (300, 0, 500) tag=ShahzadWeapon

### LvL_Persia — Ahriman Confrontation ✅ COMPLETE (2026-09-04)
- Persia_BattleBillboard placed (0, 3000, 500), battle scene backdrop
- Persia_Ahriman billboard, AhrimanLight (red PointLight) — hidden at start
- Level Blueprint: PersiaArrival Completed → Delay(5s) → reveal Ahriman+light + CameraShake

### LvL_London — Feature A: Portal Shockwave ✅ COMPLETE
### LvL_London — Feature C: Fright/Fascination/Exhilaration ✅ COMPLETE
### Git LFS ✅ COMPLETE

---

## PENDING — RESUME HERE NEXT SESSION

### Farsi Font for WBP_LanguageToggle — NEEDED
- Import a Farsi-compatible .ttf (e.g. Vazirmatn or IRANSans) as UE5 Font asset
- Apply to TextBlock_0 in WBP_LanguageToggle
- Then Farsi glyphs will render properly in-engine

### Language Toggle Logic ✅ COMPLETE (2026-09-06)
- FlipFlop wiring done via Python REPL (probe28.py)
- A branch → SetText25 → "EN | فا"
- B branch → SetText26 → "فا | EN"
- TextBlock_0 wired to both, orphan nodes removed, compiled and saved

### Portal_Persia Faravahar Texture — BLOCKED
- Need Faravahar image from Shaz

### WAV Import — BLOCKED
- Ahura Mazda voice + Tabla WAV: blocked on Apogee adapter

### Army Battle Scene — Enhancement possible
- Persia_BattleBillboard is static — particle soldiers / animated opacity possible

---

## ALL ACTOR TAGS IN LvL_Persia (confirmed 2026-09-04)
| Tag | Actors |
|-----|--------|
| Shahzad | Persia_Shahzad_Hero, Persia_Shahzad_v1 |
| Ahriman | Persia_Ahriman, Persia_Ahriman_Full |
| AhrimanLight | Persia_AhrimanLight (×2) |
| AhrimanAttack | Persia_AhrimanAttackFlare |
| ShahzadWeapon | Shahzad_Weapon_Pistol, Shahzad_Weapon_Swords, Shahzad_Weapon_SwordsCrossed |
| Enemy | Enemy_1, Enemy_2, Enemy_3 |
| PersiaColumn | Persia_Column_1–4 |
| PersiaTablet | Persia_CuneiformTablet_1–4, Persia_TabletGlow_1–4 |
| PersiaArrival | Persia_ArrivalTrigger, Persia_ArrivalBurst |

---

## GAME TIMELINE — LvL_Persia
- 0s: BeginPlay → golden scene, torches, columns
- 0.5s: PersiaArrival actors visible
- 5s after arrival: Ahriman billboard + red AhrimanLight + camera shake
- Manual: run battle_scene.py for full 8-phase battle sequence

## GAME TIMELINE — LvL_London
- 2s: Ahura Mazda voice (WAV pending)
- 6s: Cuneiform lights glow
- 10s: Villain_Ghost + DangerStrobe
- 18s: Portal + Camera Shake + Slow Motion → GoldSurge

---

## FILE LOCATIONS
| File | Path |
|------|------|
| Game Repo | https://github.com/shaz010/mgm-studio |
| Handoff | T7B/SHAHZAD/SHAHZAD_GAME_HANDOFF.md |
| Battle script | /Volumes/T7B/battle_scene.py |
| Tag script | /Volumes/T7B/tag_battle_actors.py |
| Ahriman script | /Volumes/T7B/ahriman_attack_sequence.py |
| Weapons script | /Volumes/T7B/place_weapons.py |

## KEY FACTS
- GitHub: github.com/shaz010 (repo: mgm-studio)
- T7B mount in device_bash: $HOME/mnt/T7B/
- UE5 Python: run via Output Log Cmd as `py /Volumes/T7B/scriptname.py`
- Farsi address: شما (NEVER تو)
- UE5 crash risk: NEVER call open_editor_for_assets or AssetEditorSubsystem
