# SHAHZAD Game — Session Handoff
**Date:** 13 August 2026  
**Level:** LvL_Tachara COMPLETE ✅ | LvL_Vault COMPLETE ✅ | LvL_Persepolis — in progress

---

## PLATFORM — NEVER FORGET
- Shaz is on a **Mac** — always use **Cmd** not Ctrl for all keyboard shortcuts
- Save = **Cmd+S** (never Ctrl+S)
- Undo = **Cmd+Z** (never Ctrl+Z)
- Copy = **Cmd+C**, Paste = **Cmd+V**

---

## COMMUNICATION RULES — NEVER BREAK THESE
- Always use the **exact full name** shown on screen for every node, pin, panel, and tab — never shorten or paraphrase
- When describing where to click or drop, name the exact label the user sees on screen
- **ALWAYS highlight negative values in red 🔴 — e.g. -1500 🔴 — Shaz cannot see minus signs without this**
- **Always mention LEFT or RIGHT when describing pins in Blueprint graph**
- **One step at a time — never give multiple instructions at once**
- **NEVER GUESS — if unsure of a value, ask Shaz what is shown on screen**
- **ALWAYS check Scale of original actors BEFORE placing new instances**

---

## SECURITY RULES — NEVER BREAK THESE
- NEVER Arabic script on any weapon, armour, or surface
- NEVER Islamic calligraphy — this is pre-Islamic Persia
- Script on weapons = Ancient Old Persian cuneiform OR Avestan Zoroastrian script ONLY

---

## CRITICAL KNOWN ISSUES — NEVER FORGET

### Escape key crashes UE5 on Mac
- **NEVER press Escape to exit Play In Editor**
- To release mouse during Play: press **Fn+Shift+F1**
- To stop Play: **Fn+Shift+F1** first, then click the **red Stop button ■** in the toolbar

### Negative values — always flag in red 🔴
- Shaz cannot see minus signs without red highlighting
- Every negative Location/Scale value must be shown as: **-1500** 🔴

### Construction Script collision
- Construction Script-created components do NOT get collision automatically in UE5
- Always use direct level actors (Cube from Shapes panel) for anything the player stands on

### Wall/floor geometry — overlap required
- Walls must be positioned so their inner face is INSIDE the floor edge (50-unit overlap)
- Current wall positions (X=±1500, Y=±2000) give correct 50-unit overlap with floor (Scale 35,45,1)

### Outliner search field stuck
- Clear with Cmd+A then Delete, or Escape

### Always click viewport before Cmd+S
- Blueprint editor steals focus — click viewport first

### NEVER change values that are marked ✅ without being told to
- If it works, do not touch it

### ALWAYS check Scale of originals before placing new instances
- This session: new BP_ApadanaColumns placed at Scale Z=1 — WRONG
- Original BP_ApadanaColumns3 has Scale Z=**20** — always verify first

---

## WHAT WAS ACHIEVED THIS SESSION

### BP_SimorghFeather — COMPLETE ✅
- Deleted wrong nodes from Construction Script (Cmd+A → Delete)
- Added Event ActorBeginOverlap in Event Graph
- Connected: Event ActorBeginOverlap → Set Intensity (PointLight) = **150**
- Compiled green ✅
- Pushed to GitHub ✅

### LvL_Tachara — Additional torches COMPLETE ✅
- 6 wall sconces added (East and West walls, Z=300)
- 3 corridor torches added (centre of room, Z=500)
- 4 ceiling brackets added (near ceiling, Z=900)
- Pushed to GitHub ✅

### LvL_Persepolis — Columns placed, Scale fix IN PROGRESS ⚠️
- 8 new BP_ApadanaColumns instances placed around terrace perimeter
- **⚠️ All new instances are at Scale Z=1 — MUST be changed to Scale Z=20**
- One instance Scale Z was being changed to 20 when handoff was called
- Fix all remaining instances before doing anything else next session

---

## CURRENT ACTOR VALUES

### LvL_Tachara

