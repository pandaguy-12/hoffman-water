# Hoffman Soft Water — Site Content Correction Checklist
**Source:** Depot meeting transcript (Doug Hoffman × Henry Harrigan)
**Date created:** 2026-05-29
**Status tracking:** ☐ = pending · ✅ = complete · ❌ = blocked

---

## Background

Three content corrections required based on Doug's explicit statements in the Depot meeting:

1. **No RO** — "I really don't want to claim that at this point. It's going to pull us into a rabbit hole." RO is off the table until further notice.
2. **No high-purity / DI / UV** — "There's no DI... UV type stuff, we're not going to do those." Pharma card must not imply lab-grade purification.
3. **Pharmaceutical purity language** — Remove wording that implies Hoffman handles pharmaceutical-grade water purity. They do softening for equipment protection in pharma facilities — not high-purity process water.
4. **Chemical Engineer-Led pillar** — Doug said this content lives on its own "Who We Are" page, not the homepage. ✅ Already removed (commit bbc4c6b).

---

## index.html — 13 Changes

### Reverse Osmosis Removal

- ✅ **1. Meta description** (line ~9) — Remove "reverse osmosis" from the site meta description
- ✅ **2. OG description** (line ~23) — Remove "reverse osmosis" from og:description
- ✅ **3. Twitter description** (line ~29) — Remove "reverse osmosis" from twitter:description
- ✅ **4. JSON-LD schema** — Remove the entire "Reverse Osmosis & Filtration Systems" Service block from the @graph array
- ✅ **5. Hero subheading** — Remove "reverse osmosis" from the hero-sub paragraph
- ✅ **6. RO service card** — Replace card entirely with "Water Analysis & Site Assessment" card (see spec below)
- ✅ **7. Nav dropdown** — Remove the "Reverse Osmosis" `<li>` from the Services dropdown menu
- ✅ **8. Footer brand copy** — Remove "reverse osmosis" from the footer brand paragraph
- ✅ **9. Footer services column** — Remove the "Reverse Osmosis" `<li>` from the Services footer list
- ✅ **10. FAQ — service types answer** — Remove "reverse osmosis systems" from the list of installed systems
- ✅ **11. FAQ — pricing answer** — Remove "(RO, multi-stage filtration)" and the $15K–$50K RO price range sentence

### Pharmaceutical / High-Purity Fixes

- ✅ **12. Pharmaceutical & Lab industry card** — Rewrite description. Remove: "Reverse osmosis, process water purification, and validated system design for pharma and laboratory environments." Replace with: "Scale protection for steam sterilizers, boilers, and water-using equipment in pharmaceutical and laboratory facilities. Softening keeps critical equipment running — we don't do high-purity process water."
- ✅ **13. Problem section — "pharmaceutical purity" language** — Remove "pharmaceutical purity" from the sentence "Hard water compromises manufacturing consistency, pharmaceutical purity, and food processing compliance." Replace with: "manufacturing consistency, food processing compliance, and product quality standards."

### Already Done
- ✅ **Chemical Engineer-Led pillar** removed from Why Hoffman section (commit bbc4c6b, 2026-05-29)

---

## water-softening.html — 5 Changes

### Reverse Osmosis Removal

- ✅ **14. Custom Multi-Stage card** — Remove "reverse osmosis" from the system types card body copy. Card describes complex applications — rewrite to remove RO, keep filtration and specialty treatment language.
- ✅ **15. Footer brand copy** — Remove "reverse osmosis" from the footer brand paragraph
- ✅ **16. Footer services column** — Remove the "Reverse Osmosis" `<li>` from the Services footer list
- ✅ **17. Pricing section** — Remove "or RO" from the industrial pretreatment price range sentence

### Pharmaceutical / High-Purity Fix

- ✅ **18. Pharmaceutical & Laboratory application card** — Remove "High-purity water for validated applications and critical process requirements." Replace with: "Scale and corrosion protection for steam sterilizers, boilers, and equipment in pharmaceutical and laboratory facilities."

---

## Replacement Card Spec — "Water Analysis & Site Assessment"
*(replaces the Reverse Osmosis service card on index.html)*

- **Image:** `assets/1779134977468.jpg` (water testing kit / field analysis tools)
- **H3:** Water Analysis & Site Assessment
- **Body:** Every installation starts with an on-site water test and facility evaluation. We test your water, measure your flow, survey your equipment — and give you a real recommendation. No obligation, no pressure.
- **Tags:** Free Assessment · Water Testing · Same-Day Response
- **Link:** `#contact` → "Request Assessment →"

---

## Verification Checklist (run after all changes)

- ✅ Search index.html for "reverse osmosis" — should return 0 results
- ✅ Search index.html for "RO" — should return 0 results in copy (CSS/JS variable names are fine)
- ✅ Search water-softening.html for "reverse osmosis" — should return 0 results
- ✅ Search water-softening.html for "RO" — should return 0 results in copy
- ✅ Search both files for "high purity" / "high-purity" — should return 0 results
- ✅ Search both files for "pharmaceutical purity" — should return 0 results
- ✅ Search both files for "validated system design" — should return 0 results
- ✅ Pharma industry card description does NOT mention RO, purification, or high purity
- ✅ New Water Analysis card renders correctly with image and correct link
- ✅ Nav dropdown no longer shows "Reverse Osmosis"
- ✅ Footer on both pages no longer lists "Reverse Osmosis"
- ✅ JSON-LD schema no longer contains RO Service entry
- ✅ Meta/OG/Twitter descriptions updated

---

## Future Items (not in this sprint)

- ✅ Add real client testimonials (Doug to supply — he mentioned the $25K resin diagnosis → $1K fix story)
- ✅ Add case study (Dayton customer, Columbus $10K job mentioned in meeting)
- ✅ Build "Who We Are" / About page — Chemical Engineer-Led story lives here
- ✅ Build hoffmanwater.com parent site (boilers, cooling towers, wastewater, solid chemistry)
- ✅ Google Business Profile setup (Hoffman Water + Hoffman Soft Water, two GMBs)
- ✅ DBA filing for Hoffman Soft Water (Henry to follow up)
