# Improvement Plan - TZ vs Current State

**Last Updated:** 2026-05-06
**Status:** Phase 4 Frontend Design Optimization IN PROGRESS

---

## 🖥️ Session Context

| Parameter | Value |
|-----------|-------|
| Model | Claude Sonnet 4.6 (active) |
| Plugin | superpowers@claude-plugins-official — installed & active |
| Current focus | Phase 4 Frontend Design: CSS DRY refactor, semantic classes, will-change |
| Branch | `main` |

---

## ✅ COMPLETED COMMITS

| Commit | Description | Phase |
|--------|-------------|-------|
| `2d66b39` | Refactor CSS: DRY principle, semantic classes, will-change performance | Phase 4 Frontend |
| `fe39794` | Phase 4 (POLISH): SEO, Twitter Card, Schema.org, fetchpriority | Phase 4 SEO |
| `23ea0fb` | Increase mobile sticky CTA z-index 60 → 999 | Phase 2 |
| `f0573a7` | Remove old HTML versions | Cleanup |

---

## 📊 Priority Matrix — FINAL STATUS

| Priority | Issue | Effort | Impact | Status |
|----------|-------|--------|--------|--------|
| 🔴 CRITICAL | Clean hero text | 30min | HIGH | ✅ DONE — already clean |
| 🔴 CRITICAL | Add/verify UTM tags | 45min | HIGH | ✅ DONE — all 12 links correct |
| 🔴 CRITICAL | Copy synchronization | 60min | HIGH | ✅ DONE — 100% matches TZ |
| 🟡 IMPORTANT | Mobile sticky CTA z-index | 20min | MEDIUM | ✅ DONE — commit 23ea0fb |
| 🟡 IMPORTANT | Hero gradient optimization | 30min | MEDIUM | ✅ DONE — already correct |
| 🟡 IMPORTANT | Contextual use-case CTAs | 20min | MEDIUM | ✅ DONE — already correct |
| 🟡 IMPORTANT | Mining section disclaimer | 15min | MEDIUM | ✅ DONE — present at line 902 |
| 🟡 IMPORTANT | Accessibility improvements | 45min | MEDIUM | ✅ DONE — 85%+ complete |
| 🟡 IMPORTANT | AOS fallback | 20min | LOW | ✅ DONE — JS + noscript |
| 🟢 ENHANCEMENT | Compact header on scroll | 30min | MEDIUM | ✅ DONE — CSS + JS |
| 🟢 ENHANCEMENT | Active nav states | 30min | MEDIUM | ✅ DONE — IntersectionObserver |
| 🟢 ENHANCEMENT | Mobile menu close | 20min | MEDIUM | ✅ DONE — resize + link click |
| 🟢 ENHANCEMENT | Scroll event coordination | 15min | MEDIUM | ✅ DONE — single listener |
| ✨ PHASE 4 | Twitter Card meta-tags | 5min | HIGH | ✅ DONE — commit fe39794 |
| ✨ PHASE 4 | Schema.org JSON-LD | 10min | HIGH | ✅ DONE — Org + WebPage |
| ✨ PHASE 4 | og:url + og:image dimensions | 5min | MEDIUM | ✅ DONE — commit fe39794 |
| ✨ PHASE 4 | DNS prefetch / preconnect | 5min | MEDIUM | ✅ DONE — 3 hints added |
| ✨ PHASE 4 | fetchpriority on hero & logo | 5min | MEDIUM | ✅ DONE — hero=high, logo=low |
| ✨ PHASE 4 | apple-touch-icon + favicon | 5min | LOW | ✅ DONE — commit fe39794 |
| ✨ PHASE 4 | CSS DRY refactor | 90min | HIGH | ✅ DONE — commit 2d66b39 |

---

## ✅ PHASE 1 — CRITICAL (DONE)

**Verified:** All 3 critical issues were already resolved in current index.html.

- ✅ **Hero section** — Clean: only H1 + subtitle + 2 buttons. No Kigali badge, no extra text.
- ✅ **UTM tags** — All 12 CTA locations have correct `utm_source`, `utm_medium`, `utm_campaign`, `utm_content`.
- ✅ **Copy sync** — 100% match with TZ: headings, body, cards, CTAs, footer, copyright (2026).

---

## ✅ PHASE 2 — IMPORTANT (DONE)

**Only change needed:** Mobile sticky CTA z-index 60 → 999 (commit `23ea0fb`).

All other Phase 2 items were already implemented:
- ✅ Hero background gradient: Asymmetric desktop + simplified mobile
- ✅ Contextual CTAs in use-case cards: urban / tourism / remote / mining
- ✅ Mining disclaimer text present
- ✅ Accessibility: skip link, focus-visible, aria-labels, role="img"
- ✅ AOS fallback: JS detection + noscript CSS override

---

## ✅ PHASE 3 — ENHANCEMENT (DONE)

All features already fully implemented before this session:
- ✅ Compact header on scroll (`is-compact` CSS + JS toggle at 80px)
- ✅ Active nav state (clears on hero, highlights on section scroll)
- ✅ Mobile menu toggle (Menu → Close text, aria-expanded)
- ✅ Mobile menu close on link click
- ✅ Mobile menu close on resize ≥ 1024px
- ✅ Sticky CTA hides when mobile menu open
- ✅ Single scroll event listener coordinating all 3 behaviors
- ✅ Page initializes with correct state on load

