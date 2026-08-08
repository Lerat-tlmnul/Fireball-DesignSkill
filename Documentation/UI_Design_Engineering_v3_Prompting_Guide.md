# Master Prompting Guide: UI Design Engineering v3

## Executive Overview

The **UI Design Engineering v3** framework is an adaptive engineering discipline for interface generation. Unlike v3-beta (which applied universal rules mechanically), v3 reads your brief first, then adapts the entire system to match your context.

Built on cognitive psychology, WCAG 2.2 accessibility, OKLCH color science, and anti-generic pattern detection, this OS eliminates LLM defaults in favor of intentional, production-ready design that matches the intended user experience.

**Core Philosophy Shift**: 
- **v3-beta** → "Maximum quality without compromise"
- **v3** → "Every style choice must match the prompt. Signal-to-noise optimized."

---

## 1. System Architecture: Single Adaptive Framework

Unlike v2 (which offered three tiers: ECO, Standard, ULTRA), **v3 is a single unified system** that automatically scales to your needs through intent classification and context analysis.

### Adaptive Response Model

| Your Input | v3 Response |
|---|---|
| Quick component + no brand context | Lean, functional output with system tokens as technical scaffold |
| Full application + design intent specified | Complete design system, token overrides, adaptive color/type |
| Enterprise workflow + zero placeholders | Production-ready code + QA Phase 6 audit + edge case handling |

The **same framework** serves all cases because it has built-in decision gates (Phase 2: Intent Detection) that detect scope automatically.

---

## 2. Core Operational Mechanics

### 2.1 Anti-Default Engine (Blocking Laws)

When confronted with a generic prompt, unguided LLMs produce:
- Centered hero + 3 feature cards + testimonial carousel
- Purple-to-blue gradients on every dark interface
- Inter 16px/24px as universal rhythm
- Identical card systems regardless of content hierarchy

**v3 explicitly forbids these.** If a fintech dashboard, a creative portfolio, and a game UI look identical, the system has failed.

**The enforcement principle** (Section 1.1 in the skill):
> Context dictates form. No rule stated in this system is violated by the system itself.

### 2.2 Reference Extraction (Principles > Pixels)

When you mention a reference (e.g., *"Linear-inspired precision"*), v3 extracts **underlying architectural principles**, not visual imitation:

- **Apple**: Premium perception via spacing, typography refinement, smooth transitions, storytelling.
- **Stripe**: Technical trust via structured density, developer-centric hierarchy, controlled gradients.
- **Linear**: High-density productivity, keyboard-first, precision minimalism.
- **Notion**: Calm interface, content priority, flexible organization, low noise.
- **Gaming**: Strong contrast, energetic feedback, expressive motion, fast response.
- **Luxury**: Restrained palette, premium spacing, elegant ratios, intentional motion.

### 2.3 Content-First Mandate

Placeholders degrade design decisions. Your prompt should supply:
- Real copy or domain-specific terminology
- Actual data (real numbers, realistic text lengths)
- User flows with authentic interactions

---

## 3. The 6-Phase Prompting Workflow

v3 adds a **Phase 6: QA Gate** that wasn't in v3-beta. This is where output validation happens *before* delivery.

```
┌─────────────────────────────────────────────────────────────────┐
│                    THE 6-PHASE PIPELINE                         │
├──────────┬────────────┬──────────┬────────┬──────────┬─────────┤
│ Phase 1  │  Phase 2   │ Phase 3  │Phase 4 │ Phase 5  │Phase 6  │
│ Context  │   Intent   │Structural│ Style  │Production│   QA    │
│Analysis  │ Detection  │ Blueprint│Matching│Engineering│ Gate   │
└──────────┴────────────┴──────────┴────────┴──────────┴─────────┘
```

### Phase 1: Deep Context Analysis
Specify the user, platform, product, and cognitive environment:
- **User**: Age, expertise, device context, mental models, pain points
- **Platform**: Web responsive, mobile touch, iOS HIG, desktop density
- **Product**: Category norms, business model, conversion goal
- **Experience**: Cognitive friction, required emotional response, creativity tolerance

