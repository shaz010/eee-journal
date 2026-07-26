# TAGJ Book Editing Rules — Reference for All Sessions

## Core rules (non-negotiable)

- **Never improvise.** Add only exactly what Shaz provides, word for word.
- **Never deviate** from the original request.
- **Never touch the EPUBs.** EPUBs are final delivery files. All edits go into the .docx only.
- **New content in amber gold** (hex B8860B) — this is the book's versioning convention. Every new addition must appear in this colour so readers can see what changed since last version.
- **Do not alter existing content** — no reformatting, no restructuring, no touching what is already there.
- **Do not assume placement.** If Shaz does not specify which chapter or paragraph, ask before inserting.
- **One clean pass** — make all changes in a single operation, deliver the file, done.

## File hierarchy

| Format | Purpose | Editable? |
|--------|---------|-----------|
| .docx  | Working master — all edits happen here | ✅ Yes |
| .epub  | Final delivery — English and Farsi | ❌ Never touch |
| .pdf   | Final delivery | ❌ Never touch |

## Versioning convention

- Each version marks new additions in **amber gold (B8860B)**
- Once Shaz has read and absorbed the new content, the next build normalises it to standard text
- A new colour marks whatever comes next
- Always save as the next version number (v3 → v4, etc.)

## Persian translation notes

- **Momentum = تکانه** (takaneh) — NOT شتاب (shetab / acceleration)
- Corrections to be applied to the Persian .docx in one pass once the full list is received

## Corrections log (English)

1. **Momentum = تکانه** *(Persian — replace all instances of شتاب with تکانه)*
2. **Ch.4 · Para 1** — "but I was too blind from the noise to see" → "but I was too deaf from the noise to hear it"
3. **Ch.7 · Pg.14 · Para 1** — REMOVE the sentence: "Not a morning when you wake up healed."
4. *(more to be added — Shaz is compiling the full list)*

## Repo

- English/Farsi TAGJ files live at `/root/` in the session workspace
- Latest working docx: `TAGJ_v4_Jul2026.docx`
- User uploads all files to GitHub manually — never push, never commit
