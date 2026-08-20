# TAGJ Book Handoff — فکر کن و شادی بیافرین / Think and Grow Joy
**Last updated:** 2026-08-20  
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

### Voice Testing (2026-08-20)
Tested using `fal-ai/minimax/speech-02-hd` TTS model. Results:

| # | Voice preset | Speed | Verdict |
|---|-------------|-------|---------|
| 1 | default | 1.0 | Too heavy |
| 2 | female | 1.0 | Car salesman |
| 3 | male-qn-daxuesheng | 1.0 | Good warmth |
| 4 | audiobook_female_1 | 1.0 | Nice but not quite |
| 5 | wise_woman | 1.0 | Car salesman |
| **6** | **male-qn-daxuesheng** | **0.78** | **⭐ THE GEM — keeper** |
| 7 | deep_voice_man | 0.85 | Female again |
| 8 | audiobook_male_1 | 0.78 | Female again |
| 9 | male-qn-jingying | 0.78 | Female again |
| 10 | Chatterbox model | — | Car salesman |

**Winning config:**
```
model: fal-ai/minimax/speech-02-hd
voice: male-qn-daxuesheng
speed: 0.78
```

### Next Step — Voice Cloning
Shaz to record his own voice:
1. Open **Voice Memos** on iPhone 16 Pro Max
2. Find a quiet room, speak naturally (not performed)
3. Read any passage — 20-30 seconds is enough
4. Send the audio file in the chat
5. Claude will use `fal-ai/chatterbox/text-to-speech` with the voice clone to generate the full audiobook in Shaz's own voice
6. Logic Pro available for cleanup if needed (likely won't be — iPhone 16 Pro Max mic is clean)

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

1. **Voice cloning audiobook** — Shaz to send 20-30 second voice recording. Claude to generate full audiobook in Shaz's voice using Chatterbox model.
2. **Upload latest EPUBs to GitHub** — Both EN and FA corrected versions need uploading after today's session.
3. **Promotion execution** — start with WhatsApp/Telegram broadcast using the GitHub raw links.
4. **TAGJ_BOOK_RULES.md on GitHub** — still says .docx is working master. Clarify with Shaz.

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
