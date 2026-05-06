# Mobile Optimization Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Optimize the CDC Africa website for mobile devices with improved spacing, typography, header compaction, and a better sticky CTA using IntersectionObserver.

**Architecture:** Single-file optimization targeting index.html. Changes involve: (1) adding data-hide-sticky-cta attributes to sections where CTA should hide, (2) updating CSS for mobile-first spacing/typography with clamp() values, (3) refactoring sticky CTA from scroll-event listeners to IntersectionObserver for better performance and cleaner logic.

**Tech Stack:** Vanilla JavaScript (IntersectionObserver API), CSS with clamp() for responsive sizing, Tailwind CSS for utility classes.

---

## File Structure

**Modified:**
- `index.html` — Contains all HTML, CSS (in `<style>` tags), and JavaScript (in `<script>` tags)

All changes are to a single file.

---

## Task 1: Add data-hide-sticky-cta Attributes to Sections

**Files:**
- Modify: `index.html:607` (hero section)
- Modify: `index.html:897` (extractive/mining section)
- Modify: `index.html:983` (technology section)
- Modify: `index.html:1034` (ppp section)
- Modify: `index.html:1130` (footer section)

- [ ] **Step 1: Add data-hide-sticky-cta to hero section**

Find the hero section starting at line 607 and update it:

```html
<!-- Before -->
<section id="hero" class="hero-parallax min-h-[88vh] md:min-h-screen relative flex flex-col justify-center items-center pt-24 pb-16">

<!-- After -->
<section id="hero" class="hero-parallax min-h-[88vh] md:min-h-screen relative flex flex-col justify-center items-center pt-24 pb-16" data-hide-sticky-cta>
```

- [ ] **Step 2: Add data-hide-sticky-cta to extractive/mining section**

Find the extractive section starting at line 897 and update it:

```html
<!-- Before -->
<section id="extractive" class="py-20 md:py-24 dark-engineering-bg relative border-y border-[#ff751f]/30">

<!-- After -->
<section id="extractive" class="py-20 md:py-24 dark-engineering-bg relative border-y border-[#ff751f]/30" data-hide-sticky-cta>
```

- [ ] **Step 3: Add data-hide-sticky-cta to technology section**

Find the technology section starting at line 983 and update it:

```html
<!-- Before -->
<section id="technology" class="py-16 md:py-20 bg-pure-white border-b border-gray-200">

<!-- After -->
<section id="technology" class="py-16 md:py-20 bg-pure-white border-b border-gray-200" data-hide-sticky-cta>
```

- [ ] **Step 4: Add data-hide-sticky-cta to ppp section**

Find the ppp section starting at line 1034 and update it:

```html
<!-- Before -->
<section id="ppp" class="py-16 md:py-20 bg-stone">

<!-- After -->
<section id="ppp" class="py-16 md:py-20 bg-stone" data-hide-sticky-cta>
```

- [ ] **Step 5: Add data-hide-sticky-cta to footer section**

Find the footer section starting at line 1130 and update it:

```html
<!-- Before -->
<footer id="contact" class="bg-graphite pt-16 pb-8">

<!-- After -->
<footer id="contact" class="bg-graphite pt-16 pb-8" data-hide-sticky-cta>
```

- [ ] **Step 6: Commit changes**

```bash
git add index.html
git commit -m "feat: add data-hide-sticky-cta attributes to sections for sticky CTA control"
```

---

## Task 2: Update Mobile Header Compaction CSS

**Files:**
- Modify: `index.html:124-141` (site-nav and logo styles)

- [ ] **Step 1: Update is-compact padding**

Find the `.site-nav.is-compact` styles and update:

```css
/* Before */
.site-nav.is-compact {
    padding-top: 0.65rem;
    padding-bottom: 0.65rem;
    box-shadow: var(--shadow-nav);
}

/* After */
.site-nav.is-compact {
    padding-top: 0.75rem;
    padding-bottom: 0.75rem;
    box-shadow: var(--shadow-nav);
}
```

- [ ] **Step 2: Update logo height for compact nav**

Find the `.site-nav.is-compact .brand-logo` style and update:

```css
/* Before */
.site-nav.is-compact .brand-logo {
    height: 2rem;
}

/* After */
.site-nav.is-compact .brand-logo {
    height: 34px;
}
```

- [ ] **Step 3: Update logo text size for compact nav**

