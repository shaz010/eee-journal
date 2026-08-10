# TAGJ Book Handoff — فکر کن و شادی بیافرین / Think and Grow Joy
**Last updated:** 2026-08-10  
**Maintained by:** Claude (Cowork) for Shaz Mirshahi

---

## 🔒 Non-Negotiable Rules

1. **Never improvise content.** Add only exactly what Shaz provides, word for word.
2. **Never push to GitHub.** Shaz uploads all files manually via the GitHub website.
3. **Never alter existing content** — no reformatting, no restructuring.
4. **Do not assume placement.** If Shaz does not specify which chapter or paragraph, ask first.
5. **One clean pass** — all changes in a single operation, deliver the file, done.
6. **New content in .docx = amber gold colour #B8860B** (versioning convention).
7. **Always warn before anything irreversible.**

---

## 📁 File Hierarchy

| Format | File | Purpose | Editable? |
|--------|------|---------|-----------|
| `.epub` | `TAGJ_v4_FA_corrected.epub` | Farsi delivery | ✅ Session workspace |
| `.epub` | `TAGJ_v4_EN_corrected.epub` | English delivery | ✅ Session workspace |
| `.docx` | `TAGJ_v4_Jul2026.docx` | Word master | ✅ Session workspace |
| GitHub | `Shaz010/eee-journal` | Public repo | ❌ Shaz uploads manually |

**Session workspace paths:**
- Farsi extracted: `/root/tagj_fa_uploaded/EPUB/`
- English extracted: `/root/tagj_en_epub/EPUB/`
- Packed output: `/root/TAGJ_v4_FA_corrected.epub` and `/root/TAGJ_v4_EN_corrected.epub`

**Sharing link for friends:**
```
https://github.com/Shaz010/eee-journal/raw/main/TAGJ_v4_FA_corrected.epub
```
On iPhone: open in Safari → "Open in Books". On Android: Chrome → tap file → epub reader.

**Version visibility:** Update `dcterms:modified` date in `content.opf` every time a new EPUB is packed. Apple Books uses this date to recognise a newer version.

---

## 🇮🇷 Farsi Voice Rules (Critical)

### Address = شما throughout (NEVER تو)
This book uses **classical literary Persian**. The reader is addressed as شما (respectful formal), not تو (colloquial/modern). This applies to:
- Pronouns: تو → شما
- Possessives: ات/ت → تان/تان (e.g. خودت → خودتان، زندگیت → زندگیتان)
- Verb endings: ی → ید throughout (e.g. می‌دانی → می‌دانید، هستی → هستید، بودی → بودید)

**Status:** The global شما replacement across all 9 chapters + prologue + closing is **NOT YET DONE** as of 2026-08-10. Only specific called-out instances have been corrected. This is a major pending task.

### Terminology
- **Momentum = تکانه** (takaneh) — NEVER شتاب (shetab = acceleration)
- **Source as God = پروردگار** — NOT منبع when referring to God/divine source
- **منبع** is correct when referring to a literal/physical source (laser, light, etc.)

---

## ✅ Corrections Log — Farsi

| Page | File | Status | Change |
|------|------|--------|--------|
| Prologue p.2 | `prologue.xhtml` | ✅ Done 2026-08-10 | Full paragraph شما: می‌خوانی→می‌خوانید، می‌خواستی→می‌خواستید، یاد گرفتی→یادگرفتید، پیروی کنی→پیروی کنید، فراموش کردی→فراموش کردید، خودت→خودتان، اجازه بدهی→اجازه بدهید |
| p.2 pullquote | `prologue.xhtml` | ✅ Done 2026-08-10 | این کتاب برای تو است → این کتاب برای شماست |
| p.3 | `ch1.xhtml` | ✅ Done | نساختی → نساختید |
| p.4 | `ch1.xhtml` | ✅ Already correct | کار می‌کند (was رواست in older version — base file already had correct text) |
| p.6 | `ch2.xhtml` | ✅ Done | اگر ممکن بود غرور... → اگر‌ممکن بود احساس رضایت را دست کم گرفته، بی‌حوصلگی نمی‌کردیم، نیازی به یادآوری نمی‌بود |
| p.11 | `ch4.xhtml` | ✅ Done | همیشه می‌دانستم که به همه‌ی اینها بیشتر هست → همیشه می‌دانستم از آنچه چشم می‌بیند بیشتر وجود دارد |
| p.33 | `ch5.xhtml` | ✅ Done | منبع همیشه با من است → پروردگار همیشه با من است (and از منبع بازتنظیم → از پروردگار بازتنظیم) |
| p.35 | `ch5.xhtml` | ✅ Done | کامل بودند → کاملاً معثر بودند |
| p.42 | `ch7.xhtml` | ✅ Done | می‌زایند → می‌آفریدند |
| p.55 | `ch9.xhtml` | ✅ Done | آهوید → آوید (son's name) |

---

## ✅ Corrections Log — English

| Location | File | Status | Change |
|----------|------|--------|--------|
| Closing | `closing.xhtml` | ✅ Done | Added pullquote: "Welcome to the greatest kitchen you've ever been in — the largest and the most magnificent laboratory mankind has ever known: planet Earth." |
| Ch.2 | `ch2.xhtml` | ✅ Done | Added pullquote after "emotions are the compass" para: quantum universes / emotions as frequency keys passage |

---

## ⏳ Pending Tasks

1. **Global شما replacement (Farsi)** — All 9 chapters + prologue + closing. Every verb ending ی→ید, every pronoun تو→شما, every possessive ات→تان. Not yet done. Needs a systematic Python pass chapter by chapter with review.

2. **TAGJ_BOOK_RULES.md on GitHub** says .docx is the working master. Current workflow edits EPUBs directly. Clarify with Shaz which is authoritative going forward.

3. **More corrections may be pending** — Shaz is compiling a full list. Check MASTER_VAULT.md on their device at `Documents/Claude_Vault/MASTER_VAULT.md` at start of each session.

---

## 🔄 Start-of-Session Checklist

1. Check GitHub repo for latest uploaded files: `https://github.com/Shaz010/eee-journal`
2. Ask Shaz to upload the latest corrected EPUB if you need to work from it (GitHub API can't download binary files via WebFetch due to robots.txt — use the file upload in chat)
3. Extract: `mkdir -p /root/tagj_fa_work && cd /root/tagj_fa_work && unzip -q /path/to/uploaded.epub`
4. Make all changes, then repack: `cd /root/tagj_fa_work && zip -X output.epub mimetype && zip -rg output.epub EPUB META-INF`
5. Update `dcterms:modified` date in `content.opf` before packing
6. Deliver via SendUserFile

---

## 📖 Chapter Map (Farsi)

| File | Title |
|------|-------|
| `prologue.xhtml` | مقدمه — پرده |
| `ch1.xhtml` | فصل اول — تو این را ساختی |
| `ch2.xhtml` | فصل دوم — تو هرگز گم نشده بودی |
| `ch3.xhtml` | فصل سوم — افکار سوزان |
| `ch4.xhtml` | فصل چهارم |
| `ch5.xhtml` | فصل پنجم |
| `ch6.xhtml` | فصل ششم |
| `ch7.xhtml` | فصل هفتم |
| `ch8.xhtml` | فصل هشتم |
| `ch9.xhtml` | فصل نهم |
| `closing.xhtml` | سه قانون و خداحافظی |
