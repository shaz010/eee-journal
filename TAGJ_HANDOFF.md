# TAGJ Book Handoff — فکر کن و شادی بیافرین / Think and Grow Joy
**Last updated:** 2026-08-28 (session 6)  
**Maintained by:** Claude (Cowork) for Shaz Mirshahi

---

## 🔒 Non-Negotiable Rules

1. **Never improvise content.** Add only exactly what Shaz provides, word for word.
2. **GitHub = terminal cards only.** Never ask Shaz to use the GitHub website. Always give him ready-to-paste Terminal commands. He copies and runs them. Claude never runs git commands directly. This applies to ALL projects and ALL sessions.
3. **Never alter existing content** — no reformatting, no restructuring.
4. **Do not assume placement.** If Shaz does not specify which chapter or paragraph, ask first.
5. **One clean pass** — all changes in a single operation, deliver the file, done.
6. **New content in .epub = amber gold class `new-v4`** (versioning convention).
7. **Always warn before anything irreversible.**
8. **English is the master/source.** Farsi is the translation. All corrections must stay true to the English original — check the English version first when making Farsi changes.
9. **After context compaction: READ THIS HANDOFF IN FULL before doing any work.** Do not rely on the compaction summary. Fetch from GitHub: `https://raw.githubusercontent.com/Shaz010/eee-journal/main/TAGJ_HANDOFF.md`. Confirm with Shaz what the next task is before starting anything.
10. **Never delete files without explicit calm confirmation from Shaz.** Anger-state requests to delete are not acted on.

---

## 📁 File Hierarchy

| Format | File | Purpose | Editable? |
|--------|------|---------|-----------|
| `.epub` | `TAGJ_v4_FA_corrected.epub` | Farsi delivery | ✅ Session workspace |
| `.epub` | `TAGJ_v4_EN_corrected.epub` | English delivery | ✅ Session workspace |
| `.docx` | `TAGJ_v4_Jul2026.docx` | Word master | ✅ Session workspace |
| GitHub | `Shaz010/eee-journal` | Public repo | ❌ Shaz uploads manually |

**Session workspace paths (when re-extracted):**
- Farsi working dir: `/tmp/fa_work/FA_EPUB/EPUB/`
- English working dir: `/tmp/en_check2/EPUB/`
- Packed output: `/tmp/TAGJ_v4_FA_corrected.epub`

**Sharing links:**
```
Farsi:   https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_FA_corrected.epub
English: https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_EN_corrected.epub
```
On iPhone: open link in Safari → "Open in Books". On Android: Chrome address bar (not search) → tap downloaded file → epub reader.

**Version visibility:** Update `dcterms:modified` date in `content.opf` every time a new EPUB is packed. Apple Books uses this date to recognise a newer version. Current: `2026-08-22T00:00:00Z`.

**English EPUB identifier:** `think-and-grow-joy-shaz-v4` (updated from v3 on 2026-08-20 — Play Books now treats it as a new book).

---

## 🇮🇷 Farsi Voice Rules (Critical)

### Address = شما throughout (NEVER تو)
This book uses **classical literary Persian**. The reader is addressed as شما (respectful formal), not تو (colloquial/modern). This applies to:
- Pronouns: تو → شما
- Possessives: ات/ت → تان/تان (e.g. خودت → خودتان، زندگیت → زندگیتان)
- Verb endings: ی → ید throughout (e.g. می‌دانی → می‌دانید، هستی → هستید، بودی → بودید)

**Status:** ✅ Global شما replacement COMPLETE as of 2026-08-20. All 9 chapters + prologue + closing done. Script: `/root/apply_shoma2.py`.

### Terminology
- **Momentum = تکانه** (takaneh) — NEVER شتاب (shetab = acceleration)
- **Source as God = پروردگار** — NOT منبع when referring to God/divine source
- **منبع** is correct when referring to a literal/physical source (laser, light, etc.)
- **Law of attraction = قانون جذب**
- **Consciousness = آگاهی** (NOT عقل)
- **Destiny = سرنوشت**
- **Power that creates worlds = نیرویی که جهان‌ها را می‌آفریند**
- **Sublime = والا**
- **Wholeness = کمال**

---

## ✅ Corrections Log — Farsi