The `.site-nav.is-compact .logo-text-nav` is already at 26px, which is fine for mobile. No change needed. Verify it stays at 26px.

- [ ] **Step 4: Add mobile menu button compactness in media query**

Find the media query section for mobile (around line 416 in the style tag) and add/update:

```css
@media (max-width: 640px) {
    .site-nav {
        padding: 0.75rem 1.5rem;
    }
    
    .brand-logo {
        height: 32px;
    }
    
    .logo-text-nav {
        font-size: 24px;
    }
    
    #mobileMenuButton {
        padding: 0.5rem 1rem;
        font-size: 10px;
    }
}
```

- [ ] **Step 5: Commit changes**

```bash
git add index.html
git commit -m "feat: compact mobile header with optimized padding and logo sizing"
```

---

## Task 3: Update Trust Strip Optimization CSS

**Files:**
- Modify: `index.html:353-367` (trust strip styles)
- Update: HTML trust strip section (around line 728-770)

- [ ] **Step 1: Update trust-label font size with clamp**

Find the `.trust-label` style and update:

```css
/* Before */
.trust-label {
    color: var(--cdc-white);
    font-family: 'Goodly', Arial, Helvetica, sans-serif;
    font-size: clamp(1.5rem, 2.5vw, 1.875rem);
    line-height: 1;
}

/* After */
.trust-label {
    color: var(--cdc-white);
    font-family: 'Goodly', Arial, Helvetica, sans-serif;
    font-size: clamp(1.5rem, 3.2vw, 2.25rem);
    line-height: 1.1;
}
```

- [ ] **Step 2: Add mobile-specific trust strip padding**

Add a new media query at the end of the style section:

```css
@media (max-width: 640px) {
    #why-africa {
        padding-top: 2.25rem;
        padding-bottom: 2.25rem;
    }
    
    .trust-label {
        font-size: 1.5rem;
        margin-bottom: 0.5rem;
    }
    
    .trust-value {
        font-size: 9px;
    }
}
```

- [ ] **Step 3: Update trust strip in HTML for better spacing**

Find the "Why Africa" section starting around line 726 and ensure the padding classes use mobile-optimized values. The section should already have `py-16 md:py-20`, which translates to 4rem on mobile (64px) and 5rem on desktop. We'll make this `py-9 md:py-20` (2.25rem on mobile = 36px).

Find and update:

```html
<!-- Before -->
<section id="why-africa" class="py-16 md:py-20 bg-stone border-b border-gray-200">

<!-- After -->
<section id="why-africa" class="py-9 md:py-20 bg-stone border-b border-gray-200">
```

- [ ] **Step 4: Commit changes**

```bash
git add index.html
git commit -m "feat: optimize trust strip spacing and typography for mobile"
```

---

## Task 4: Update Typography with clamp() Values

**Files:**
- Modify: `index.html:46-500` (style section with typography rules)

- [ ] **Step 1: Update section-title sizing with clamp**

Find or add section-title styling to use clamp:

```css
.section-title {
    font-size: clamp(2.5rem, 10.5vw, 3.25rem);
    line-height: 1.15;
    font-family: 'Goodly', Arial, Helvetica, sans-serif;
}
```

If `.section-title` doesn't exist, add it. If it does, update the font-size to use clamp.

- [ ] **Step 2: Update body typography for mobile**

Add or update body text styling in the mobile media query:

```css
@media (max-width: 640px) {
    body {
        font-size: 1.0625rem;
        line-height: 1.65;
    }
    
    p {
        font-size: 1.0625rem;
        line-height: 1.65;
    }
    
    .card-b2b {
        font-size: 0.96875rem;
    }
}
```

- [ ] **Step 3: Add heading size hierarchy**

Add h2 and h3 sizing rules:

```css
h2 {
    font-size: clamp(2rem, 8vw, 3rem);
}

h3 {
    font-size: clamp(1.25rem, 5vw, 1.75rem);
}

@media (max-width: 640px) {
    h2 {
        font-size: 1.75rem;
    }
    
    h3 {
        font-size: 1.1875rem;
    }
}
```

- [ ] **Step 4: Commit changes**

```bash
git add index.html
git commit -m "feat: implement responsive typography with clamp() values"
```

---

## Task 5: Standardize Section Spacing

**Files:**
- Modify: `index.html:668, 726, 772, 897, 983, 1034, 1130` (various sections)

