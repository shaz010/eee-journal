# SHAHZAD GAME HANDOFF
Last updated: 2026-08-30

## Project
Unreal Engine 5.8 — Game set in dark 1980s London night.
Level: **LvL_London** on T7B drive (`/Volumes/T7B/`)

## Security Rules (IMMUTABLE)
- ❌ NEVER Arabic script on any weapon, armour, or surface
- ❌ NEVER Islamic calligraphy — this is pre-Islamic Persia
- ✅ Script on surfaces = Ancient Old Persian cuneiform (خط میخی) OR Avestan Zoroastrian script ONLY

## Claude Behaviour Rules (IMMUTABLE)
- **Every 10 minutes**: deliver updated handoff MD automatically — no waiting for session end
- **When Shaz compliments something**: immediately note WHAT worked and HOW, add to handoff
- **All commands**: always in a copyable code block — never inline text
- **Terminal commands go in Terminal. UE5 commands go in UE5 Output Log Cmd field.** Never mix them.
- **Never ask Shaz to repeat context** — read the handoff first every session
- **After compaction**: fetch this handoff from GitHub BEFORE doing any work
- **Files to T7B**: device_bash can write directly to T7B via $HOME/mnt/T7B/
- **GitHub**: give Terminal commands only — Shaz runs them, Claude never pushes
- **Short replies** — eye strain. One action at a time.

## What Worked (copy these approaches)
- **Bounding box decal placement** (`replace_decals3.py`): use `get_actor_bounds()` to find wall surface, place decal at `origin.x ± (extent.x - 5)` embedded in wall — this worked ✅
- **Cuneiform texture**: PIL + NotoSansOldPersian font, gold (255,210,60), 2px glow, transparent background ✅
- **Rain audio**: freesound.org WAV, import task, looping AmbientSound, volume_multiplier 3.0 ✅
- **Niagara rain**: Fountain template, Cone Z=-1, Gravity -2000, Spawn 5000, Radius 2000 ✅
- **Proximity glow** (`cuneiform_glow.py`): PointLight per decal, gold (255,210,60), intensity 4000, attenuation_radius 250 — invisible far, glows up close ✅
- **device_bash → T7B**: write scripts directly via `$HOME/mnt/T7B/` — no need for SendUserFile drag ✅

## Completed ✅
- Fog — dark night atmosphere, exponential height fog
- Rain audio — `Rain_Ambient` actor, volume 3.0
- Rain visual — `Rain_Niagara` actor, NS_Rain_London system
- Cuneiform texture — `T_Cuneiform` imported
- Cuneiform material — `M_Cuneiform`, Deferred Decal, T_Cuneiform→Emissive+Opacity
- Cuneiform on walls — 16 DecalActors (Cuneiform_0 to _15) on all 8 buildings, CONFIRMED VISIBLE ✅
- **Feature #8 — Cuneiform proximity glow** — 16 CuneiformLight PointLights, gold, tight radius ✅

## Pending ⏳ (hardest → easiest)
1. Feature #1: Portal opening sequence (hardest)
2. Feature #2: Ahura Mazda's voice
3. Feature #3: Villain appears in LvL_London
4. Feature #4: Spatial/quadraphonic audio
5. Feature #5: Heartbeat tabla pulse
6. Feature #6: Weather reacts to danger
7. Feature #7: Slow motion kill + feather
- Voice line recording: iPhone → Logic Pro (reverb, delay, pitch) → WAV → replace VoiceLine1/2/3 (BLOCKED until 12V/2A adapter arrives)
- Climax sound recording: same process (BLOCKED until adapter)
- WBP_SimorghDialogue — dialogue UI content
- Save level to Git after each major milestone

## Climax Line (LOCKED)
"Ahura Mazda did not choose you because you are ready. He chose you because it is time."

## Key Scripts on T7B
| Script | Purpose |
|--------|---------|
| `replace_decals3.py` | Bounding-box decal placement — USE THIS ONE |
| `place_rain2.py` | Place Niagara rain actor |
| `london_rain.py` | Import rain WAV + AmbientSound |
| `cuneiform_glow.py` | Proximity glow lights for cuneiform — Feature #8 ✅ |

## UE5 Python
- Output Log Cmd field: `py /Volumes/T7B/scriptname.py`
- UE5 caches scripts — use new filename if changes don't apply
- `py` does NOT work in Mac Terminal — UE5 only
- device_bash CAN write directly to T7B: `$HOME/mnt/T7B/`

## Asset Paths
- Rain audio: `/Game/LvL_London/Audio/Rain_London`
- Cuneiform texture: `/Game/LvL_London/Materials/T_Cuneiform`
- Cuneiform material: `/Game/LvL_London/Materials/M_Cuneiform`
- Niagara rain: `/Game/LvL_London/NS_Rain_London`

## Building Positions (confirmed)
- L side (X≈+655): Building_L1(Y=700,Z=780), L2(Y=200,Z=650), L3(Y=-300,Z=910), L4(Y=-800,Z=715)
- R side (X≈-655): Building_R1(Y=700,Z=845), R2(Y=200,Z=585), R3(Y=-300,Z=975), R4(Y=-800,Z=650)
