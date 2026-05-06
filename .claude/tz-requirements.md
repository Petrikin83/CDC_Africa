# TZ Requirements Checklist

## Page Sections

- [x] Header / Navigation
- [x] Hero Section
- [x] Trust Strip
- [x] About CDC Africa
- [x] Why Africa
- [x] Use Cases (4 cards)
- [x] Extractive Sector / Mining
- [x] Technology
- [x] PPP & Economic Value
- [x] Footer / Final CTA

---

## 1. Header / Navigation

### Requirements
- [ ] Fixed header at top
- [ ] Left side: CDC logo + separator + "AFRICA" text
- [ ] Right side links:
  - [ ] About
  - [ ] Why Africa
  - [ ] Use Cases
  - [ ] Mining
  - [ ] PPP / ROI
  - [ ] Global Capabilities → (to cdc.company)
- [ ] Compact header on scroll (less padding, smaller logo, shadow)
- [ ] Mobile menu with "Menu" button
- [ ] Active nav state (but NOT on hero)
- [ ] All external links with `target="_blank" rel="noopener noreferrer"`

### Links
- Global Capabilities: `https://cdc.company` + UTM tags

---

## 2. Hero Section

### Layout
- [ ] Desktop: Text left-aligned, background image visible on right
- [ ] Mobile/Tablet: Centered text, darker overlay
- [ ] Minimum height: min-h-screen

### Copy (EXACT - no modifications)
```
Infrastructure That
Moves Economies.

Ropeway infrastructure for African cities, tourism destinations, 
cable bridges, remote regions and mining operations — powered by 
CDC global engineering.

[Explore CDC Global Capabilities] [View African Use Cases]
```

### Critical Requirements
- ❌ NO Kigali plaque in hero
- ❌ NO "CDC Africa brings..." text in hero
- ❌ NO "We are in Africa. One partner..." in hero
- ✅ Clean, premium, uncluttered
- ✅ Image should be visible (not too dark overlay)

### Background Gradient
```css
Desktop:
linear-gradient(90deg, 
    rgba(46,46,46,0.88) 0%, 
    rgba(46,46,46,0.76) 34%, 
    rgba(46,46,46,0.34) 64%, 
    rgba(46,46,46,0.48) 100%),
linear-gradient(to bottom, rgba(46,46,46,0.28) 0%, rgba(46,46,46,0.54) 58%, rgba(46,46,46,0.90) 100%)

Mobile:
radial-gradient(circle at 50% 28%, rgba(255,117,31,0.10), transparent 34%),
linear-gradient(to bottom, rgba(46,46,46,0.66), rgba(46,46,46,0.94))
```

