# SHAHZAD Game Project — Session Handoff
**Last updated:** Aug 29 2026  
**Project:** UE5.8 Mac — Pre-Islamic Persia action game  
**GitHub:** github.com/Shaz010/eee-journal (T7B drive: /Volumes/T7B/SHAHZAD)

---

## ✅ COMPLETED THIS SESSION (Aug 29 2026)

### BP_Enemy — AI MoveTo FULLY WORKING
- BeginPlay → Delay(10s) → AI MoveTo → Get Player Character
- Self connected to Pawn pin ✅
- Get Player Character Return Value → Target Actor ✅
- Auto Possess AI = "Placed in World or Spawned" ✅
- NavMesh Bounds Volume added to LvL_Persia ✅
- **ALL 3 enemies walk toward player 10 seconds after level start ✅**

### BP_Enemy — Error nodes deleted
- Deleted StopJumping (K2Node_CallFunction_23) — leftover player input
- Deleted IA_Look (K2Node_EnhancedInputAction_4) — leftover player input
- Compiled clean — no errors ✅

### LvL_London — Created
- Empty level at /Game/LvL_London.umap ✅
- Pushed to GitHub ✅

### LvL_Memory — Voice lines + Simorgh dialogue WIRED & PLAY TESTED
- VoiceLine3: "The past is not gone. It breathes beneath your feet."
- VoiceLine2: "Ahura Mazda watches. Every step is judgment."
- VoiceLine1: "You were here before. You will be here again."
- Chain: BeginPlay → Delay(5s) → VoiceLine3 → Delay(4s) → VoiceLine2 → Delay(4s) → VoiceLine1 → Delay(2s) → WBP_SimorghDialogue (Create Widget → Add to Viewport)
- PLAY TESTED: all voices fire, collecting 5 thoughts triggers scene change ✅
- Audio files: VoiceLine1/2/3.wav in /Game/Audio/ — fal-ai PLACEHOLDERS only

### LvL_Memory Level Blueprint
- Compiled clean — no errors ✅

### GitHub
- Pushed and up to date ✅

---

## 🔴 PENDING (in priority order — never ask Shaz to choose)

1. **Voice lines — replace placeholders** — iPhone recording when quiet → AirDrop to Mac → Logic Pro (reverb, delay, pitch drop) → export WAV → replace VoiceLine1/2/3.wav in UE5 Content Browser (/Game/Audio/)
2. **Climax sound** — same: iPhone → Logic Pro → import WAV into UE5
3. **LvL_London** — build out the London environment
4. **WBP_SimorghDialogue** — build out the dialogue UI content (currently connected, widget exists but content TBD)

---

## SESSION RULES (never ask Shaz to repeat)

- ❌ Never guess UE5 UI locations — max 2 attempts then send research agent
- ❌ Never ask Shaz to choose priority order
- ✅ Document every breakthrough in SHAHZAD_MASTER.md immediately
- ✅ GitHub push after each meaningful fix (Shaz runs from Terminal)
- ✅ How to open Level Blueprint: toolbar Blueprints icon (near Play) → hover tooltip = "List of world Blueprints available to the user for editing or creation"
- ✅ Content Browser does NOT contain Level Blueprints
- ✅ PlaySound2D fires instantly — always add Delay nodes between sounds
- ✅ fal-ai download links expire — use `curl -L "url" -o ~/Downloads/filename.wav` immediately
- ✅ ElevenLabs curl must run from Shaz's Mac Terminal — cloud container can't reach it

## SECURITY RULE (immutable)
- ❌ NEVER Arabic script on any weapon, armour, or surface
- ❌ NEVER Islamic calligraphy — this is pre-Islamic Persia
- ✅ Script on weapons = Ancient Old Persian cuneiform OR Avestan Zoroastrian script ONLY

---

## FILE LOCATIONS
- T7B Mac: /Volumes/T7B/
- Git repo: /Volumes/T7B/SHAHZAD/.git
- Master notes: /Volumes/T7B/SHAHZAD_MASTER.md
- BP_Enemy: /Game/BP_Enemy (Content Browser)
- Audio placeholders: /Game/Audio/VoiceLine1.wav, VoiceLine2.wav, VoiceLine3.wav
- LvL_Memory: active level with voice chain + Simorgh dialogue
- LvL_Persia: 3 enemies walking ✅
- LvL_London: empty level, ready to build

## GITHUB PUSH (run in Terminal)
```
cd /Volumes/T7B/SHAHZAD
rm /Volumes/T7B/SHAHZAD/.git/index.lock   # if lock exists
git add -A
git commit -m "your message"
git push
```
Note: "Everything up-to-date" after lock errors = push succeeded fine.
