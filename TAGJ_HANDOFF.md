# TAGJ Book Handoff — فکر کن و شادی بیافرین / Think and Grow Joy
**Last updated:** 2026-08-21  
**Maintained by:** Claude (Cowork) for Shaz Mirshahi

---

## 🔒 Non-Negotiable Rules

1. **Never improvise content.** Add only exactly what Shaz provides, word for word.
2. **Never push to GitHub.** Shaz uploads all files manually via the GitHub website.
3. **Never alter existing content** — no reformatting, no restructuring.
4. **Do not assume placement.** If Shaz does not specify which chapter or paragraph, ask first.
5. **One clean pass** — all changes in a single operation, deliver the file, done.
6. **New content in .epub = amber gold class `new-v4`** (versioning convention).
7. **Always warn before anything irreversible.**
8. **English is the master/source.** Farsi is the translation. All corrections must stay true to the English original — check the English version first when making Farsi changes.

---

## 📁 File Hierarchy

| Format | File | Purpose | Editable? |
|--------|------|---------|-----------|
| `.epub` | `TAGJ_v4_FA_corrected.epub` | Farsi delivery | ✅ Session workspace |
| `.epub` | `TAGJ_v4_EN_corrected.epub` | English delivery | ✅ Session workspace |
| `.docx` | `TAGJ_v4_Jul2026.docx` | Word master | ✅ Session workspace |
| GitHub | `Shaz010/eee-journal` | Public repo | ❌ Shaz uploads manually |

**Session workspace paths (when re-extracted):**
- Farsi working dir: `/root/tagj_fa_work/EPUB/`
- English working dir: `/tmp/en_v4/EPUB/`
- Packed output: `/root/TAGJ_v4_FA_corrected.epub` and `/root/TAGJ_v4_EN_corrected.epub`

**Sharing links:**
```
Farsi:   https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_FA_corrected.epub
English: https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_EN_corrected.epub
```
On iPhone: open link in Safari → "Open in Books". On Android: Chrome address bar (not search) → tap downloaded file → epub reader.

**Version visibility:** Update `dcterms:modified` date in `content.opf` every time a new EPUB is packed. Apple Books uses this date to recognise a newer version. Current date: `2026-08-20T00:00:00Z`.

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
| 2026-08-20 | Prologue | `prologue.xhtml` | ✅ Done | Added condensed Farsi translation of new passage (new-v4, amber) |
| 2026-08-20 | Ch1 closing | `ch1.xhtml` | ✅ Done | Added full Farsi translation of new passage before bridge paragraph (new-v4, amber) |

---

## ✅ Corrections Log — English

| Date | Location | File | Status | Change |
|------|----------|------|--------|--------|
| 2026-08-10 | Closing | `closing.xhtml` | ✅ Done | Added pullquote: "Welcome to the greatest kitchen..." |
| 2026-08-10 | Ch.2 | `ch2.xhtml` | ✅ Done | Added quantum universes / emotions as frequency keys pullquote |
| 2026-08-20 | Prologue | `prologue.xhtml` | ✅ Done | Added condensed passage: "The discovery that made this book necessary..." (new-v4, amber) |
| 2026-08-20 | Ch1 closing | `ch1.xhtml` | ✅ Done | Added full passage: "Greatest ideation inspiring me to write this book..." (new-v4, amber) |

---

## 🎧 Audiobook — Status & Plan

### Naming Convention
All AI-generated versions are prefixed `pre_WR_` = **pre-Whole Recording** — placeholders until Shaz records his own voice.

---

### ✅ pre_WR_EN — English Audiobook (COMPLETE)
**Voice:** fal-ai/minimax/speech-02-hd, `male-qn-daxuesheng`, speed 0.78 ("Gem")  
**Files:** 14 MP3s in `~/Music/TAGJ_audiobook/`  
**Playlist launcher:** `~/Music/TAGJ_audiobook/Play_TAGJ_EN.command` (double-click in Finder)  
**iCloud:** `~/Library/Mobile Documents/com~apple~CloudDocs/TAGJ_audiobook/`

| File | Chapter |
|------|---------|
| 00_prologue.mp3 | Prologue |
| 01_chapter_one.mp3 | Chapter 1 |
| 02_chapter_two.mp3 | Chapter 2 |
| 03_chapter_three_p1.mp3 | Chapter 3 Part 1 |
| 03_chapter_three_p2.mp3 | Chapter 3 Part 2 |
| 04_chapter_four.mp3 | Chapter 4 |
| 05_chapter_five_p1.mp3 | Chapter 5 Part 1 |
| 05_chapter_five_p2.mp3 | Chapter 5 Part 2 |
| 05_chapter_five_p3.mp3 | Chapter 5 Part 3 |
| 06_chapter_six.mp3 | Chapter 6 |
| 07_chapter_seven.mp3 | Chapter 7 |
| 08_chapter_eight.mp3 | Chapter 8 |
| 09_chapter_nine.mp3 | Chapter 9 |
| 10_closing.mp3 | Closing |

**Note:** Ch3 and Ch5 split into parts due to fal-ai 4500-char limit.

---

### ✅ pre_WR_FA — Persian Audiobook (COMPLETE)
**Voice:** edge-tts `fa-IR-FaridNeural`, rate="-15%" — best available Tehran accent  
**Files:** 11 MP3s in `~/Music/TAGJ_FA_audioboo/` (folder name truncated — leave as-is)  
**Playlist launcher:** `~/Music/TAGJ_FA_audioboo/Play_TAGJ_FA.command` (double-click in Finder)  
**iCloud:** `~/Library/Mobile Documents/com~apple~CloudDocs/TAGJ_FA_audiobook/`  
**Sister's zip:** `~/Desktop/TAGJ_FA_audiobook.zip` (19.9MB) — send via Telegram  
**Sister's instructions:** sent in Persian (Telegram-ready text in session chat)