#### Room Geometry
- Floor (Cube): Location 0,0,0 — Scale 35,45,1 — M_TacharaStone ✅
- Ceiling (Cube6): Location 0,0,1000 — Scale 30,40,1 — M_TacharaStone ✅
- North wall (Cube2): Location 0,2000,500 — Scale 30,1,10 — M_TacharaStone ✅
- South wall (Cube3): Location 0,**-2000** 🔴,500 — Scale 30,1,10 — M_TacharaStone ✅
- East wall (Cube4): Location 1500,0,500 — Scale 1,40,10 — M_TacharaStone ✅
- West wall (Cube5): Location **-1500** 🔴,0,500 — Scale 1,40,10 — M_TacharaStone ✅

#### BP_TorchFlicker original 13 instances
All at Z=700, Intensity=800, Temperature=1200K, Attenuation Radius=800

| Name | X | Y |
|------|---|---|
| BP_TorchFlicker | 0 | 0 |
| BP_TorchFlicker2 | 0 | 1800 |
| BP_TorchFlicker3 | 0 | **-1800** 🔴 |
| BP_TorchFlicker4 | 1300 | 0 |
| BP_TorchFlicker5 | **-1300** 🔴 | 0 |
| BP_TorchFlicker6 | **-1000** 🔴 | 1800 |
| BP_TorchFlicker7 | 1000 | 1800 |
| BP_TorchFlicker8 | **-1000** 🔴 | **-1800** 🔴 |
| BP_TorchFlicker9 | 1000 | **-1800** 🔴 |
| BP_TorchFlicker10 | 1300 | 1000 |
| BP_TorchFlicker11 | 1300 | **-1000** 🔴 |
| BP_TorchFlicker12 | **-1300** 🔴 | 1000 |
| BP_TorchFlicker13 | **-1300** 🔴 | **-1000** 🔴 |

#### Additional torches added this session (all BP_TorchFlicker)

**Wall sconces (Z=300):**
| X | Y |
|---|---|
| 1400 | 1800 |
| 1400 | **-1800** 🔴 |
| **-1400** 🔴 | 1800 |
| **-1400** 🔴 | **-1800** 🔴 |
| 1400 | 0 |
| **-1400** 🔴 | 0 |

**Corridor torches (Z=500):**
| X | Y |
|---|---|
| 0 | 1000 |
| 0 | **-1000** 🔴 |
| 0 | 0 |

**Ceiling brackets (Z=900):**
| X | Y |
|---|---|
| 1000 | 1500 |
| **-1000** 🔴 | 1500 |
| 1000 | **-1500** 🔴 |
| **-1000** 🔴 | **-1500** 🔴 |

#### Lighting
- DirectionalLight: default ✅
- SkyLight: Intensity 0.01 (nearly off)
- Player Start: Location 0,0,200

#### M_TacharaStone Material
- Base Color: R=0.025, G=0.012, B=0.008
- Roughness: 0.2
- Applied to all 6 room cubes ✅

---

### LvL_Persepolis

#### CONFIRMED WORKING VALUES — DO NOT CHANGE WITHOUT INSTRUCTION
- Terrace (Cube): Location 0,0,900 — Scale **50,50,18** — M_Limestone ✅
- Desert Floor (Cube2): Location 0,0,**-100** 🔴 — Scale 500,500,1 — M_DesertSand ✅
- BP_ApadanaStairs: Location 0,0,0 — Working ✅
- Player Start: X=300, Y=**-2000** 🔴, Z=1850, Yaw=270

#### BP_ApadanaColumns — CONFIRMED SCALE ✅
- **Scale X=1, Y=1, Z=20** — THIS IS THE CORRECT SCALE FOR ALL COLUMN INSTANCES
- All instances: Location Z=1800 (terrace top)

