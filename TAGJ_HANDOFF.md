# SHAHZAD UE5 — Session Handoff Update
Last updated: 2026-09-10

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

## Your Salon Pro — iOS App Store (updated 2026-09-10)

### Current Status
- ✅ **Waiting for Review — Build 7, Version 1.0** (confirmed in App Store Connect)
- ✅ salon.html v0.48 + app.html v2.57 live on getcommissionpro.com
- ✅ viewController.swift updated on MacBook Pro with WKScriptMessageHandler for openURL
  - File at: `/Users/shahbazmirshahi/Desktop/Your Salon/Your Salon Pro/viewController.swift`
  - Adds `config.userContentController.add(self, name: "openURL")` so Privacy/EULA links open in Safari
- ✅ Build 7 confirmed attached to active review submission (not Build 5)
- ✅ App Review notes submitted explaining sign-in bypass + paywall compliance

### Pending (Your Salon Pro)
- Wait for Apple review response (1–3 days)
- If rejected again: submission has Build 7 + server-side HTML fixes — should pass
- Xcode on MacBook Pro: "Unable to log in with account shahbazmirshahi@mac.com" warning in Signing & Capabilities — low priority, doesn't block current review

### Key Files
| File | Version | Status |
|------|---------|--------|
| salon.html | v0.48 | Live on GitHub Pages |
| app.html | v2.57 | Live on GitHub Pages |
| viewController.swift | openURL handler | Written to MacBook Pro |
| Build | 7 (1.0) | In App Store Review queue |

---

## Session Progress Today (2026-09-10)
- ✅ viewController.swift written to MacBook Pro with WKScriptMessageHandler for openURL
- ✅ Confirmed Build 7 is attached to "Waiting for Review" submission in App Store Connect
- ✅ Attempted to switch from Build 5 → Build 7 — already on Build 7 (no switch needed)
- ✅ Logged into App Store Connect via Chrome to verify build

## Pending (UE5)
- Language Toggle wiring (above)
- Portal_Persia Faravahar texture (blocked — need image from Shaz)
- WAV Import (blocked — Apogee adapter)

## Key Rules Reminder
- NEVER Arabic script, NEVER Islamic calligraphy — pre-Islamic Persia only
- NEVER AssetEditorSubsystem / open_editor_for_assets (crashes UE5)
- Files to T7B: device_bash via $HOME/mnt/T7B/
- Farsi address: شما (NEVER تو)
