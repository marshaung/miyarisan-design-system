# 妙利散 Miyarisan — Design System

## Company Overview

**妙利散** (Miyarisan) is the official Taiwan distributor of **Miyarisan Pharmaceutical Co., Ltd.** (ミヤリサン製薬株式会社), a Japanese pharmaceutical company with 70+ years of history. The core product is **妙利散® BM** — a medical-grade probiotic (藥字號益生菌) containing the proprietary strain *Clostridium butyricum* MIYAIRI 588 (CBM588).

The brand operates in a **medical/pharmaceutical context**: primary audiences are **physicians and pharmacists** (B2B medical channel), with secondary consumer-facing communication for patients.

## Product

| Product | Description |
|---|---|
| 妙利散® BM | 1g/包 × 42包; 整腸劑；活性宮入菌（芽胞菌）製劑 |
| CBM588 菌株 | *Clostridium butyricum* MIYAIRI 588 — spore-forming, butyrate-producing, acid-resistant |

**Key claims:** 整腸・消化・次世代益生菌製劑 / 70年以上の愛用益生菌 / 日本No.1

## Sources Provided

| Source | Notes |
|---|---|
| Figma file `miyarisan.fig` | Mounted as VFS — file was empty (no frames); not usable |
| GitHub: `marshaung/miyarisan` | Private repo — returned 409; inaccessible |
| GitHub: `marshaung/miyarisan-web` | Single-page `index.html` — main design source (medical info page) |
| GitHub: `marshaung/landing-page` | Private repo — returned 409; inaccessible |
| `uploads/蘭亭黑.zip` | 蘭亭黑 font family (couldn't extract due to CJK path; see Typography) |
| `uploads/妙利散黑.svg` | Logo — black variant |
| `uploads/妙利散紅.svg` | Logo — red/brand variant |
| `uploads/妙利散白.svg` | Logo — white variant |
| `uploads/221011_妙利散.png` | Brand identity square (hot pink gradient + logo) |
| `uploads/260326_首頁初稿_確認版.jpg` | Homepage draft — pink/red landing page layout |
| `uploads/截圖 2026-04-23 中午12.49.24.png` | Dark homepage screenshot — navy background variant |
| `uploads/妙利散產品盒裝.png` | Product box photo (white/red BM box) |

---

## CONTENT FUNDAMENTALS

### Tone & Voice
- **Professional but accessible** — content bridges medical authority (doctors, pharmacies) with consumer understanding
- **Third-person product references**: "妙利散" or "CBM588" — not "我們的產品"
- **Educational-first**: copy leads with science and mechanism, then benefit
- **Measured claims**: careful to distinguish "科學教育" from medical advice; always includes disclaimers
- **No hype, no emoji** — serious pharmaceutical register

### Language
- **Traditional Chinese (繁體中文)** primary; Japanese secondary (origin/heritage context); some English for technical terms (CBM588, pH, ATP, HDAC)
- Scientific terms used directly: *Clostridium butyricum*, butyrate, SCFA, peer-reviewed
- Casing: product names in mixed script 妙利散® BM / MIYARISAN®
- Numbers: Arabic numerals for data (50+年、60–90%、pH 2)

### Copy Examples
- Hero: 「不是所有益生菌，都能在醫療情境下發揮作用」
- Badge: 「醫療級益生菌」「醫療級酪酸菌」
- Section eyebrow: uppercase letter-spaced labels (醫療級定義 / 穩定性數據)
- CTA: 「了解菌株特色 →」「查看研究報告」「了解購買途徑」
- Disclaimers always close sections: 「本頁資訊為科學文獻背景介紹，供衛教參考目的，不構成醫療建議」

### Emoji / Icons
- **No emoji in production UI** — the website uses emoji sparingly as placeholders (🧫🛡️⚡) in mechanism diagrams only
- Icons: text-based, or SVG placeholders; no icon font library observed

---

## VISUAL FOUNDATIONS

### Colors
**Primary brand: 桃紅色 (rose red / hot pink)**
- Brand Red (dark, web): `#8b1a2e` — used as CSS primary red in medical content pages
- Brand Red Mid: `#a82040`
- Brand Red Light: `#c0284f`
- Brand Crimson (packaging/logo): `#C8194B` — extracted from product box and logo gradient
- Brand Hot Pink (logo gradient end): `#E5186E` — the bright magenta end of the logo
- Navy (dark theme bg): `#0B1A35` — deep medical navy for dark homepage variant
- Red Pale (backgrounds): `#fdf2f4`

**Neutral scale:**
- Text primary: `#111827`
- Text 2: `#374151`
- Text 3 (muted): `#6b7280`
- Text 4 (faint): `#9ca3af`
- Border: `#e5e7eb`
- Border 2: `#d1d5db`
- BG: `#ffffff`
- BG Gray: `#f7f8fa`
- BG Gray 2: `#f0f2f5`

**Semantic:**
- Green (success/check): `#16a34a`
- Blue (info/badge): `#2563eb`
- Amber (warning): `#d97706`

### Typography
- **Primary Chinese**: 蘭亭黑 (LanTing Hei) — provided as zip; **substituted with Noto Sans TC** (Google Fonts)
- **Primary Latin**: Inter (Google Fonts)
- **Body**: Noto Sans TC 400/500; line-height 1.9; letter-spacing 0.03–0.04em
- **Display/H1**: weight 900; letter-spacing -0.02em; clamp(32px, 4.5vw, 58px)
- **Eyebrow labels**: 11–12px; weight 700–800; letter-spacing 0.08–0.12em; UPPERCASE
- **Data/numbers**: weight 900; letter-spacing -0.03em; large scale (34–38px)

### Spacing & Layout
- Container max-width: 1100–1200px; centered
- Section padding: 88px vertical / 48px horizontal (desktop); 64px / 24px (mobile)
- Grid: 2-col (feature split), 3-col (pillars/butyrate), 4-col (stats)
- Gap: 24px (cards), 64px (feature splits)

### Corner Radii
- Cards: `--radius: 16px`
- Small elements: `--radius-sm: 10px`
- Micro (badges/pills): `--radius-xs: 6px` or 99px (pill)

### Shadows
- Small: `0 1px 3px rgba(0,0,0,0.06), 0 1px 2px rgba(0,0,0,0.04)`
- Default: `0 4px 16px rgba(0,0,0,0.07), 0 1px 4px rgba(0,0,0,0.04)`
- Large: `0 12px 40px rgba(0,0,0,0.09), 0 4px 12px rgba(0,0,0,0.05)`
- Hover: cards lift 2–3px on translateY(-2px to -3px)

### Backgrounds
- White sections alternate with `#f7f8fa` (light gray) for rhythm
- Dark sections use `#0B1A35` navy with white text (homepage hero)
- No heavy gradients in UI body — gradients reserved for brand identity / logo
- Product logo uses a vibrant hot-pink gradient (crimson → magenta)

### Animation & Interaction
- Transition: `0.18–0.2s` ease on hover (color, background, shadow, transform)
- Cards: lift on hover (`translateY(-2px)`) + shadow increase
- Buttons: `translateY(-1px)` + box-shadow on hover
- Bar charts: `width 1.2–1.3s cubic-bezier(.22,.68,0,1.2)` (spring)
- FAQ accordion: slide open (display toggle, no CSS transition on height)
- Scroll behavior: smooth

### Hover / Press States
- Buttons: darker shade of primary + glow shadow
- Links: color changes to `--red` or `--text`
- Nav links: background pill `#f7f8fa`, color `--text`
- Active nav: `--red` color + `--red-pale` background

### Cards
- Background: white; border: 1px solid `#e5e7eb`; border-radius: 16px
- Shadow: `--shadow-sm` default, `--shadow` on hover
- No colored left-border only cards
- Padding: 32–40px

### Imagery
- Medical/clinical stock photography (laboratory, doctors, microscopy)
- Product box photography (white/red packaging on clean background)
- Brand uses circular pattern motifs (concentric circles in product box design)
- Image aspect ratio: 4:3 common; 16:9 for mobile banners
- No illustration; no hand-drawn elements

### Blur / Transparency
- Navigation: `backdrop-filter: blur(16px)` + `rgba(255,255,255,0.92)` frosted glass
- Sticky nav background: semi-transparent white

---

## ICONOGRAPHY

See assets/ for all logo files.

**Logo variants:**
- `assets/logo-black.svg` — black wordmark (dark backgrounds use white/inverted version)
- `assets/logo-red.svg` — red/brand color wordmark
- `assets/logo-white.svg` — white wordmark (for dark/colored backgrounds)
- `assets/logo-brand.png` — full brand identity square (hot pink gradient + MIYARISAN oval badge + 妙利散® Chinese wordmark)
- `assets/product-box.png` — product box (BM, white/red)
- `assets/homepage-draft.jpg` — homepage layout reference (pink/red theme)
- `assets/homepage-dark.png` — homepage layout reference (dark navy theme)

**Icon system:** No dedicated icon library/font found. The codebase uses:
- Unicode/emoji as lightweight placeholders in mechanism diagrams only
- SVG inline for logos
- No Heroicons, Lucide, or similar CDN icon set found in the codebase

**Recommendation:** Adopt [Lucide](https://lucide.dev) (stroke-based, 1.5px, clean) for any UI icons needed — consistent with the clean, clinical aesthetic. Load via CDN: `https://unpkg.com/lucide@latest`

---

## File Index

```
README.md                    — this file
SKILL.md                     — agent skill definition
colors_and_type.css          — all CSS custom properties (colors, type, spacing)
assets/
  logo-black.svg             — logo black
  logo-red.svg               — logo red
  logo-white.svg             — logo white
  logo-brand.png             — brand identity (pink gradient square)
  product-box.png            — product box photography
  homepage-draft.jpg         — homepage layout reference
  homepage-dark.png          — dark homepage reference
preview/
  colors-brand.html          — brand color swatches
  colors-neutral.html        — neutral + semantic colors
  type-scale.html            — typography scale specimen
  type-body.html             — body text specimens
  spacing-tokens.html        — spacing / radius / shadow tokens
  components-buttons.html    — button variants
  components-badges.html     — badges + pills
  components-cards.html      — card components
  components-nav.html        — navigation bar
  brand-logos.html           — logo display
  brand-product.html         — product photography
ui_kits/
  website/
    README.md                — website UI kit notes
    index.html               — interactive website prototype
```
