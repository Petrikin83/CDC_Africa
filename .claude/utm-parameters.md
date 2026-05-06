# UTM Parameters Configuration

**All external links to `cdc.company` MUST include UTM parameters for analytics tracking.**

---

## UTM Structure

### Base URL
```
https://cdc.company
```

### Full URL Format
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=[SPECIFIC_VALUE]
```

### UTM Parameters (Fixed)
- `utm_source` = `cdc_africa`
- `utm_medium` = `landing`
- `utm_campaign` = `africa_gateway`
- `utm_content` = **Varies by location** (see below)

---

## All CTA Locations with utm_content Values

### Navigation Bar

**Location:** Header menu → "Global Capabilities" link

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=nav_cta
```

**Text:** Global Capabilities

**Attributes:**
```html
target="_blank" rel="noopener noreferrer"
```

---

### Hero Section

**Location 1: Primary CTA Button**

**utm_content:** `hero_primary_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=hero_primary_cta
```

**Text:** Explore CDC Global Capabilities

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=hero_primary_cta"
   target="_blank"
   rel="noopener noreferrer"
   class="btn-pill">
   Explore CDC Global Capabilities
</a>
```

---

### About Section

**Location: Text CTA at end of About**

**utm_content:** `about_text_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=about_text_cta
```

**Text:** Explore the CDC global platform →

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=about_text_cta"
   target="_blank"
   rel="noopener noreferrer"
   class="text-link-arrow">
   Explore the CDC global platform →
</a>
```

---

### Use Cases Section

#### Card 1: Urban Cableways

**utm_content:** `usecase_urban`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_urban
```

**Text:** Explore urban capabilities →

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_urban"
   target="_blank"
   rel="noopener noreferrer"
   class="text-link-arrow">
   Explore urban capabilities →
</a>
```

---

#### Card 2: Mountain & Park Access

**utm_content:** `usecase_tourism`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_tourism
```

**Text:** Explore tourism capabilities →

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_tourism"
   target="_blank"
   rel="noopener noreferrer"
   class="text-link-arrow">
   Explore tourism capabilities →
</a>
```

---

#### Card 3: Cable Bridges & Remote Access

**utm_content:** `usecase_remote`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_remote
```

**Text:** Explore remote access capabilities →

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_remote"
   target="_blank"
   rel="noopener noreferrer"
   class="text-link-arrow">
   Explore remote access capabilities →
</a>
```

---

#### Card 4: Industrial Logistics

**utm_content:** `usecase_mining`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_mining
```

**Text:** Explore mining capabilities →

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=usecase_mining"
   target="_blank"
   rel="noopener noreferrer"
   class="text-link-arrow">
   Explore mining capabilities →
</a>
```

---

### Extractive Sector Section

**Location: Mining section CTA button**

**utm_content:** `mining_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=mining_cta
```

**Text:** Explore CDC Mining Capabilities

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=mining_cta"
   target="_blank"
   rel="noopener noreferrer"
   class="btn-pill">
   Explore CDC Mining Capabilities
</a>
```

---

### Technology Section

**Location: Technology section CTA button**

**utm_content:** `technology_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=technology_cta
```

**Text:** Explore CDC Global

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=technology_cta"
   target="_blank"
   rel="noopener noreferrer"
   class="btn-pill">
   Explore CDC Global
</a>
```

---

### PPP & ROI Section

**Location: PPP section CTA button**

**utm_content:** `ppp_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=ppp_cta
```

**Text:** Explore PPP-Ready Infrastructure Models

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=ppp_cta"
   target="_blank"
   rel="noopener noreferrer"
   class="btn-pill">
   Explore PPP-Ready Infrastructure Models
</a>
```

---

### Footer Section

#### Primary CTA Button

**utm_content:** `footer_primary_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=footer_primary_cta
```

**Text:** Explore CDC Global Capabilities

**Implementation:**
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=footer_primary_cta"
   target="_blank"
   rel="noopener noreferrer"
   class="btn-pill">
   Explore CDC Global Capabilities
</a>
```

---

### Mobile Sticky CTA

**Location: Fixed button at bottom of mobile screen (appears after scrolling past hero)**

**utm_content:** `mobile_sticky_cta`

**URL:**
```
https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=mobile_sticky_cta
```

**Text:** Explore CDC Global Capabilities

**Implementation:**
```html
<div class="mobile-sticky-cta">
  <a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=mobile_sticky_cta"
     target="_blank"
     rel="noopener noreferrer"
     class="btn-pill">
     Explore CDC Global Capabilities
  </a>
</div>
```

---

## Summary Table

| Location | utm_content | Button Text | Status |
|----------|-------------|-------------|--------|
| Navigation | `nav_cta` | Global Capabilities | ⏳ |
| Hero (Primary) | `hero_primary_cta` | Explore CDC Global Capabilities | ⏳ |
| About | `about_text_cta` | Explore the CDC global platform → | ⏳ |
| Use Case: Urban | `usecase_urban` | Explore urban capabilities → | ⏳ |
| Use Case: Tourism | `usecase_tourism` | Explore tourism capabilities → | ⏳ |
| Use Case: Remote | `usecase_remote` | Explore remote access capabilities → | ⏳ |
| Use Case: Mining | `usecase_mining` | Explore mining capabilities → | ⏳ |
| Mining Section | `mining_cta` | Explore CDC Mining Capabilities | ⏳ |
| Technology Section | `technology_cta` | Explore CDC Global | ⏳ |
| PPP Section | `ppp_cta` | Explore PPP-Ready Infrastructure Models | ⏳ |
| Footer (Primary) | `footer_primary_cta` | Explore CDC Global Capabilities | ⏳ |
| Mobile Sticky | `mobile_sticky_cta` | Explore CDC Global Capabilities | ⏳ |

**Total Links:** 12

---

## Validation Checklist

When implementing, verify:

- [ ] All `href` starts with `https://cdc.company?`
- [ ] All links include `utm_source=cdc_africa`
- [ ] All links include `utm_medium=landing`
- [ ] All links include `utm_campaign=africa_gateway`
- [ ] Each link has unique `utm_content` value (from table above)
- [ ] All external links have `target="_blank"`
- [ ] All external links have `rel="noopener noreferrer"`
- [ ] No typos in UTM parameter names
- [ ] No typos in utm_content values
- [ ] Test links in analytics dashboard

---

## Testing in Google Analytics

Once implemented:

1. Go to Google Analytics
2. Navigate to: Traffic → Source/Medium
3. Look for: `(direct) / (none)` → Filter by `cdc_africa` source
4. Verify all 12 utm_content values appear
5. Check conversion funnels for each entry point

---

## Quick Copy-Paste Reference

Use these as templates for copy-pasting into index.html:

### Template: Standard Button
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=REPLACE_WITH_CONTENT"
   target="_blank"
   rel="noopener noreferrer"
   class="btn-pill">
   Button Text Here
</a>
```

### Template: Arrow Link
```html
<a href="https://cdc.company?utm_source=cdc_africa&utm_medium=landing&utm_campaign=africa_gateway&utm_content=REPLACE_WITH_CONTENT"
   target="_blank"
   rel="noopener noreferrer"
   class="text-link-arrow">
   Link Text →
</a>
```

---

## Maintenance Notes

- Review utm_content values quarterly with marketing team
- Update this document if new CTA locations are added
- Sync with analytics dashboard naming conventions
- Keep GA4 filter updated if domain changes
