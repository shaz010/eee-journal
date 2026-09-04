# SHAHZAD GAME HANDOFF
Last updated: 2026-09-03

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
- ✅ #8 Cuneiform proximity glow — 16 CuneiformLight PointLights
- ✅ #7 Slow-mo kill + feather — NS_FeatherDrop + BP_SlowMoKill
- ✅ #6 Weather reacts to danger — DangerZone_Trigger + BP_WeatherDanger
- ✅ #5 Heartbeat tabla pulse — BP_TablaHeartthreat
- ✅ #4 Spatial/quadraphonic audio — SA_London_Spatial + Rain actors
- ✅ #3 Villain appears — BeginPlay → Delay(10s) → Villain_Ghost unhidden. Green compile.
- 🔄 #2 Ahura Mazda's voice — WIRED (Play Sound 2D at 2s). WAV pending adapter.
- ✅ #1 Portal opening sequence — COMPLETE (see below)

## Feature #1 — Portal Opening Sequence ✅
- 3 actors placed in LvL_London at X=5000, Y=0:
  - Portal_Persia — plane mesh (portal surface), scale 4×6
  - Portal_GoldLight — amber PointLight (255,180,60), intensity 50000, radius 2000
  - Portal_VioletRim — violet PointLight (130,60,255), intensity 20000, radius 3000, at X=4800
- All tagged `PortalActors`
- All hidden at game start
- Level Blueprint: BeginPlay → Delay(2s) → Play Sound 2D (Ahura voice) → Delay(8s) → Get All Actors with Tag (PortalActors) → For Each Loop → Set Actor Hidden In Game (Hidden=false)
- Compiled green ✅
- Visual reference: PERSEPOLIS_APOCALYPSE_LOCKED.jpg + SHAHZAD_FARAVAHAR_POWER_LOCKED.jpg
- Portal aesthetic: gold Faravahar wings of fire between Persepolis columns tearing through London brick

## Scripts on T7B
- `/Volumes/T7B/villain_delete.py` — deleted 2 duplicate Villain_Ghost actors ✅
- `/Volumes/T7B/ahura_voice_setup.py` — created SA_AhuraMazda_Voice + AhuraMazda_Voice actor ✅
- `/Volumes/T7B/ahura_voice_bp.py` — confirmed actor, auto_activate=False ✅
- `/Volumes/T7B/portal_open.py` — spawned 3 portal actors ✅
- `/Volumes/T7B/portal_tag.py` — tagged all 3 with PortalActors tag ✅

## Pending / Blocked
- Feature #2 WAV: import Ahura Mazda voice → assign to Play Sound 2D node. BLOCKED until Apogee adapter arrives (5V 3A, 4mm×1.7mm EIAJ-2 + USB Mini-B to USB-C on order)
- Portal material: Portal_Persia plane needs glowing emissive Faravahar material (next session)
- Tabla WAV: add real tabla WAV to BP_TablaHeartthreat — BLOCKED until adapter
- WBP_SimorghDialogue — dialogue UI content
- Logic sounds: cinematic/legacy packs downloading to T7B via symlink — curation pass needed
- GitHub push: run commands below after any session

## GitHub Push Commands (Terminal)
```
cd ~/Downloads/eee-journal
cp /Volumes/T7B/SHAHZAD/SHAHZAD_GAME_HANDOFF.md .
git add SHAHZAD_GAME_HANDOFF.md
git commit -m "Session 2026-09-03: Feature #1 portal complete"
git push
```

## Key Paths
- T7B scripts: /Volumes/T7B/
- Handoff on T7B: /Volumes/T7B/SHAHZAD/SHAHZAD_GAME_HANDOFF.md
- GitHub handoff: https://raw.githubusercontent.com/Shaz010/eee-journal/main/SHAHZAD_GAME_HANDOFF.md
- FAL assets: /Volumes/T7B/SHAHZAD/06_APPROVED/
- Logic Library: symlink ~/Music/Logic Pro Library.bundle → /Volumes/T7B/Logic_Pro_Library.bundle/

## UE5 Notes
- `py` only works in UE5 Output Log Cmd — NOT Terminal
- NEVER press Escape in UE5 — use ■ Stop or Fn+Shift+F1
- Portal actors at X=5000 face player (player starts near X=0)
- Villain mesh: /Game/Characters/Mannequins/Meshes/SKM_Manny_Simple
- AhuraMazda_Voice actor at X=0,Y=0,Z=0 — auto_activate=False
- Apogee Duet ORIGINAL: 5V 3A, 4mm×1.7mm centre-positive (EIAJ-2), USB Mini-B to Mac