#### BP_ApadanaColumns instances (all must be Scale Z=20)
| Instance | X | Y | Z | Scale Z | Status |
|----------|---|---|---|---------|--------|
| BP_ApadanaColumns3 | **-2175** 🔴 | **-2175** 🔴 | 1800 | 20 | ✅ Original |
| New corner | 2175 | **-2175** 🔴 | 1800 | 20 | ⚠️ Fix Scale |
| New corner | 2175 | 2175 | 1800 | 20 | ⚠️ Fix Scale |
| New corner | **-2175** 🔴 | 2175 | 1800 | 20 | ⚠️ Fix Scale |
| New mid-side | 0 | **-2175** 🔴 | 1800 | 20 | ⚠️ Fix Scale |
| New mid-side | 0 | 2175 | 1800 | 20 | ⚠️ Fix Scale |
| New mid-side | **-2175** 🔴 | 0 | 1800 | 20 | ⚠️ Fix Scale |
| New mid-side | 2175 | 0 | 1800 | 20 | ⚠️ Fix Scale |

#### M_DesertSand Material
- Constant3Vector: R=0.65, G=0.50, B=0.30 → Multiply B pin → Base Color
- Noise node: Scale=10, Function=Simplex Texture Based → Multiply A pin
- Constant: 0.8 → Roughness

---

### LvL_Vault

#### COMPLETE ✅
- Floor (Cube): Location 0,0,0 — Scale 15,20,1 — M_VaultStone ✅
- Ceiling (Cube2): Location 0,0,500 — Scale 15,20,1 — M_VaultStone ✅
- North wall (Cube3): Location 0,1000,250 — Scale 15,1,5 — M_VaultStone ✅
- South wall (Cube4): Location 0,**-1000** 🔴,250 — Scale 15,1,5 — M_VaultStone ✅
- East wall (Cube5): Location 750,0,250 — Scale 1,20,5 — M_VaultStone ✅
- West wall (Cube6): Location **-750** 🔴,0,250 — Scale 1,20,5 — M_VaultStone ✅
- Player Start: Location 0,0,200 ✅
- BP_TorchFlicker: Location 0,**-900** 🔴,200 (near entrance) ✅
- BP_TorchFlicker2: Location 0,800,200 (near far wall/artefact) ✅
- BP_SimorghFeather: Location 0,800,150 ✅
- DirectionalLight: default, SkyLight Intensity=0.01 ✅

#### M_VaultStone Material
- Base Color: R=0.015, G=0.010, B=0.008
- Roughness: 0.6

#### BP_SimorghFeather Blueprint — COMPLETE ✅
- Components: PointLight + Sphere Collision ✅
- Event Tick → Random Float in Range (Min=100, Max=300) → Set Intensity (pulsing glow) ✅
- Event ActorBeginOverlap → Set Intensity 150 (flash when player touches feather) ✅
- Compiled green, pushed to GitHub ✅

---

## WHAT TO DO NEXT — IN ORDER

### Step 1: Fix all new BP_ApadanaColumns Scale Z to 20 ⚠️ URGENT
- In LvL_Persepolis, click each new column instance in the Outliner
- Set Scale Z to 20 on every one that is currently at Scale Z=1
- There are 7 remaining (one was being changed when handoff was called)
- Save and push to GitHub when done

### Step 2: Niagara flames on torches
- Add real fire particle effects to BP_TorchFlicker in all levels

### Step 3: Story implementation
- Dialogue UI so Simorgh voice plays in LvL_Vault
- LvL_Memory flashback level (triggered by Simorgh)

### Step 4: Push all changes to GitHub

---

## STORY — Chapter 1 Written ✅
- File: /root/SHAHZAD_Ch1_Vault_Dialogue.md
- ROXANA finds Simorgh feather by accident in vault
- She seeks cure for Great Forgetting (Alzheimer's) affecting someone she loves
- That person also connected to brother's fight against the dark one (Ahriman)
- Simorgh speaks as voice only — no visual form in Ch1
- Feather = BP_SimorghFeather trigger object

---

## GITHUB
- Repo: https://github.com/shaz010/SHAHZAD-game
- Project lives on external drive: /Volumes/T7B/SHAHZAD
- .gitignore excludes: Intermediate/, Saved/, Binaries/, Build/, DerivedDataCache/
- To push future changes: cd /Volumes/T7B/SHAHZAD → git add . → git commit -m "message" → git push

---

## APPLE & GOOGLE ACCOUNTS
- Both developer accounts active and paid
- Currently in test/assessment phase
- Game packaging path confirmed