- [ ] **Step 1: Update about section padding**

Find the about section (line 668) and update:

```html
<!-- Before -->
<section id="about" class="py-14 md:py-20 bg-pure-white border-b border-gray-200">

<!-- After -->
<section id="about" class="py-14 md:py-20 bg-pure-white border-b border-gray-200">
```

No change needed; py-14 (3.5rem = 56px) on mobile is acceptable.

- [ ] **Step 2: Update use-cases section spacing**

Find the use-cases section (line 772) and ensure it has:

```html
<section id="use-cases" class="py-14 md:py-20 bg-pure-white">
```

This is good as-is (56px on mobile).

- [ ] **Step 3: Update extractive section spacing**

Find the extractive section (line 897) and update:

```html
<!-- Before -->
<section id="extractive" class="py-20 md:py-24 dark-engineering-bg relative border-y border-[#ff751f]/30" data-hide-sticky-cta>

<!-- After -->
<section id="extractive" class="py-16 md:py-24 dark-engineering-bg relative border-y border-[#ff751f]/30" data-hide-sticky-cta>
```

Changes py-20 (80px) to py-16 (64px) on mobile for better spacing.

- [ ] **Step 4: Update technology section spacing**

Find the technology section (line 983) and ensure it stays:

```html
<section id="technology" class="py-16 md:py-20 bg-pure-white border-b border-gray-200" data-hide-sticky-cta>
```

This is good (56px on mobile).

- [ ] **Step 5: Update ppp section spacing**

Find the ppp section (line 1034) and ensure it stays:

```html
<section id="ppp" class="py-16 md:py-20 bg-stone" data-hide-sticky-cta>
```

This is good (56px on mobile).

- [ ] **Step 6: Update footer spacing**

Find the footer (line 1130) and update:

```html
<!-- Before -->
<footer id="contact" class="bg-graphite pt-16 pb-8" data-hide-sticky-cta>

<!-- After -->
<footer id="contact" class="bg-graphite pt-14 pb-8 md:pt-16 md:pb-8" data-hide-sticky-cta>
```

Changes pt-16 (64px) to pt-14 (56px) on mobile.

- [ ] **Step 7: Commit changes**

```bash
git add index.html
git commit -m "feat: standardize section padding across mobile and desktop breakpoints"
```

---

## Task 6: Update Hero Background Overlay

**Files:**
- Modify: `index.html:197-206` (hero-parallax styles)

- [ ] **Step 1: Soften hero background overlay**

Find the `.hero-parallax` style and update the gradients:

```css
/* Before */
.hero-parallax {
    background-image:
        radial-gradient(circle at 74% 36%, rgba(255,117,31,0.08), transparent 34%),
        linear-gradient(90deg, rgba(46,46,46,0.88) 0%, rgba(46,46,46,0.76) 34%, rgba(46,46,46,0.34) 64%, rgba(46,46,46,0.48) 100%),
        linear-gradient(to bottom, rgba(46,46,46,0.28) 0%, rgba(46,46,46,0.54) 58%, rgba(46,46,46,0.90) 100%),
        url('./hero-bg.png');
    background-attachment: fixed;
    background-size: cover;
    background-position: center right;
}

/* After */
.hero-parallax {
    background-image:
        radial-gradient(circle at 74% 36%, rgba(255,117,31,0.12), transparent 34%),
        radial-gradient(circle at 28% 70%, rgba(255,255,255,0.04), transparent 28%),
        linear-gradient(90deg, rgba(46,46,46,0.72) 0%, rgba(46,46,46,0.62) 34%, rgba(46,46,46,0.26) 64%, rgba(46,46,46,0.38) 100%),
        linear-gradient(to bottom, rgba(46,46,46,0.18) 0%, rgba(46,46,46,0.44) 58%, rgba(46,46,46,0.82) 100%),
        url('./hero-bg.png');
    background-attachment: fixed;
    background-size: cover;
    background-position: center right;
}
```

This softens the overlay by:
- Increasing the orange accent radial gradient opacity (0.08 → 0.12) for more prominence
- Adding a subtle white radial gradient for depth
- Reducing the linear gradient opacity slightly to make the background image more visible

- [ ] **Step 2: Commit changes**

```bash
git add index.html
git commit -m "feat: soften hero background overlay with improved gradient composition"
```

---

## Task 7: Implement IntersectionObserver for Sticky CTA

