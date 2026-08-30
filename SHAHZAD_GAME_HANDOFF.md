# SHAHZAD GAME HANDOFF
Last updated: 2026-08-30

## Project
Unreal Engine 5.8 — Game set in dark 1980s London night.
Level: **LvL_London** on T7B drive (`/Volumes/T7B/`)

## Security Rules (IMMUTABLE)
- ❌ NEVER Arabic script on any weapon, armour, or surface
- ❌ NEVER Islamic calligraphy — this is pre-Islamic Persia
- ✅ Script on surfaces = Ancient Old Persian cuneiform (خط میخی) OR Avestan Zoroastrian script ONLY

## Completed ✅
- **Fog**: Dark night atmosphere, exponential height fog
- **Rain Audio**: freesound.org WAV imported → `/Game/LvL_London/Audio/Rain_London` → looping AmbientSound actor `Rain_Ambient`, volume 3.0
- **Rain Visual**: Niagara system `NS_Rain_London` — Fountain template, Cone Axis Z=-1, Gravity Z=-2000, Spawn Rate 5000, Sphere Radius 2000. Actor `Rain_Niagara` at Z=3000, scale 10,10,1
- **Cuneiform Texture**: `T_Cuneiform` imported — real Old Persian Unicode (U+103A0–U+103DF), gold (255,210,60), NotoSansOldPersian font
- **Cuneiform Material**: `M_Cuneiform` — Domain: Deferred Decal, Blend: Translucent, T_Cuneiform → RGB→Emissive, A→Opacity
- **Cuneiform Decals**: 6 DecalActors (Cuneiform_0 to _5) placed on building walls

## In Progress 🔄
- **Cuneiform visibility**: Decals placed but position may be off — `replace_decals3.py` ready on T7B, uses bounding boxes for precise wall placement
  - Run: `py /Volumes/T7B/replace_decals3.py`

## Pending ⏳
- Confirm cuneiform visible on walls after replace_decals3.py
- Remove amber marker lights (MARKER_ actors) once confirmed
- Voice line replacement: iPhone → Logic Pro (reverb, delay, pitch) → WAV → import UE5
- Climax sound: same iPhone → Logic Pro path
- WBP_SimorghDialogue — dialogue UI content

## Key Scripts on T7B
| Script | Purpose |
|--------|---------|
| `replace_decals3.py` | Reposition decals using building bounding boxes |
| `fix_cuneiform.py` | Original decal placement |
| `mark_cuneiform.py` | Amber marker lights (debug only) |
| `place_rain2.py` | Place Niagara rain actor |
| `london_rain.py` | Import rain WAV + AmbientSound |

## UE5 Python Rules
- Run scripts via Output Log Cmd: `py /Volumes/T7B/scriptname.py`
- UE5 caches scripts — use new filename if changes don't apply
- device_bash CANNOT write to /Volumes/T7B — use Write→SendUserFile→drag to T7B

## Asset Paths
- Rain audio: `/Game/LvL_London/Audio/Rain_London`
- Cuneiform texture: `/Game/LvL_London/Materials/T_Cuneiform`
- Cuneiform material: `/Game/LvL_London/Materials/M_Cuneiform`
- Niagara rain: `/Game/LvL_London/NS_Rain_London`