| File | Chapter |
|------|---------|
| 00_prologue.mp3 | مقدمه |
| 01_chapter_one.mp3 | فصل اول |
| 02_chapter_two.mp3 | فصل دوم |
| 03_chapter_three.mp3 | فصل سوم |
| 04_chapter_four.mp3 | فصل چهارم |
| 05_chapter_five.mp3 | فصل پنجم |
| 06_chapter_six.mp3 | فصل ششم |
| 07_chapter_seven.mp3 | فصل هفتم |
| 08_chapter_eight.mp3 | فصل هشتم |
| 09_chapter_nine.mp3 | فصل نهم |
| 10_closing.mp3 | خداحافظی |

**Generator script:** `/root/tagj_fa_audiobook.py` — run on Mac Terminal (edge-tts SSL blocked in cloud)

---

### ❌ Why AI Voices Aren't the Final Version
- **Farid (Farid Neural):** Half Tehran accent — technically correct but emotionally flat. Doesn't capture the intimacy and effect the book demands.
- **Gem (male-qn-daxuesheng):** Warm and paced well in English, but AI — the soul isn't there.
- **Verdict:** Voice and sound in a book like TAGJ are everything. The wrong delivery kills the effect. AI voices are placeholders only.

---

### 🎙️ Next Step — Record in Own Voice via Logic Pro

**Plan:**
1. Set up Logic Pro on Mac with a decent mic (or even AirPods Pro in quiet room as backup)
2. Record each chapter as a clean take — no music bed, just voice
3. Use Logic Pro for light processing: noise reduction, EQ, light compression, normalise
4. Export each chapter as WAV or AIFF from Logic Pro
5. **Option A:** Use as final audiobook directly (cleanest)
6. **Option B:** Feed 3-5 minutes of clean export to ElevenLabs professional clone → regenerate all chapters in Shaz's voice at scale

**ElevenLabs requirements for voice cloning:**
- Minimum: 3-5 minutes of clean audio (not 20-30 seconds — that produces bad results)
- No background noise, no music
- Speak naturally, varied pace — don't perform
- API key: `sk_e1eb26e36302a111967fe494ec902c7efb4f4ba5476882c6`
- Model for generation: `eleven_multilingual_v2` (handles both EN and FA)
- Script for cloning: `/root/elevenlabs_clone_both.py`

**Logic Pro session naming:** `TAGJ_EN_recording` / `TAGJ_FA_recording`

**Voice testing done (2026-08-20):**

| # | Voice preset | Speed | Verdict |
|---|-------------|-------|---------|
| 1 | default | 1.0 | Too heavy |
| 2 | female | 1.0 | Car salesman |
| 3 | male-qn-daxuesheng | 1.0 | Good warmth |
| 4 | audiobook_female_1 | 1.0 | Nice but not quite |
| 5 | wise_woman | 1.0 | Car salesman |
| **6** | **male-qn-daxuesheng** | **0.78** | **⭐ THE GEM — EN placeholder** |
| 7 | deep_voice_man | 0.85 | Female again |
| 8 | audiobook_male_1 | 0.78 | Female again |
| 9 | male-qn-jingying | 0.78 | Female again |
| 10 | Chatterbox model | — | Car salesman |

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

1. **Record in own voice** — Set up Logic Pro session. Record each chapter in EN and FA. Export clean WAV/AIFF per chapter. This is the WR (Whole Recording) version that replaces all pre_WR files.
2. **ElevenLabs voice clone (optional)** — Once 3-5 min clean Logic Pro export is ready, run `/root/elevenlabs_clone_both.py` to clone voice, then regenerate all chapters at scale. Only needed if direct recording isn't used as final.
3. **Upload latest EPUBs to GitHub** — Both EN and FA corrected versions need uploading after 2026-08-20 session.
4. **Promotion execution** — start with WhatsApp/Telegram broadcast using the GitHub raw links.
5. **TAGJ_BOOK_RULES.md on GitHub** — still says .docx is working master. Clarify with Shaz.

---

## 🔄 Start-of-Session Checklist

1. Clone repo: `git clone https://github.com/Shaz010/eee-journal.git /root/eee-journal`
2. Extract Farsi: `mkdir -p /root/tagj_fa_work && cd /root/tagj_fa_work && unzip -q /root/eee-journal/TAGJ_v4_FA_corrected.epub`
3. Extract English: `mkdir -p /tmp/en_v4 && cd /tmp/en_v4 && unzip -q /root/eee-journal/TAGJ_v4_EN_corrected.epub`
4. Make all changes
5. Update `dcterms:modified` in `content.opf` to today's date
6. Repack: `cd /root/tagj_fa_work && zip -X /root/TAGJ_v4_FA_corrected.epub mimetype && zip -rg /root/TAGJ_v4_FA_corrected.epub EPUB META-INF`
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
| `ch4.xhtml` | فصل چهارم |
| `ch5.xhtml` | فصل پنجم |
| `ch6.xhtml` | فصل ششم |
| `ch7.xhtml` | فصل هفتم |
| `ch8.xhtml` | فصل هشتم |
| `ch9.xhtml` | فصل نهم |
| `closing.xhtml` | سه قانون و خداحافظی |