**Files:**
- Modify: `index.html:384-420` (CSS for mobile-sticky-cta)
- Modify: `index.html:1206-1215` (JavaScript updateStickyCta function)
- Modify: `index.html:1297-1315` (scroll and resize listeners)

- [ ] **Step 1: Update sticky CTA animation timing**

Find the `.mobile-sticky-cta` CSS and update:

```css
/* Before */
.mobile-sticky-cta {
    display: none;
    opacity: 0;
    transform: translateY(16px);
    pointer-events: none;
    transition: opacity var(--t-fast), transform var(--t-fast);
}

.mobile-sticky-cta.is-visible {
    opacity: 1;
    transform: translateY(0);
    pointer-events: auto;
}

/* After */
.mobile-sticky-cta {
    display: none;
    opacity: 0;
    transform: translateY(16px);
    pointer-events: none;
    transition: opacity 420ms cubic-bezier(0.4, 0, 0.2, 1), transform 420ms cubic-bezier(0.4, 0, 0.2, 1);
    will-change: opacity, transform;
}

.mobile-sticky-cta.is-visible {
    opacity: 1;
    transform: translateY(0);
    pointer-events: auto;
}
```

- [ ] **Step 2: Update mobile media query for sticky CTA**

Find the mobile media query section (around line 416) and update the sticky CTA styles:

```css
@media (max-width: 640px) {
    .mobile-sticky-cta {
        display: block;
        position: fixed;
        bottom: 1rem;
        left: 1rem;
        right: 1rem;
        z-index: 40;
        border-radius: var(--radius-full);
        padding: 0.875rem 1.25rem;
        font-size: 0.875rem;
        box-shadow: var(--shadow-btn);
    }
}
```

- [ ] **Step 3: Replace scroll-based sticky CTA logic with IntersectionObserver**

Find the JavaScript section starting at line 1193. Locate the `updateStickyCta` function (around line 1206) and replace the entire sticky CTA logic:

Replace this:
```javascript
const updateStickyCta = () => {
    if (!mobileStickyCta) return;

    const shouldShow =
        window.innerWidth <= 640 &&
        window.scrollY > window.innerHeight * 0.55 &&
        !isMobileMenuOpen;

    mobileStickyCta.classList.toggle('is-visible', shouldShow);
};
```

With this:
```javascript
const initStickyCtaObserver = () => {
    if (!mobileStickyCta || window.innerWidth > 640) return;
    
    const hiddenSections = document.querySelectorAll('[data-hide-sticky-cta]');
    const observerOptions = {
        root: null,
        rootMargin: '0px',
        threshold: 0
    };
    
    const observerCallback = (entries) => {
        let shouldHide = false;
        
        entries.forEach(entry => {
            if (entry.target.hasAttribute('data-hide-sticky-cta') && entry.isIntersecting) {
                shouldHide = true;
            }
        });
        
        const isVisible = !shouldHide && !isMobileMenuOpen;
        mobileStickyCta.classList.toggle('is-visible', isVisible);
    };
    
    const observer = new IntersectionObserver(observerCallback, observerOptions);
    hiddenSections.forEach(section => observer.observe(section));
};

const updateStickyCta = () => {
    // No-op: IntersectionObserver handles visibility
};
```

- [ ] **Step 4: Initialize IntersectionObserver on load and resize**

Find where `updateStickyCta()` is called initially (around line 1313) and the resize listener (around line 1303), then update:

Replace:
```javascript
window.addEventListener('resize', () => {
    if (window.innerWidth >= 1024) {
        closeMobileMenu();
    }

    updateNav();
    updateStickyCta();
    updateActiveNav();
});

updateNav();
updateStickyCta();
updateActiveNav();
```

With:
```javascript
let stickyCtaObserver = null;

window.addEventListener('resize', () => {
    if (window.innerWidth >= 1024) {
        closeMobileMenu();
    }

    updateNav();
    updateActiveNav();
    
    if (window.innerWidth <= 640 && !stickyCtaObserver) {
        initStickyCtaObserver();
    }
});

updateNav();
updateActiveNav();

if (window.innerWidth <= 640) {
    initStickyCtaObserver();
}
```

Also remove the old `updateStickyCta()` call from the scroll listener (around line 1299):

```javascript
/* Before */
window.addEventListener('scroll', () => {
    updateNav();
    updateStickyCta();
    updateActiveNav();
});

/* After */
window.addEventListener('scroll', () => {
    updateNav();
    updateActiveNav();
});
```

