# SHAHZAD GAME HANDOFF
Last updated: 2026-08-31

## Project: LvL_London — UE5.8

## Security Rules (IMMUTABLE)
- ❌ NEVER Arabic script on any weapon, armour, or surface
- ❌ NEVER Islamic calligraphy — pre-Islamic Persia
- ✅ Script = Ancient Old Persian cuneiform OR Avestan Zoroastrian ONLY

## Claude Rules (IMMUTABLE)
- Every 10 min: deliver updated handoff MD automatically
- All commands: copyable code block — never inline
- Terminal commands → Terminal. UE5 commands → UE5 Output Log Cmd. Never mix.
- Never ask Shaz to repeat context
- After compaction: fetch handoff from GitHub BEFORE any work
- Files to T7B: device_bash via $HOME/mnt/T7B/
- GitHub: Terminal commands only — Shaz runs them

## Features Status
- ✅ #8 Cuneiform proximity glow — 16 CuneiformLight PointLights (gold, 4000 intensity, r=250)
- ✅ #7 Slow-mo kill + feather — NS_FeatherDrop + BP_SlowMoKill
- ✅ #6 Weather reacts to danger — DangerZone_Trigger + BP_WeatherDanger
- ✅ #5 Heartbeat tabla pulse — BP_TablaHeartthreat (distance-driven loop)
- ✅ #4 Spatial/quadraphonic audio — SA_London_Spatial + Rain_NE/NW/SE/SW actors
- 🔄 #3 Villain appears in LvL_London — IN PROGRESS (see below)
- ⏳ #2 Ahura Mazda's voice
- ⏳ #1 Portal opening sequence (hardest)

## Feature #3 — Current State (INTERRUPTED)
- BP_VillainGhost created at /Game/LvL_London/Characters/BP_VillainGhost
- M_Villain_Shadow created at /Game/LvL_London/Characters/M_Villain_Shadow
- 3x Villain_Ghost actors in LvL_London (NEED TO DELETE 2 DUPLICATES — keep only 1)
  - 1x BP_VillainGhost type (from villain_setup.py)
  - 2x SkeletalMeshActor type (from villain_place.py + villain_place2.py)
  - KEEP: the SkeletalMeshActor at Location (3000, 0, 0) with SKM_Manny_Simple mesh
  - DELETE: the other 2
- Actor Hidden In Game = TRUE on villain ✅ (correct — hidden at game start)
- Level Blueprint: BeginPlay → Delay(10s) → Set Actor Hidden In Game (Hidden=FALSE) wired ✅
- MISSING: Target connection on Set Actor Hidden In Game — needs direct reference to Villain_Ghost
- TO DO NEXT SESSION:
  1. Run villain_cleanup.py to delete duplicate Villain_Ghost actors
  2. In viewport, click Villain_Ghost in Outliner (keep selected)
  3. Toolbar → Blueprints → Open Level Blueprint
  4. Right-click in graph → "Create a Reference to Villain_Ghost" 
  5. Connect blue dot from reference → Target on Set Actor Hidden In Game
  6. Compile → Done for "appear" logic

## Scripts on T7B
- `/Volumes/T7B/villain_setup.py` — created BP_VillainGhost + M_Villain_Shadow
- `/Volumes/T7B/villain_place.py` — first attempt (failed: wrong property name)
- `/Volumes/T7B/villain_place2.py` — placed SkeletalMeshActor with SKM_Manny_Simple ✅
- `/Volumes/T7B/villain_cleanup.py` — NEEDS TO BE WRITTEN (delete duplicate Villain_Ghost actors)

## Pending / Blocked
- Add real tabla WAV to BP_TablaHeartthreat → BLOCKED until 12V/2A adapter arrives
- Voice line recording (iPhone → Logic Pro → WAV) → BLOCKED until adapter
- Climax sound recording → BLOCKED until adapter
- WBP_SimorghDialogue — dialogue UI content
- GitHub push after Feature #3

## Key Paths
- T7B scripts: /Volumes/T7B/
- Handoff: /Volumes/T7B/SHAHZAD/SHAHZAD_GAME_HANDOFF.md
- GitHub backup: Downloads/eee-journal/SHAHZAD_GAME_HANDOFF.md

## UE5 Notes
- `py` only works in UE5 Output Log Cmd — NOT Terminal
- Script caching: use new filename if changes don't apply
- NEVER press Escape in UE5 — use ■ Stop button or Fn+Shift+F1
- Mac keys: Cmd (not Ctrl), Option (not Alt)
- Villain mesh: /Game/Characters/Mannequins/Meshes/SKM_Manny_Simple
- Rain sound: /Game/LvL_London/Audio/Rain_London
- SA_London_Spatial: /Game/LvL_London/Audio/SA_London_Spatial