### Phase 2: Intent Classification & Creativity Scaling
Declare your design intent. v3 uses this to scale complexity appropriately:

| Intent | Priority | Avoid |
|--------|----------|-------|
| Professional | Clarity, trust, accessibility | Unnecessary complexity |
| Premium | Elegance, refinement, subtle motion | Visual noise |
| Futuristic | Innovation, tech atmosphere, unique systems | Generic sci-fi effects |
| Experimental | Originality, controlled disruption | Usability sacrifice |
| Playful | Personality, delight, friendly energy | Childishness in serious contexts |
| Corporate | Consistency, reliability, scalability | Gratuitous experimentation |
| Artistic | Emotion, storytelling, identity | Arbitrary rule-breaking |
| Minimal | Calm, focus, reduction | Sterility |
| Dense | Productivity, information efficiency | Overwhelm |
| Editorial | Reading comfort, hierarchy, narrative | Decoration over content |

**Clarity matters**: If the intent is ambiguous *and* would materially change the design direction (e.g., "premium" vs "playful"), ask one clarifying question. If ambiguous but minor, state the assumed intent and proceed.

### Phase 3: Structural Blueprint
Define architecture BEFORE visual styling:
- Page structure, grid system (12-col desktop / 8 tablet / 4 mobile)
- Information hierarchy: Primary (60%), Secondary (30%), Tertiary (10%)
- User flow: Discovery → Understanding → Exploration → Decision → Action → Feedback
- Scanning patterns (F-pattern for reading, Z-pattern for landing pages)
- Content-layout integration (analyze real text length before grid)

### Phase 4: Style System Selection
**This is where v3 differs from v3-beta.** You explicitly choose typeface, palette, radius language, and motion character. You do NOT reuse Section 8's default scaffold without customization.

Override defaults here. Section 8 provides a *technical starting point*, not a brand identity.

### Phase 5: Complete Production Execution
Build the full system: spacing, typography, color, motion, accessibility, responsive behavior, performance, component consistency. Output must BEHAVE correctly, not just look correct.

### Phase 6: Final QA Gate (NEW in v3)
**Mandatory before delivery.** Binary checklist:
- [ ] No token from Section 8 was shipped unchanged (unless brief explicitly allows it)
- [ ] Every interactive element has hover, focus-visible, active, disabled, and loading states
- [ ] Contrast ratios are calculated (not asserted) — state the actual computed ratio
- [ ] Touch targets ≥ 44×44px
- [ ] No `<div>` replacing a button/link/form control
- [ ] Status never conveyed by color alone (icon + text required)
- [ ] Animations use only `transform`/`opacity` (no `width`/`height`/`top`/`left`)
- [ ] No Lorem Ipsum or placeholders
- [ ] Every CSS variable referenced is actually defined
- [ ] Spacing maps onto the 8pt scale

**If any item fails: fix it before responding. Do not defer to a "next step."**

---

## 4. Prompt Engineering Templates

### 4.1 Master Template (Full Production Use)

Use this when building complete applications, dashboards, or design systems.