### Buttons
- [ ] Primary: "Explore CDC Global Capabilities"
- [ ] Secondary: "View African Use Cases" (scroll to #use-cases)
- [ ] Both fullwidth on mobile, side-by-side on desktop

---

## 3. Trust Strip / Proof Bar

### Copy (EXACT format)
```
Kigali-Based
Regional Hub

Global CDC
Engineering Access

PPP-Ready
Infrastructure Logic

4 Sectors
Urban • Tourism • Remote • Mining
```

### Requirements
- [ ] Dark background (graphite)
- [ ] 4 columns on desktop, 2x2 grid on mobile
- [ ] Compact, no extra padding
- [ ] Acts as proof bar (moves Kigali context from hero)

---

## 4. About / CDC Africa

### Heading
```
The African hub for CDC's global ropeway engineering.
```

### Body Text
```
CDC Africa is the regional hub bringing CDC's global engineering 
capability to African infrastructure projects. From Kigali, we help 
governments, developers, investors and industrial operators identify 
where ropeway systems can create real economic value.
```

### Key Message Card
```
One regional partner for high-value infrastructure opportunities.
```

### Bullet Points (EXACT)
```
✓ Local presence in Kigali, Rwanda
✓ Access to CDC's global engineering platform
✓ Support for governments, PPPs, developers and investors
✓ Urban, tourism, remote access, cable bridges and mining applications
```

### CTA
- [ ] "Explore the CDC global platform →" (to cdc.company + UTM)

### Layout
- [ ] 2 columns on desktop (text left, card right)
- [ ] Stack on mobile

---

## 5. Why Africa

### Heading
```
Africa's growth requires new infrastructure models.
```

### Body Text
```
Across the continent, cities and regions are growing faster than 
traditional infrastructure can keep up. Ropeway transport creates a 
complementary mobility layer that can bypass congestion, reduce land 
use, accelerate deployment and connect difficult terrain.
```

### Four Cards (EXACT copy)

**Card 1: Urban Pressure**
```
Fast-growing cities need mobility systems that can expand 
without massive road construction.
```

**Card 2: Complex Terrain**
```
Hills, mountains, valleys and protected landscapes require 
infrastructure that adapts to geography.
```

**Card 3: Limited Access**
```
Islands, remote regions, rivers and isolated communities need 
reliable links to unlock value.
```

**Card 4: Economic Growth**
```
Better mobility supports jobs, tourism, productivity, integration 
and investment attraction.
```

---

## 6. Use Cases (4 Cards)

### Section Heading
```
What are you planning?
```

### Section Subtitle
```
CDC Africa helps route different project opportunities toward the 
right global CDC capability.
```

### Card 1: Urban Cableways

- **Label:** Cities
- **Heading:** Urban Cableways
- **Placeholder Text:** Urban Corridor / Ropeway System
- **Body:** For capitals and fast-growing cities facing congestion, limited road capacity and difficult land acquisition.
- **CTA:** Explore urban capabilities → (utm_content=usecase_urban)

### Card 2: Mountain & Park Access

- **Label:** Tourism
- **Heading:** Mountain & Park Access
- **Placeholder Text:** Kilimanjaro-Type / Mountain Access
- **Body:** For Kilimanjaro-type mountain destinations, national parks, resorts and premium natural sites where access must grow without damaging the landscape.
- **CTA:** Explore tourism capabilities → (utm_content=usecase_tourism)

**IMPORTANT:** Use "Kilimanjaro-type" — NOT as confirmed project, just as example

### Card 3: Cable Bridges & Remote Access

- **Label:** Connectivity
- **Heading:** Cable Bridges & Remote Access
- **Placeholder Text:** Cable Bridges / Remote Access
- **Body:** For Madagascar-type island regions, valleys, rivers and isolated communities where roads are slow, costly or difficult to build.
- **CTA:** Explore remote access capabilities → (utm_content=usecase_remote)

**IMPORTANT:** Use "Madagascar-type" — NOT as confirmed project, just as example

### Card 4: Industrial Logistics

- **Label:** Mining
- **Heading:** Industrial Logistics
- **Placeholder Text:** Material Transport / Mining System
- **Body:** For mining operators and industrial sites requiring heavy-load material transport across terrain unreachable by conventional systems.
- **CTA:** Explore mining capabilities → (utm_content=usecase_mining)

### Layout
- [ ] 4 columns on large desktop
- [ ] 2 columns on tablet
- [ ] 1 column on mobile
- [ ] Images are placeholders, not photos

---

## 7. Extractive Sector / Mining

### Section Heading
```
Material Ropeways & Cable Cranes
for Mining Operations.
```

### Subheading
```
Heavy-load ropeway systems can move bulk materials across extreme 
terrain, reduce dependence on haul roads and support mining operations 
as they evolve.
```

### Four Metrics (EXACT)

```
40T+
Capacity Potential

Up to 3 km
Span Between Supports

Up to 60°
Slope Operation

Year-Round
All-Weather Operation
```

### Disclaimer (MUST INCLUDE)
```
Technical parameters depend on project configuration, terrain, 
system type and operational requirements.
```

### Four Feature Cards (EXACT copy)

**Card 1: No Haul Roads**
```
Bulk transport in a single pass with reduced dependence on road 
clearing and heavy ground infrastructure.
```

**Card 2: Fewer Towers, Lower Impact**
```
Long spans can reduce the number of supports, lower cost drivers 
and minimize terrain impact.
```

**Card 3: Extreme Terrain & Conditions**
```
Designed for terrain unreachable by conventional systems, including 
high altitude, severe wind and extreme cold conditions.
```

**Card 4: Modular & Relocatable**
```
Systems can be adapted and relocated as mining operations evolve 
and extraction zones shift.
```

### CTA
- [ ] "Explore CDC Mining Capabilities" (utm_content=mining_cta)

---

## 8. Technology

### Heading
```
Proven technology.
Applied to African realities.
```

### Body Text
```
CDC Africa is the regional access point to CDC's international 
ropeway engineering platform — combining local project context 
with global technical capability, safety thinking, feasibility 
expertise and implementation experience.
```

### Three Feature Cards (EXACT copy)

**Card 1: AirBridge® Technology**
```
Advanced aerial transport technology for passenger and cargo movement 
across cities, terrain barriers and infrastructure gaps.
```

**Card 2: CDC Lab**
```
Continuous innovation, testing and adaptation for climate conditions, 
terrain challenges and operational realities.
```

**Card 3: Project Structuring**
```
Support for feasibility, route logic, technical validation, financial 
modeling and PPP-ready project development.
```

### CTA
- [ ] "Explore CDC Global" (utm_content=technology_cta)

---

## 9. PPP & Economic Value

### Heading
```
Built for infrastructure conversations.
```

### Body Text
```
CDC Africa supports discussions around public-private partnerships, 
concessions, government-funded projects and blended finance opportunities.
```

### Four Value Cards (EXACT copy)

**Card 1: Lower CAPEX Potential**
```
Reduced land acquisition, simplified construction and fewer heavy 
civil works.
```

**Card 2: Faster Time to Impact**
```
Earlier project activation compared with slow, capital-intensive 
infrastructure models.
```

**Card 3: Revenue Generation**
```
Passenger fares, tourism ticketing, commercial integration and 
concession structures.
```

**Card 4: Scalable Capacity**
```
Modular infrastructure for phased growth and demand-based planning.
```

### Final Message
```
More than transport — economic growth.

CDC Africa projects are designed to support job creation, tourism 
development, urban productivity, regional connectivity and investment 
attraction.

We don't just move people — we enable economic ecosystems.
```

### CTA
- [ ] "Explore PPP-Ready Infrastructure Models" (utm_content=ppp_cta)

---

## 10. Footer / Final CTA

### Heading
```
Ready to explore CDC's global ropeway platform?
```

### Body Text
```
Continue to CDC Global to review technology background, engineering 
capabilities, system applications and international project expertise.
```

### Buttons
- [ ] "Explore CDC Global Capabilities" (utm_content=footer_primary_cta)
- [ ] "Contact CDC Africa" (mailto:info@cdc.africa)

### Contact Line (ONE LINE)
```
Kigali, Rwanda • info@cdc.africa
```

### Bottom Copyright
```
CDC Africa — Infrastructure for Economic Growth in Africa
© 2026 CDC Africa. Kigali, Rwanda.
```

---

## JavaScript / UX Behavior

- [ ] **Compact header on scroll:** Reduce padding, logo height, add shadow
- [ ] **Active nav state:** Highlight current section (NOT on hero)
- [ ] **Mobile menu:** Toggle open/close, close on link click
- [ ] **Mobile sticky CTA:** Show "Explore CDC Global" after scrolling past hero (>55% viewport height)
- [ ] **AOS fallback:** If CDN fails, show content without animations
- [ ] **noscript fallback:** Make AOS content visible if JS disabled

---

## Accessibility Requirements

- [ ] `aria-label` on nav
- [ ] `alt` text on all images
- [ ] `role="img"` + `aria-label` on placeholder visuals
- [ ] `focus-visible` outline on links and buttons (2px orange, 4px offset)
- [ ] Skip link to main content
- [ ] `prefers-reduced-motion` media query support

### Focus Style (EXACT)
```css
a:focus-visible,
button:focus-visible {
    outline: 2px solid #ff751f;
    outline-offset: 4px;
    border-radius: 999px;
}
```

---

## Meta & Technical

- [ ] `<meta name="viewport" content="width=device-width, initial-scale=1.0">`
- [ ] `<meta name="description" content="...">`
- [ ] `<meta property="og:title" content="...">`
- [ ] `<meta property="og:image" content="./hero-bg.png">`
- [ ] All external links: `target="_blank" rel="noopener noreferrer"`
- [ ] All cdc.company links: Include UTM parameters
- [ ] Preload hero image: `<link rel="preload" as="image" href="./hero-bg.png">`

---

## Assets

- [ ] **Logo:** ./Logo_CDC_new.png
- [ ] **Hero Background:** ./hero-bg.png
- [ ] **Placeholder Cards:** Use schematic/engineering visuals, NOT random photos
- [ ] **Fonts:** Goodly (OTF), Lato (TTF) — locally hosted

---

## What NOT to Do

❌ Don't turn page into long corporate site
❌ Don't overload hero with text
❌ Don't claim Kilimanjaro/Madagascar as confirmed projects
❌ Don't use random Unsplash photos for cards
❌ Don't make it too tourist-focused
❌ Don't use startup-style branding
❌ Don't make all CTAs identical
❌ Don't hide important content behind animations
❌ Don't create footer with excessive whitespace
❌ Don't place Kigali badge in hero
❌ Don't overuse orange text in first screen