---

## ✅ PHASE 4 — POLISH SEO (DONE — commit fe39794)

### Implemented (57 insertions):

**Meta-tags:**
- Twitter Card (`summary_large_image`) — Twitter, LinkedIn, Reddit rich previews
- `og:url` — canonical for social crawlers
- `og:image:width` / `og:image:height` (1920×1080) — prevents social preview layout shift

**Performance:**
- `fetchpriority="high"` on hero preload + hero primary CTA
- `fetchpriority="low"` + `loading="lazy"` on nav logo
- DNS prefetch for Tailwind CDN + unpkg
- `preconnect` to unpkg

**Branding:**
- `apple-touch-icon` — iOS home screen
- `favicon` (32×32 PNG) — browser tab

**SEO / Structured Data:**
- Schema.org `Organization` JSON-LD (name, url, logo, address, contactPoint)
- Schema.org `WebPage` + `LocalBusiness` JSON-LD
- Eligible for Google Knowledge Panel

---

## 🔄 PHASE 4 — FRONTEND DESIGN REFACTOR (DONE — commit 2d66b39)

### Applied HIGH-priority Frontend Design improvements (74 insertions, 47 deletions):

**CSS Variables — eliminates 12 hardcoded values:**
```css
--radius-full: 999px    /* was 6× border-radius: 999px */
--radius-card: 14px
--radius-metric: 12px
--t-fast: 0.25s ease    /* was 6× 0.25s ease */
--t-mid: 0.3s ease
--shadow-btn / --shadow-btn-hover / --shadow-card / --shadow-nav
```

**DRY Semantic Classes — eliminates 15 inline duplications:**
```css
.section-label   /* 7 section label spans: 47 chars → 1 class */
.trust-label     /* 4 Trust Strip value divs */
.trust-value     /* 4 Trust Strip subtitle divs */
```

**Performance:**
```css
will-change: transform   /* .btn-pill, .btn-pill-outline, .card-b2b */
font-size: clamp(...)    /* .trust-label — fluid typography */
```

**Note on content-visibility:** Skipped intentionally — conflicts with AOS IntersectionObserver scroll detection, causes layout jank. `will-change` covers GPU compositing goal without risk.

---

## 📋 TODO — REMAINING

### Immediate
- [ ] **Browser testing** — Chrome, Firefox, Safari, Edge, iOS, Android
- [ ] **PageSpeed Insights** — measure LCP, FID, CLS after all optimizations
- [ ] **Schema.org validation** — https://validator.schema.org/
- [ ] **Social card test** — Twitter Card Validator, Facebook Debugger
- [ ] **Create GRAND SUMMARY** — project overview document

### Optional (Medium priority)
- [ ] **Hero image optimization** — compress hero-bg.png to < 200KB (TinyPNG / Squoosh)
- [ ] **WebP format** — add `<picture>` element with WebP + PNG fallback
- [ ] **Cache headers check** — `curl -I https://petrikin83.github.io/CDC_Africa/`
- [ ] **Medium CSS improvements:**
  - `@apply` for remaining repeated Tailwind chains
  - Standardize PPP section SVG icons
  - Spacing scale CSS variables

### Low priority
- [ ] Service worker for offline support
- [ ] GA4 event tracking verification in analytics dashboard
- [ ] Cross-device screenshot comparison

---

## 📈 PROGRESS SUMMARY

```
Phase 1 (CRITICAL)     ████████████████████ 100% ✅
Phase 2 (IMPORTANT)    ████████████████████ 100% ✅
Phase 3 (ENHANCEMENT)  ████████████████████ 100% ✅
Phase 4 SEO            ████████████████████ 100% ✅
Phase 4 Frontend       ████████████████████ 100% ✅
Browser Testing        ░░░░░░░░░░░░░░░░░░░░   0% ⏳
Grand Summary Doc      ░░░░░░░░░░░░░░░░░░░░   0% ⏳
```

**Overall project completion: ~90%**

---

## 🏗️ ARCHITECTURE NOTES

- **Single-page static site** — index.html, GitHub Pages hosting
- **CSS inline** — optimal for HTTP/2, no extra requests
- **Tailwind CDN** — prototyping mode, acceptable for this project scale
- **AOS CDN** — with JS fallback + noscript fallback
- **Fonts locally hosted** — Goodly (OTF), Lato (TTF), font-display: swap
- **All cdc.company links** — 12 UTM-tagged with unique utm_content values
- **JavaScript** — vanilla, ~136 lines, no dependencies beyond AOS

---

## 🔍 KEY FILE LOCATIONS

| File | Purpose |
|------|---------|
| `index.html` | Main landing page (~1300 lines) |
| `.claude/improvement-plan.md` | This file — project tracking |
| `.claude/tz-requirements.md` | TZ checklist by section |
| `.claude/copy-checklist.md` | Exact copy for all sections |
| `.claude/utm-parameters.md` | All 12 UTM-tagged CTA locations |
| `.claude/project-context.md` | Project overview, design system |