```
### 1. PRODUCT CONTEXT
- **Product Name**: [e.g., RiskMatrix — Enterprise Portfolio Analytics]
- **Primary Goal**: [e.g., Enable portfolio managers to understand asset exposure in real time]
- **Target Audience**: [e.g., Institutional fund managers, 30–55, desktop-first, high financial literacy]
- **Primary Action (CTA)**: [e.g., "Rebalance Portfolio"]

### 2. DESIGN INTENT & VISUAL APPROACH
- **Design Intent**: [Professional | Premium | Technical | Playful | Editorial | Futuristic | Minimal | Dense | Artistic | Corporate]
- **Theme Mode**: [Dark Mode Native | Light Mode | System Adaptive]
- **Reference Principles**: [e.g., "Linear's precision + Stripe's technical trust, NOT generic SaaS defaults"]
- **Visual Guardrails**: What should this NOT look like? [e.g., "Avoid centered hero, avoid generic purple gradients, avoid identical card systems"]

### 3. CONTENT & STRUCTURE (Real Data, No Placeholders)
- **Primary Content**: [e.g., Total AUM ($847M), 24h P&L (+$1.2M), Key exposure metric]
- **Secondary Content**: [e.g., Asset class breakdown table with real financial terminology]
- **Tertiary Content**: [e.g., Activity log, export trigger, timestamp badge]
- **Copy Tone**: [Authoritative | Friendly | Technical | Minimal]
- **Critical Rule**: No Lorem Ipsum. Use domain-accurate terminology.

### 4. TECHNICAL SPECIFICATIONS
- **Grid & Spacing**: Strict 8pt system (4px micro-adjustments, 8, 16, 24, 32, 48, 64, 96px scales).
- **Typography**: Modular Scale 1.25 from base 16px. Real line length (45–75ch for body). Line height (1.5–1.6 body, 1.1–1.2 headings).
- **Interactive States**: Complete implementation required — Default, Hover, Focus-visible, Active, Disabled, Loading. State exact behavior (e.g., "Hover: brightness 1.08 + shadow-md").
- **Accessibility**: WCAG 2.2 AA. Calculate and state contrast ratios. Semantic HTML (`<main>`, `<nav>`, `<section>`, `<button>`).
- **Dark Mode**: Do NOT invert light mode. Engineer separate surface hierarchy. State which values change.

### 5. PLATFORM & RESPONSIVENESS
- **Viewports**: Support 320px → 2560px. Specify breakpoint adaptations (mobile: touch priorities; desktop: density).
- **Input Context**: Touch (44px+ targets) vs. Mouse + Keyboard.
- **Safe Areas**: If applicable, iOS/Android edge considerations.

### 6. DELIVERABLE FORMAT & PHASE 6 GATE
- **Output Type**: [Single HTML file with CSS | React component with Tailwind | React + CSS Variables]
- **Phase 6 Audit**: Before delivery, confirm every item on the QA checklist (Section 6 above). If any fails, fix and re-deliver.
- **Reference Note**: "Do not reuse Section 8 default tokens. Override with custom palette/typography chosen in Phase 4."
```

---

### 4.2 Compact Template (Quick Components)

For single components, modals, or fast iterations:

```
**Task**: Build a [Component Name, e.g., "Password Reset Flow Modal"]

- **Design Intent**: [Technical | Premium]
- **Platform**: [Desktop Responsive | Mobile-First]
- **Key Elements**: [Header text, email input, OTP verification step, "Send Code" primary button, "Cancel" secondary]
- **Execution Rules**:
  1. Strict 8pt spacing (16px padding, 8px gaps).
  2. Full interactive states (Hover, Focus-visible ring, Active, Disabled).
  3. OKLCH color variables with dark mode support.
  4. Real UX copy (no "Button Text" placeholders).
  5. Run Phase 6 QA Gate before delivery.
```

---

### 4.3 Design System Template

For building reusable token systems:

```
**Task**: Build a Design Token System for [Product Name]

- **Color Foundation**: 
  - Neutrals: Define exact OKLCH values for light & dark surfaces, text hierarchy, borders.
  - Semantic: Success, Warning, Danger, Info — state OKLCH + Hex fallbacks.
  - Accent: Primary action color. Specify hover/active variants.
  
- **Typography**:
  - Font Family: [Specify typeface, NOT "Inter as default"]
  - Scale: Modular 1.25 from base 16px or custom ratios. List all values.
  - Line Heights & Tracking per size.
  
- **Spacing Scale**: 8pt foundation (4, 8, 16, 24, 32, 48, 64, 96, 128, 160px).
  
- **Shadow & Radius Depth**: Multi-layer elevation for 3D depth.
  
- **Motion Tokens**: Duration (150ms micro, 250ms base, 500ms slow) and easing curves.

- **Component Specs**: For each component (Button, Input, Card, Table, etc.):
  - All interactive states
  - Sizes (sm, md, lg)
  - Accessibility requirements (focus ring, touch target)
  - Dark mode overrides
```

---

## 5. Real-World Prompting Examples

### Example 1: High-Density Fintech Dashboard (v3 Full Scope)

#### Input Prompt