- [ ] **Step 5: Commit changes**

```bash
git add index.html
git commit -m "feat: replace scroll-based sticky CTA with IntersectionObserver for better performance"
```

---

## Task 8: Test Mobile Optimization

**Files:**
- Test: `index.html` (open in browser and test on mobile viewport)

- [ ] **Step 1: Open the site in a browser**

Start a local HTTP server (if not already running):

```bash
python -m http.server 8000
```

Then open `http://localhost:8000` in your browser.

- [ ] **Step 2: Test mobile viewport on desktop browser**

Open DevTools (F12), toggle device toolbar (Ctrl+Shift+M or Cmd+Shift+M), and set viewport to 375px width (iPhone SE).

- [ ] **Step 3: Verify header compaction**

Scroll down and verify:
- Nav padding changes from 4px to ~12px (more compact)
- Logo height is 34px in compact state
- Menu button text is appropriately sized

- [ ] **Step 4: Verify sticky CTA behavior**

Scroll through sections and verify sticky CTA:
- Does NOT appear when hero section is visible
- Does NOT appear when in mining (extractive), technology, ppp, or footer sections
- Appears smoothly when scrolling past hero into "about" section
- Disappears smoothly when scrolling into sections marked with data-hide-sticky-cta
- Animation duration feels right (~420ms)

- [ ] **Step 5: Verify trust strip spacing**

Scroll to "Why Africa" section and verify:
- Padding is reduced on mobile (36px instead of 64px)
- Title text size is approximately 24px
- Subtitle is appropriately sized

- [ ] **Step 6: Verify typography**

Check various sections:
- Section titles use responsive sizing with clamp()
- Body text is 17px with 1.65 line-height
- Headings are appropriately sized for mobile

- [ ] **Step 7: Verify section spacing**

Scroll through all sections and verify consistent spacing:
- Most sections have 56px padding (py-14)
- Extractive section has 64px padding (py-16)
- Footer has 56px top padding
- Spacing feels balanced on mobile

- [ ] **Step 8: Verify hero background**

Check hero section:
- Background image is visible (not too dark)
- Overlays are softer (structure visible, text readable)
- Orange accent is visible

- [ ] **Step 9: Test mobile menu**

Verify sticky CTA hides when mobile menu is open.

- [ ] **Step 10: Test at different breakpoints**

Test at:
- 375px (mobile)
- 640px (sm breakpoint)
- 768px (md breakpoint)
- 1024px (lg breakpoint)

Verify responsive behavior across all breakpoints.

- [ ] **Step 11: Check performance (DevTools Lighthouse)**

Run Lighthouse audit and verify:
- No JavaScript errors in console
- Performance score remains good
- No layout shifts

---

## Self-Review Checklist

**Spec Coverage:**
- ✅ Task 1: data-hide-sticky-cta on hero, mining, technology, ppp, footer
- ✅ Task 2: Mobile header padding 12px, logo height 34px, menu button compact
- ✅ Task 3: Trust strip padding 18px, title 24px, subtitle 9px
- ✅ Task 4: Typography with clamp() values for responsive sizing
- ✅ Task 5: Section spacing standardization (56px normal, 64px extractive, etc.)
- ✅ Task 6: Hero background softer overlay with improved gradients
- ✅ Task 7: IntersectionObserver for sticky CTA with 420ms animation
- ✅ Task 8: Mobile testing at various breakpoints and scenarios

**Placeholder Scan:**
- ✅ No TBD, TODO, or implement-later language
- ✅ All code steps include actual CSS/JS
- ✅ All commands with expected output
- ✅ No "similar to Task N" references
- ✅ No unspecified error handling

**Type/Property Consistency:**
- ✅ data-hide-sticky-cta used consistently across all sections
- ✅ CSS variable names consistent (--cdc-orange, --t-fast, etc.)
- ✅ Animation timing consistent (420ms)
- ✅ Tailwind classes consistent (py-14, py-16, py-20)

---

## Execution Notes

- **Single file:** All changes are to `index.html` — no file creation needed
- **Atomic commits:** Each task produces a logical commit
- **Testing:** Step 8 covers comprehensive mobile testing
- **No dependencies:** Tasks 1-7 can be done in any order; Task 8 must be last
- **Rollback:** Each commit is independently revertible if needed