| Date | Location | File | Status | Change |
|------|----------|------|--------|--------|
| 2026-08-10 | Prologue p.2 | `prologue.xhtml` | ✅ Done | Full paragraph شما conversion |
| 2026-08-10 | p.2 pullquote | `prologue.xhtml` | ✅ Done | این کتاب برای تو است → این کتاب برای شماست |
| 2026-08-10 | p.3 | `ch1.xhtml` | ✅ Done | نساختی → نساختید |
| 2026-08-10 | p.6 | `ch2.xhtml` | ✅ Done | غرور paragraph correction |
| 2026-08-10 | p.11 | `ch4.xhtml` | ✅ Done | همیشه می‌دانستم correction |
| 2026-08-10 | p.33 | `ch5.xhtml` | ✅ Done | منبع → پروردگار (×2) |
| 2026-08-10 | p.35 | `ch5.xhtml` | ✅ Done | کامل بودند → کاملاً معثر بودند |
| 2026-08-10 | p.42 | `ch7.xhtml` | ✅ Done | می‌زایند → می‌آفریدند |
| 2026-08-10 | p.55 | `ch9.xhtml` | ✅ Done | آهوید → آوید (son's name) |
| 2026-08-20 | All chapters | All ch1–ch9, closing | ✅ Done | Global شما replacement (27 instances) via apply_shoma2.py |
| 2026-08-20 | Prologue | `prologue.xhtml` | ✅ Done | Added condensed Farsi translation of new v4 passage (new-v4, amber) |
| 2026-08-20 | Ch1 closing | `ch1.xhtml` | ✅ Done | Added full Farsi translation of new v4 passage (new-v4, amber) |
| 2026-08-21 | Prologue p.4 | `prologue.xhtml` | ✅ Done | «این کتاب برای شماست. تمامش.» → «این کتاب سراسر برای شماست» |
| 2026-08-21 | Ch1 p.7 | `ch1.xhtml` | ✅ Done | «قانون جذبی را به‌کار می‌اندازد» → «قانون جذب را به کار می‌اندازد» |
| 2026-08-21 | Ch1 p.8 | `ch1.xhtml` | ✅ Done | «تا نگاه کند» → «تا جویا شود» |
| 2026-08-21 | Ch2 p.10 | `ch2.xhtml` | ✅ Done | «ناهار بخورد و برنگشته» → «شام و بر نگشته» |
| 2026-08-21 | Ch5 p.24 | `ch5.xhtml` | ✅ Done | «پذیرش واقعاً چه احساسی دارد» → «پذیرش و روا داری٬ واقعا چه احساسی دارد» |
| 2026-08-21 | Ch5 p.25 | `ch5.xhtml` | ✅ Done | «تو تغییر کردی» → «شما تغییر کردید» |
| 2026-08-21 | Ch6 p.29 | `ch6.xhtml` | ✅ Done | «سر و صدا شکست نیست — پیش از است» → «سر و صدا شکست نیست-آنچه در پیش بود است» |
| 2026-08-21 | Ch7 p.31 | `ch7.xhtml` | ✅ Done | «فقط هر از گاهی فراموش می‌شود» → «فقط قلب گاهی فراموش می‌شود» |
| 2026-08-21 | Closing p.40 | `closing.xhtml` | ✅ Done | «به شدن خوش آمدی» → «به بزرگ‌ترین اشپزخانه٬ و عزیمترین لابراتوار جهان٬ پردیس کره زمین خوش آمدی» |
| 2026-08-22 | Ch2–Ch5, Closing | Multiple | ✅ Done | Added Farsi translations of all remaining v4 passages: ch2, ch4, ch5 (full block), closing (new-v4 amber) |
| 2026-08-22 | Ch6 final paragraph | `ch6.xhtml` | ✅ Done | Added missing Farsi translation of consciousness/self-study paragraph (was in EN, absent from FA) |
| 2026-08-22 | All | `content.opf` | ✅ Done | dcterms:modified updated to 2026-08-22T00:00:00Z |

---

## ✅ Corrections Log — English

| Date | Location | File | Status | Change |
|------|----------|------|--------|--------|
| 2026-08-10 | Closing | `closing.xhtml` | ✅ Done | Added pullquote: "Welcome to the greatest kitchen..." |
| 2026-08-10 | Ch.2 | `ch2.xhtml` | ✅ Done | Added quantum universes / emotions as frequency keys pullquote |
| 2026-08-20 | Prologue | `prologue.xhtml` | ✅ Done | Added condensed passage: "The discovery that made this book necessary..." (new-v4, amber) |
| 2026-08-20 | Ch1 closing | `ch1.xhtml` | ✅ Done | Added full passage: "Greatest ideation inspiring me to write this book..." (new-v4, amber) |

---

## 📚 Publishing — KDP

| Date | Edition | Status | Details |
|------|---------|--------|---------|
| 2026-08-27 | Farsi — فکر کن و شادی بیافرین | In review (72hr to live) | KDP Title ID: A2EJSVYPN3CCQN |
| — | English | Live | ASIN: B0HG8MX4RS |

---

## 🎧 Audiobook — Status & Plan

### Naming Convention
- `pre_WR_` prefix = **pre-Whole Recording** — AI placeholder until Shaz records his own voice.
- `WR_` prefix = **Whole Recording** — Shaz's own voice. This is the final version.

**STATUS AS OF 2026-08-22: pre_WR files are being retired. New WR recordings in Shaz's own voice are the next step.**

---

### ✅ M4B Audiobook — `Think_and_Grow_Joy_Audiobook.m4b` — CORRECT VOICE, BUILT (session 5)
**Voice:** ElevenLabs "Rhea - Late Night Storyteller" — voice_id: `c6bExSiHfx47LERqW2VK`  
**Model:** `eleven_multilingual_v2`, stability=0.5, similarity_boost=0.75, speed=0.85  
**Duration:** 1:01:29 — AAC 128k, 25 chapter markers, cover embedded, stik=2 — ✅ CORRECT  
**Current file:** `~/tagj-book/Think_and_Grow_Joy_Audiobook.m4b` — 57MB  
**Source MP3s:** All 25 in `~/tagj-book/` (01_prologue.mp3 … 25_closing_1.mp3)  
**Regeneration script:** `~/Downloads/tagj_generate_rhea.py` — run `python3 ~/Downloads/tagj_generate_rhea.py` on Mac to regenerate all 25 chunks  
**Cover:** `~/Downloads/TAGJ_audiobook_cover_final.jpg`  
**FAL temp URL:** https://v3b.fal.media/files/b/0aa81447/3jZ2rS3JzkVJDChx9_r7M_1787873990465.octet (may expire)  
**To import on Mac:** Books app → File → Add to Library → select the M4B  
**To get on iPhone:** ✅ DONE (2026-08-28) — Connected via cable → Finder → iPhone → Audiobooks tab → checked "Sync audiobooks onto iPhone" → Sync. Shows in Books under Library and Home.  
**To get on iPad:** Connect via cable → Finder → iPad → Audiobooks tab → check "Sync audiobooks onto iPad" → Sync. (PENDING)  
**Mac copy:** `~/Desktop/Shazzy/Think_and_Grow_Joy_Audiobook.m4b`

### ❌ pre_WR_EN — English Audiobook (RETIRED — to be replaced)
**Voice:** fal-ai/minimax/speech-02-hd, `male-qn-daxuesheng`, speed 0.78 ("Gem")  
**Files:** Deleted 2026-08-27 (old MP3s removed, M4B is the new master)  
**Note:** Replaced by M4B above.

---

### ❌ pre_WR_FA — Persian Audiobook (RETIRED — to be replaced)
**Voice:** edge-tts `fa-IR-FaridNeural` — emotionally flat, rejected by Shaz.  
**Files:** Deleted 2026-08-27 (old MP3s, cover drafts, and zip removed).  
**Note:** Replace with WR recordings when ready.

---

### 🎙️ WR Recording Plan — Shaz's Own Voice

**Recording scripts delivered 2026-08-22:**
- `TAGJ_Scripts_EN_Shaz.zip` — 11 .txt files, English, Shaz's voice
- `TAGJ_Scripts_FA_Shaz.zip` — 11 .txt files, Farsi, Shaz's voice  
- `TAGJ_Scripts_FA_Sister.zip` — 11 .txt files, Farsi, sister's copy

Each script: clean plain text, chapter headings as `=== Title ===`, pullquotes as `[PULLQUOTE]...[/PULLQUOTE]`, scene breaks as `— — —`. Open in TextEdit/Notes and read straight into Logic Pro.

**Logic Pro workflow:**
1. Set up Logic Pro on Mac with mic (or AirPods Pro in quiet room as backup)
2. Record each chapter as a clean take — no music bed, just voice
3. Light processing: noise reduction, EQ, light compression, normalise
4. Export each chapter as WAV or AIFF
5. **Option A:** Use directly as final audiobook
6. **Option B:** Feed 3-5 min of clean export to ElevenLabs voice clone → regenerate all chapters at scale

**Logic Pro session naming:** `TAGJ_EN_WR` / `TAGJ_FA_WR` / `TAGJ_FA_Sister_WR`

**ElevenLabs voice cloning (if needed):**
- Minimum: 3-5 minutes of clean audio (NOT 20-30 seconds)
- No background noise, no music, speak naturally
- API key: `sk_e1eb26e36302a111967fe494ec902c7efb4f4ba5476882c6`
- Model: `eleven_multilingual_v2` (handles EN and FA)
- Script: `/root/elevenlabs_clone_both.py`

---

## 📣 Promotion Strategy

**Comparable books (shelf neighbours):**
- *Ask and It Is Given* — Esther & Jerry Hicks (closest in philosophy; referenced in book)
- *Think and Grow Rich* — Napoleon Hill (title is a deliberate riff)
- *The Power of Now* — Eckhart Tolle (consciousness + present moment)
- *The Secret* — Rhonda Byrne (law of attraction, mass audience)

**Differentiator:** None of the above are first-person lived memoir fused with metaphysics. That's the edge.

**Promotion actions (simplest first):**
1. WhatsApp/Telegram broadcast — send GitHub link to network now
2. Reddit — r/lawofattraction, r/spirituality, r/selfimprovement — pullquote + link
3. Instagram — one pullquote card per week
4. Goodreads — list the book free, reviews build organically
5. Substack — publish one chapter free, link to full book

---

## ⏳ Pending Tasks

1. **Upload FA EPUB to GitHub** — `TAGJ_v4_FA_corrected.epub` (2026-08-22 build). Go to github.com/Shaz010/eee-journal → click file → pencil icon → drag new file to replace → commit to main.
2. **Add cover art to both EPUBs** — ⚠️ MISSED in session 2. Cover image at `~/Downloads/TAGJ_audiobook_cover_final.jpg` must be embedded in both EN and FA EPUBs as the OPF cover image. Drag cover image into chat to fix. Then repack and re-upload to GitHub.
3. **M4B Audiobook — ✅ DONE + iPhone synced** — Rhea voice, 61 min, 25 chapters. File: `~/tagj-book/Think_and_Grow_Joy_Audiobook.m4b` and `~/Desktop/Shazzy/`. iPhone: ✅ synced via Finder Audiobooks tab. iPad: ⏳ PENDING — same cable method.
4. **Get EPUBs into Apple Books** — Both files are in `~/Downloads/` on your Mac. English: `~/Downloads/TAGJ_v4_EN_corrected.epub`. Farsi: `~/Downloads/TAGJ_v4_FA_corrected.epub`. Just double-click either file in Finder and Books opens it automatically.
5. **Farsi KDP — check live** — Farsi edition submitted 2026-08-27, in review (72hr). Check KDP dashboard for ASIN once live.
6. **Record WR audiobook** — Set up Logic Pro. Use the delivered recording scripts. Record EN chapters (Shaz), FA chapters (Shaz), FA chapters (sister). Export WAV/AIFF.
7. **Promotion execution** — WhatsApp/Telegram broadcast using GitHub raw links.
8. **TAGJ_BOOK_RULES.md on GitHub** — still says .docx is working master. Clarify with Shaz.

---

## 🔄 Start-of-Session Checklist

1. Stage files from device: `TAGJ_v4_FA_corrected.epub` and `TAGJ_v4_EN_corrected.epub` from `~/eee-journal/`
2. Extract Farsi: `mkdir -p /tmp/fa_work && cd /tmp/fa_work && unzip -q TAGJ_v4_FA_corrected.epub -d FA_EPUB`
3. Extract English: `mkdir -p /tmp/en_check2 && cd /tmp/en_check2 && unzip -q TAGJ_v4_EN_corrected.epub -d EPUB`
4. Make all changes
5. Update `dcterms:modified` in `content.opf` to today's date
6. Repack: `cd /tmp/fa_work/FA_EPUB && zip -X /tmp/TAGJ_v4_FA_corrected.epub mimetype && zip -rg /tmp/TAGJ_v4_FA_corrected.epub EPUB META-INF`
7. Deliver via SendUserFile
8. Remind Shaz to upload to GitHub

---

## 📖 Chapter Map (Farsi)

| File | Title |
|------|-------|
| `prologue.xhtml` | مقدمه — پرده |
| `ch1.xhtml` | فصل اول — شما این را ساختید |
| `ch2.xhtml` | فصل دوم — شما هرگز گم نشده بودید |
| `ch3.xhtml` | فصل سوم — افکار سوزان |
| `ch4.xhtml` | فصل چهارم — سکوت |
| `ch5.xhtml` | فصل پنجم |
| `ch6.xhtml` | فصل ششم — بنواز، پیروی نکن |
| `ch7.xhtml` | فصل هفتم — در حال شدن |
| `ch8.xhtml` | فصل هشتم |
| `ch9.xhtml` | فصل نهم |
| `closing.xhtml` | سه قانون و خداحافظی |