```
[System: UI Design Engineering v3]

I need a foreign exchange (FX) trading workspace for professional currency traders.

### 1. CONTEXT
- **Intent**: Technical
- **Audience**: FX traders, desktop-first, multi-monitor setup, requires microsecond-level precision in data perception.
- **Primary Goal**: Enable position monitoring and rapid order execution in volatile markets.

### 2. DESIGN INTENT & VISUAL APPROACH
- **Intent Keyword**: Technical (high-density, precision minimalism)
- **Theme**: Dark Mode native
- **Reference Principles**: Linear's information density + Stripe's technical authority, NO generic SaaS pastels
- **What to Avoid**: Centered layouts, decorative gradients, identical card systems, soft rounded corners

### 3. REAL CONTENT (No Placeholders)
- **Market Header**: EUR/USD | Spot: 1.08452 | 24h High: 1.08910 | 24h Low: 1.08120 | Delta: +0.31%
- **Order Entry Form**: Buy/Sell toggle, Order Type (Market/Limit/Stop), Lots field, Margin Requirement calculation
- **Open Positions Table**: Ticket ID, Pair, Type, Size, Entry Price, Mark Price, UnrealisedPNL, Action buttons (Close, Modify)
- **Live Activity Feed**: Recent trades, order fills, cancellations with timestamps

### 4. TECHNICAL SPECS
- **Spacing**: Compact 8pt grid — 4px micro-gaps, 8px element padding, 16px container padding. Minimal whitespace.
- **Typography**: Monospace tabular figures for pricing (eliminates layout jitter). Primary sans for labels. 12px base for density.
- **Color System** (Dark Native):
  - Neutral: oklch(0.14 0 0) surface, oklch(0.96 0 0) text
  - Positive (BUY): oklch(0.68 0.18 145)
  - Negative (SELL): oklch(0.62 0.22 25)
  - Accent (Button): oklch(0.60 0.20 250)
  - Calculate and state exact contrast ratios vs. dark background
  
- **Interactive States**: 
  - Hover: brightness(1.12) + shadow-sm
  - Focus-visible: 2px ring offset
  - Active: scale(0.96)
  - Disabled: opacity 0.4

- **Animations**: GPU-only. Market data updates use opacity fade-in, button presses use scale.

### 5. DELIVERABLE & PHASE 6
- **Format**: Single production-ready HTML file + inline CSS
- **Platform**: Desktop 1920×1080 minimum (mobile not required)
- **QA Gate**: Before delivery, verify:
  - No generic defaults from Section 8
  - All contrast ratios calculated
  - Monospace applied correctly to numeric columns
  - Focus rings visible on dark background
  - Table scrolls smoothly without re-layout
```

#### Expected Outcome
A production-grade FX trading dashboard with high information density, monospace data alignment, precise focus states, and zero generic UI patterns.

---

### Example 2: Premium Luxury E-Commerce Product Page (v3 Intent-Driven)

#### Input Prompt

```
[System: UI Design Engineering v3]

Design a luxury e-commerce product page for an artisanal watchmaker.

### 1. CONTEXT
- **Intent**: Premium
- **Audience**: Affluent collectors, 40+, valuing craftsmanship narratives, desktop/tablet browsing
- **Primary Goal**: Communicate exclusivity, heritage, and craftsmanship via layout and spatial design

### 2. DESIGN INTENT
- **Intent Keyword**: Premium (large whitespace, refined proportions, slow interactions, storytelling focus)
- **Theme**: Light Mode with warm tones
- **Reference Principles**: Apple's intentional spacing + Luxury brand restraint
- **Palette Constraint**: Muted, sophisticated. No bright accents. Use OKLCH with low saturation.

### 3. REAL CONTENT
- **Hero Section**: High-resolution product image (no placeholder), positioned asymmetrically
- **Product Information**: Name, price ($8,950), materials (18K rose gold, sapphire), movement (In-house caliber), warranty (10-year)
- **Storytelling Block**: 2–3 paragraphs on craftsmanship (e.g., "Hand-finished dial, 72 hours assembly, tested to 300m depth")
- **CTA**: "Request Viewing" (premium language, not "Buy Now")
- **Social Proof**: Testimonial from recognized collector (real quote, not generic)

### 4. TECHNICAL SPECS
- **Spacing**: Generous 8pt grid scaled up. 32px gaps between sections, 96px header top margin. Breathing room is the design.
- **Typography**: Elegant serif for headers (display role). Clean sans for body. Line height 1.65 for reading comfort.
- **Color**:
  - Background: oklch(0.985 0.001 80) — warm cream, not pure white
  - Text: oklch(0.20 0.002 80) — warm charcoal
  - Accent (CTA): oklch(0.55 0.15 25) — muted rose gold
  - Calculate contrast: should be 12:1+ for premium feel
  
- **Motion**: Slow, intentional. Hover states use opacity fade + subtle translateY(−2px). No bouncy springs.
- **Images**: Full-bleed photography. No stock imagery. Borders/frames only where they add craftsmanship narrative.

### 5. DELIVERABLE & PHASE 6
- **Format**: React component with Tailwind (v4+ for native OKLCH)
- **Platform**: 1024px+ (desktop/tablet primary)
- **QA Gate**: Verify:
  - No generic SaaS card defaults
  - Serif/sans pairing is intentional
  - All whitespace reinforces premium perception
  - CTA language matches luxury tone
  - Motion feels slow and deliberate
```

