# GRAIN — Game Project Handoff
Last updated: 2026-10-31

## What is Grain?

A Rygar-inspired side-scroller game by **Shaz & Roxana** (father & daughter).
Inspired by Rygar (Atari/Tecmo, 1990) — disc-flail combat, ancient world aesthetic.

**Goal:** Web prototype → TestFlight (iOS + Mac) → free + paid tiers.

## Characters

| Char | Player | Weapon | HP | Speed |
|------|--------|--------|----|-------|
| RYKAR | Shaz | Disc (throws + returns on chain) | 120 | 3.6 |
| ROX | Roxana | Slash arc blade | 90 | 5.2 |

## Phase Roadmap

| Phase | Theme | Status |
|-------|-------|--------|
| 1 | Rygar side-scroller — run/jump/disc/enemies/boss | ✅ Web prototype live |
| 2 | Space / asteroids — zero gravity, momentum | ⬜ Planned |
| 3 | Black holes & gravity wells — warp, bad actors | ⬜ Planned (paid) |

Free: Phase 1+2 | Paid: Phase 3+

## Current Build — Phase 1 v0.1 (2026-10-31)

- Title + char select + solo + co-op ✅
- P1: arrows/WASD + Z=attack + X=jump ✅
- P2 co-op: IJKL + U=attack + O=jump ✅
- 4000px scrolling level + parallax background ✅
- Enemies: grunt, fly, demon boss ✅
- Rygar disc weapon (throws + returns on chain) ✅
- Rox slash weapon ✅
- HP / lives / score / victory / game over ✅
- Mobile touch controls ✅

## Files

| File | Repo | Notes |
|------|------|-------|
| grain.html | mgm-studio (to add) | Single-file game |
| GRAIN_HANDOFF.md | eee-journal (T7B) + Mac | This file |

## Next Steps

- [ ] Shaz + Roxana play-test — collect feedback
- [ ] Add sound effects (Web Audio API)
- [ ] More enemy types (ranged, shielded)
- [ ] High score localStorage save
- [ ] Push grain.html to mgm-studio

## Phase 2 Prep

- [ ] Zero-gravity physics (no ground, momentum-based)
- [ ] Asteroid field generation
- [ ] Energy pulse weapon (space variant)

## Phase 3 Prep (Paid)

- [ ] Gravity well mechanic
- [ ] Warp tunnels
- [ ] Bad actor enemies
- [ ] Apple IAP gate (StoreKit 2)

## TestFlight Plan

1. Port to WKWebView Xcode app
2. iOS + macOS Catalyst bundle
3. Free = Ph1+2 · Paid = Ph3 via Apple IAP
4. TF internal → App Store

## Non-negotiables

1. Shaz & Roxana both co-creators
2. Apple IAP only — no Stripe
3. Co-op from day one
4. Web prototype before native
5. Separate from Your Salon

## Key Dates

| Event | Date |
|-------|------|
| Started | 2026-10-31 |
| Phase 1 prototype | 2026-10-31 |

*Maintained by Claude. Lives in: eee-journal/T7B + Mac + mgm-studio/Git.*
