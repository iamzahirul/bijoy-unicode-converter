# বিজয় ⇄ ইউনিকোড কনভার্টার · Bijoy ⇄ Unicode Converter

> পুরনো **Bijoy / SutonnyMJ** লেখা এক ক্লিকে **ইউনিকোডে** রূপান্তর করুন — আর উল্টোটাও। Two-way converter between legacy Bijoy (ANSI) Bangla and Unicode, fully in the browser.

Bangladesh's govt offices, courts and newspapers still carry decades of text typed in Bijoy. Copy it anywhere modern (web, Facebook, Word Unicode) and it turns into garbage like `Avwg evsjv‡`ki`. This tool fixes that — instantly, for free, offline.

## ✨ Features

- ✅ **Bijoy → Unicode** with full conjunct (যুক্তাক্ষর) support: `Dfq cv‡k...` → `উভয় পাশে...`
- ✅ **Unicode → Bijoy** reverse conversion (round-trip tested ✔)
- ✅ Handles kars reordering, রেফ, হসন্ত, য-ফলা, র-ফলা, ং ঃ ঁ, বাংলা সংখ্যা
- ✅ **Smart hint**: paste the wrong type of text and it suggests flipping modes
- ✅ One-click **swap**, **copy**, sample texts, char/word counter
- ✅ **100% offline** — no data ever leaves your browser, no signup, no ads
- ✅ Zero build step: open `index.html` or host on free GitHub Pages

## 🧪 Verified

```text
বিজয়   : Dfq cv‡k av‡bi kx‡l †ewóZ cvwb‡Z fvmgvb RvZxq dzj kvcjv|
ইউনিকোড : উভয় পাশে ধানের শীষে বেষ্টিত পানিতে ভাসমান জাতীয় ফুল শাপলা।
```

Round-trip test: `আমার সোনার বাংলা...` → বিজয় → ইউনিকোড = **identical** ✔
Conjunct test: `বিজ্ঞান, বন্ধু, শুভ্র, রাষ্ট্র, বিদ্যালয়, জাতীয় সংসদ` ✔

## 🚀 Run locally

```bash
# any static server (needed for the lib/*.js files):
python -m http.server 8080
# → http://localhost:8080
```

## 🌍 Deploy on GitHub Pages

```bash
git init && git add . && git commit -m "Day 2/100: Bijoy to Unicode converter (bijoy+unicode, two-way, offline)"
git branch -M main
git remote add origin https://github.com/iamzahirul/day-02-bijoy-unicode-converter.git
git push -u origin main
```

Then: **Settings → Pages → Deploy from branch → main / (root)** → live at `https://iamzahirul.github.io/day-02-bijoy-unicode-converter/`

## 📁 Structure

```
index.html          → UI (dark, Bangla-first, mobile friendly)
lib/base.js         → character classification helpers
lib/bijoy.js        → Bijoy/Sutonny → Unicode map + reordering
lib/unicode.js      → Unicode → Bijoy map + reordering
```

## 🗺️ Roadmap (v2 ideas)

- [ ] Batch file convert (upload `.txt` → download Unicode `.txt`)
- [ ] Support SomewhereIn / Boisakhi fonts (maps already in `lib/`!)
- [ ] Browser extension for one-click convert on any page
- [ ] Microsoft Word macro version for govt offices

## ⚖️ License & Credits

Licensed under **Apache-2.0** (see [LICENSE](LICENSE)).

The character maps and reordering engine are based on the open-source project
**[bangla-converter by Woliul Hasan](https://github.com/woliul/bangla-converter)** (Apache-2.0).
The UI, smart-mode detection, swap/copy workflow and packaging are original work.

---

*Day 2 of 100 — built in public by Rasel [@iamzahirul](https://github.com/iamzahirul)*