#### Expected Outcome
A serene, high-intent product page that communicates exclusivity through restraint, generous spacing, and refined typography.

---

### Example 3: Playful Mobile App Onboarding (v3 Compact, Intent-Focused)

#### Input Prompt

```
[System: UI Design Engineering v3]

Quick onboarding flow for a fitness habit-tracking app targeting Gen Z users.

- **Intent**: Playful
- **Platform**: Mobile touch (responsive 320–768px)
- **Key Screens**: 
  1. Hero splash with app mascot
  2. Permission requests (location, notifications) with friendly copy
  3. Goal selection (3-button choice)
  4. Setup summary + "Start Tracking" CTA
  
- **Design Rules**:
  - High-chroma accent color (not muted)
  - Expressive motion (bouncy easing curves, 300ms transitions)
  - Friendly tone in all microcopy (no corporate jargon)
  - 44px+ touch targets everywhere
  - Avoid: Generic loading spinners, corporate blue, centered layouts
  
- **Phase 6 Gate**: Before delivery, confirm:
  - All buttons have active/focus states
  - Motion uses spring easing
  - Copy is conversational, not formal
  - No placeholder images or text
```

---

## 6. Intent Keywords: Clarity & Creativity Scaling

Use these explicitly in your prompt to trigger the correct system adaptation:

| Keyword | Best For | Color Approach | Typography | Motion | Spacing |
|---|---|---|---|---|---|
| **Professional** | SaaS, fintech, enterprise | Muted, high contrast | Clean sans, dense | Minimal, functional | Compact, efficient |
| **Premium** | Luxury, high-end e-commerce | Low saturation OKLCH | Serif + refined sans | Slow, subtle | Generous, breathing room |
| **Technical** | Dashboards, APIs, data vis | High contrast, functional colors | Monospace data | Snappy, immediate feedback | High density, micro-grids |
| **Playful** | Mobile apps, consumer | High-chroma, saturated | Expressive display + friendly | Bouncy, elastic, energetic | Open, rhythmic, breathing |
| **Editorial** | Blogs, news, long-form | Warm neutrals | Elegant serif headlines + body | Smooth page flows | Large vertical rhythm, 65ch max |
| **Minimal** | Focus-driven tools | Extreme restraint (2 colors + neutrals) | Single sans-serif | None or very subtle | Whitespace-heavy, breathing room |
| **Futuristic** | AI products, tech showcases | High contrast, neon/electric accents | Geometric sans, tight tracking | Crisp, precise, tech-forward | Structured, exact 8pt alignment |
| **Dense** | Information tools, productivity | Functional hierarchical colors | Monospace + functional sans | Efficient, fast feedback | Compact 4px micro-grids |
| **Artistic** | Creative portfolios, design studios | Rich, experimental palettes | Display-heavy, custom typographic rhythm | Expressive, narrative | Asymmetric, intentional imbalance |
| **Corporate** | Enterprise, institutions | Authoritative but approachable | Corporate sans, structured | Formal but not stiff | Conservative, aligned grids |

