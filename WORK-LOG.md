# iBOOD Email CRO — Work Log

## Project Overview

Built a custom Claude Code skill and 5 HTML email template variants for iBOOD's daily deals newsletter (500K+ subscribers). The goal: increase open rates (baseline 30%), click-through rates, and purchase conversions through CRO-driven template design.

**Live preview:** https://ibood-email-templates.vercel.app

---

## What We Built

### 1. Claude Code Skill: `daily-deals-cro`

**Location:** `~/.claude/skills/daily-deals-cro/SKILL.md`

A reusable skill that triggers when working on daily deals email optimization. Contains:

- **Audit framework** — Score emails on 8 criteria (subject line, hero deal, price presentation, sub-deals grid, urgency/scarcity, CTAs, mobile optimization, social proof)
- **Optimize mode** — Generates 5 subject line variants, hero deal improvements, and quick wins
- **Template design principles** — Visual hierarchy, color usage, typography rules
- **Output format** — Structured audit reports with scores, problems, quick wins, and expected impact

### 2. Five Email Template Variants

Each template tests a different CRO hypothesis:

| # | Template | Hypothesis | Expected CTR Lift |
|---|----------|-----------|-------------------|
| 1 | **Urgency-First** | Countdown timers + stock indicators + "bijna op" badges trigger loss aversion | +20-30% hero |
| 2 | **Price Punch** | Savings in EUR (not just %) + dark theme = stronger value perception | +15-20% hero |
| 3 | **Social Proof** | Reviews + "X verkocht" + live shoppers = trust + bandwagon effect | +20-30% hero |
| 4 | **Single Focus Hero** | Hero dominates 60% viewport, fewer choices = faster decisions (Hick's Law) | +30-40% hero |
| 5 | **Mobile-First** | 420px, single column, 44px+ tap targets for 70%+ mobile opens | +20-30% mobile |

### 3. Showcase Website

`index.html` — Interactive showcase with tab navigation, iframe previews, hypothesis cards, and insights panels for each template. Deployed on Vercel.

---

## Brand Guidelines Incorporated

### Colors
| Color | Hex | Usage |
|-------|-----|-------|
| iOrange | `#FC5628` | CTAs, action elements, interactive elements |
| iBlue | `#6EA9E5` | Secondary, accents |
| iDark | `#1E0033` | Text, dark backgrounds, logo |
| Blue Steel | `#B6CFF2` | Light backgrounds, subtle accents |
| Discount Green | `#5CE567` | Discount badges, savings |
| White | `#FFFFFF` | Backgrounds |

### Discount Badges (strict rules)
- **Primary badge:** `#5CE567` background + `#1E0033` text (speech bubble shape)
- **Secondary badge:** `#1E0033` background + `#FFFFFF` text
- Never use other colors for discount badges
- Never mirror badges or use wrong shapes

### Brand Principles
1. **Kwaliteit** — Serieus over producten, beste deals elke dag
2. **Rebels** — Onverwacht, breekt met standaard
3. **Eigenzinnig** — Uitgesproken energie, eigen ding
4. **Platform** — Beste prijzen, verrassend aanbod
5. **Toegankelijk** — Community-first, eerlijk, transparant

### Brand Voice
- Playful, Bold, Rebels, Eigenzinnig, Toegankelijk
- Language: Dutch (Nederlands)

### Brand Traits (tone boundaries)
| WEL | NIET |
|-----|------|
| Energetic | In your face |
| Adaptable | Inconsistent |
| Fun | Childish |
| Goofy | Dumb |
| Informal | Sloppy |
| Dedicated | Obsessed |
| Similar | Different |
| Positive | Exaggerated |
| Enthousiastic | Hysterical |
| Professional | A smart ass |

---

## Changes Made

### Initial Build
- Created skill definition at `~/.claude/skills/daily-deals-cro/SKILL.md`
- Built 5 HTML email templates with placeholder product data
- Created `index.html` showcase page
- Deployed to Vercel: `ibood-email-templates.vercel.app`

### Brand Color Pass
Applied brand palette across all templates:
- `#ff6b35` → `#FC5628` (iOrange)
- `#1a1a2e` / `#0a0a1a` → `#1E0033` (iDark)
- `#22c55e` / `#00e676` → `#5CE567` (Discount Green)
- `#ff4444` / `#ffd700` / `#ffc107` → `#FC5628` (consolidated to iOrange)
- Light backgrounds → `#E8F0FB` (Blue Steel tint)

### Brand Guidelines Pass
Fixed brand-specific rules across all 5 templates:
- **Discount badges** — Changed from orange bg + white text → green bg (`#5CE567`) + dark text (`#1E0033`)
- **Save/bespaar badges** — Text changed from white to `#1E0033`
- **Campaign banners** — Replaced generic purple gradients with brand dark gradient (`#1E0033` → `#2d1b4e`)
- **Campaign CTAs** — Text color updated to iOrange (`#FC5628`)

### Skill Updates
Added to `SKILL.md`:
- Brand principles (5 pillars)
- Brand colors table
- Discount badge rules (primary, secondary, special events)
- Brand traits (10 tone pairs with boundaries)

---

## File Structure

```
ibood-email-templates/
├── index.html                      # Showcase page with all 5 templates
├── template-1-urgency.html         # Urgency-first variant
├── template-2-price-punch.html     # Price-focused variant
├── template-3-social-proof.html    # Social proof variant
├── template-4-single-focus.html    # Single focus hero variant
├── template-5-mobile-first.html    # Mobile-first variant
└── WORK-LOG.md                     # This file
```

---

## Next Steps

- [ ] A/B test templates against current production email
- [ ] Replace placeholder images with real product photos
- [ ] Connect to email service provider (ESP) for dynamic content
- [ ] Set up tracking for CTR per template section (hero, sub-deals, flash sales)
- [ ] Test email rendering across clients (Gmail, Outlook, Apple Mail)
- [ ] Consider table-based layout for broader email client compatibility
- [ ] Build dynamic version that pulls live deal data
