# SHAHZAD UE5 — Session Handoff Update
Last updated: 2026-09-04 ~16:56

## IMMEDIATE NEXT STEP
WBP_LanguageToggle is OPEN in UE5 Widget Editor (Designer view).

### To wire Language Toggle OnClicked:
1. Click **Graph** tab (top-right of widget editor)
2. In the Graph, right-click empty space → search **"OnClicked"** → pick **Event OnClicked (Button_2)**
3. From that node's white exec pin, drag → search **FlipFlop** → add it
4. From FlipFlop **A** pin → drag → search **SetText** → pick **Set Text (TextBlock_0)**
   - In the text pin, type: `EN | فا`
5. From FlipFlop **B** pin → drag → search **SetText** → pick **Set Text (TextBlock_0)**
   - In the text pin, type: `فا | EN`
6. Click **Compile** (top toolbar) → **Save**

### Alternative (if Button_2 OnClicked isn't in right-click):
- In **Designer** tab → click **Button_2** in Hierarchy
- In Details panel right side → scroll to **Events** → click **+** next to **OnClicked**
- This auto-creates the event node in Graph

---

## Session Progress Today
- ✅ F_Vazirmatn composite Font asset created
- ✅ Vazirmatn_Regular FontFace linked via import_text
- ✅ WBP_LanguageToggle TextBlock_0 font set to F_Vazirmatn (compiled, saved)
- ✅ WBP_LanguageToggle is open and ready for graph wiring
- 🔄 Language Toggle OnClicked wiring — NEXT

## Pending
- Language Toggle wiring (above)
- Portal_Persia Faravahar texture (blocked — need image from Shaz)
- WAV Import (blocked — Apogee adapter)
- Update TAGJ_HANDOFF.md

## Key Rules Reminder
- NEVER Arabic script, NEVER Islamic calligraphy — pre-Islamic Persia only
- NEVER AssetEditorSubsystem / open_editor_for_assets (crashes UE5)
- Files to T7B: device_bash via $HOME/mnt/T7B/
- Farsi address: شما (NEVER تو)