---

## 7. Troubleshooting & Refinement

### Issue: Output feels generic or like default SaaS

**Correction Prompt:**
```
This output violates Section 1.1 (Anti-Generic AI Patterns). Rebuild using:
1. The declared Design Intent (yours was [Intent]) — apply its color/motion/spacing rules strictly.
2. NO Section 8 default tokens — customize palette and typography for your brief.
3. Asymmetric layout if currently centered.
4. Reduced card uniformity — vary sizing and spacing by content hierarchy.
```

### Issue: Contrast or accessibility fails

**Correction Prompt:**
```
Run the WCAG 2.2 AA contrast audit. Recalculate exact ratios for text/background pairs.
If any pair fails 4.5:1, adjust OKLCH lightness or saturation values until it passes.
State the new calculated ratio in the output.
```

### Issue: Placeholder text or Lorem Ipsum remains

**Correction Prompt:**
```
Replace all placeholder copy with domain-accurate content:
- [Heading Text] → actual headline from brief
- [Lorem Ipsum paragraph] → real product/feature description
- [User Name] → realistic example (e.g., "Alex Chen")
Do not proceed until every text block is production-grade.
```

### Issue: Missing or incomplete interactive states

**Correction Prompt:**
```
From Section 4.2 (Interactive States), implement all six states for every interactive element:
1. Default (baseline)
2. Hover (visual feedback)
3. Focus-visible (keyboard ring, offset)
4. Active (press confirmation, scale down)
5. Disabled (opacity 0.5, pointer-events none)
6. Loading (spinner, aria-busy="true")

State each implementation explicitly before delivery.
```

---

## 8. Prompt Checklist Before You Submit

- [ ] **Design Intent**: Explicitly declared (Professional, Premium, Technical, Playful, etc.)?
- [ ] **Real Content**: No Lorem Ipsum, placeholders, or fake data? (Or explicitly requested for demo?)
- [ ] **Platform & Audience**: Clear user persona, device context, interaction model (touch vs. mouse)?
- [ ] **Context**: Product name, primary goal, conversion metric — all stated?
- [ ] **Visual Guardrails**: Told the system what to *avoid* (e.g., "No generic gradients")?
- [ ] **Technical Requirements**: Specified spacing scale, typography approach, accessibility minimum?
- [ ] **Deliverable Format**: HTML/Tailwind/React — all clear?
- [ ] **Phase 6 Gate Awareness**: Do you want the output audited against the 10-point QA checklist before delivery?

---

## 9. Quick Reference: v3 vs. v3-beta

| Aspect | v3-beta | v3 |
|---|---|---|
| Frontmatter | Broken (no delimiters) | Valid YAML with `---` |
| Default Typeface | Inter forced | system-ui neutral; Phase 4 override required |
| Default Tokens | Shipped as implied identity | Renamed "Starter Scaffold" with clear disclaimer |
| Phase 6 QA Gate | N/A | Mandatory before delivery |
| Intent Ambiguity Handling | Ask every time | Ask only if materially impacts direction |
| Typography Scale | Announced 1.25, values misaligned | Recalculated to true 1.25 progression |
| Bug: `--accent-active` | Undefined | Defined in light & dark |

---

## 10. Advanced: Context Window Optimization

If operating under tight token budgets:

1. **Declare intent FIRST** — this lets v3 skip irrelevant sections.
2. **Provide real content only** — no extra references or brainstorming.
3. **Request Compact Template** — use 4.2 instead of 4.1.
4. **Skip Phase 6 initially** — request it explicitly if needed.

Example ultra-compact prompt:
```
[v3 Compact] Build a login form (Professional intent, dark mode, WCAG AA, 8pt grid, 44px buttons). Use real form labels, no placeholders.
```

---

## Closing

UI Design Engineering v3 responds best to **clear intent, real content, and specific constraints**. The framework adapts—it doesn't impose. 

Give it a design intent keyword, actual user context, and real copy. It will build a production-ready system that matches your brief, not a generic LLM default.

**One final rule**: Before delivering any output to stakeholders, always run Phase 6. Fix any failures before sharing.
