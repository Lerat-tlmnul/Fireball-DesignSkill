---
name: ui-design-engineering
description: >
  Use when the user asks to design, build, redesign, or review a UI, UX flow,
  landing page, dashboard, design system, or individual component (web,
  mobile, or desktop). Applies cognitive-psychology principles, WCAG 2.2
  accessibility math, OKLCH color, spacing/type systems, and anti-generic
  design patterns to produce production-ready front-end code rather than
  static mockups. Do not use for pure backend, data-pipeline, or non-visual
  engineering tasks.
---

# UI Design Engineering v3 OS

## 0. Core Philosophy & First Principles
UI Engineering is an applied science, not aesthetic decoration. Every pixel must be justified by:
- Cognitive Psychology (Hick's Law, Miller's Law, Gestalt)
- Human-Computer Interaction & Optical Perception
- Mathematical Systems (8pt grid, Modular Scale 1.25)
- Accessibility (WCAG 2.2 AA/AAA with calculated ratios)
- Platform Conventions (iOS HIG, Material 3, Web Standards)
- Business Objectives & User Jobs-to-be-Done

**Prime Directives:**
1. Beautiful but confusing = FAILURE.
2. Functional but soulless = INCOMPLETE.
3. Design must feel obvious before users understand why.
4. Great interfaces are understood, not just seen.
5. Ship production-ready code. Never generate prototypes or placeholders.

## 1. BLOCKING LAWS (Highest Priority — Non-Negotiable)

### 1.1 Anti-Generic AI Patterns (FORBIDDEN)
NEVER default to these statistically probable but creatively bankrupt patterns:
- Centered hero + gradient mesh + 3 feature cards + logo cloud + testimonial carousel
- Purple-to-blue diagonal gradients as primary brand expression
- Glassmorphism spam (blur + translucent cards without semantic purpose)
- Identical card systems with uniform shadow/radius regardless of content hierarchy
- Inter as an unexamined default typeface, or 16px/24px as a universal rhythm
- Lucide outline icons without contextual intent or optical correction
- Same layout structure across fintech, gaming, luxury, AI, edu, music

**Rule:** Context dictates form. A banking dashboard and a creative portfolio MUST have divergent design languages.

> **Enforcement note:** Section 8 ships one concrete token set so the system is runnable out of the box. Those values are a *starting scaffold*, not a brand identity — Phase 4 (Style System Selection) MUST override typeface, palette, and radius language before any real deliverable ships. Reusing Section 8 unchanged for a real brief is itself a violation of 1.1.

### 1.2 Reference Adaptation: Principles > Pixels
When references are provided, extract underlying logic, NOT visual appearance:
- **Apple:** Premium perception via intentional spacing, refined typography, smooth transitions, product storytelling. NOT white backgrounds + rounded cards.
- **Stripe:** Technical confidence via structured layouts, developer-oriented hierarchy, controlled gradients, precise interactions.
- **Linear:** High density + productivity focus + keyboard-first + precision minimalism.
- **Notion:** Calm interface + content priority + flexible organization + low noise.
- **Gaming:** Strong contrast + energetic feedback + expressive visuals + fast response.
- **Luxury:** Restrained palette + premium materials + large spacing + slow intentional motion.
- **Brutalist:** Intentional imperfection + visible structure + rule-breaking WITH purpose.

### 1.3 Content-First Mandate
Interfaces are communication systems, not component showcases.
- NEVER use Lorem Ipsum, fake stats, placeholder images, or empty states unless explicitly requested.
- Before ANY layout work, define: user needs, problem solved, required actions, message priority, information hierarchy.
- Every element must justify existence via: user understanding, user action, product storytelling, OR business objective.
- If removing an element loses nothing, it should not exist.

### 1.4 Production Mindset Enforcement
You are a senior front-end engineer, NOT a mockup generator.
- NO empty sections, fake buttons, missing nav, unfinished components, or "Coming soon" blocks.
- Generated output must be immediately deployable. Users should never imagine missing pieces.

## 2. Adaptive Workflow Engine

### Phase 1: Deep Context Analysis
- **User:** Age, tech literacy, device context, mental models, JTBD, pain points
- **Platform:** Web (responsive/keyboard), Mobile (touch/safe areas/gestures), iOS (HIG/SF), Android (Material/FAB), Desktop (density/shortcuts), Tablet (hybrid)
- **Product:** Category norms, single key metric, business model, conversion goal
- **Experience:** Cognitive friction points, required 3-second emotional response, creativity tolerance, interaction style

### Phase 2: Intent Classification & Creativity Scaling
Classify BEFORE designing. Adapt creativity level to context:

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

**Prompt is source of truth.** If intent is ambiguous and it materially changes the design direction (e.g. "premium" vs "playful" would produce different systems), ask one targeted clarifying question before generating. If ambiguity is minor, state the assumed intent explicitly in the response and proceed.

### Phase 3: Structural Blueprint
Define architecture BEFORE visual styling:
- Page structure, grid system (12-col desktop / 8 tablet / 4 mobile), content density, navigation model
- Information Hierarchy: Primary (strongest emphasis), Secondary (supporting), Tertiary (useful but subordinate)
- User Flow: Discovery → Understanding → Exploration → Decision → Action → Feedback → Return
- Scanning Patterns: F-pattern for reading, Z-pattern for landing pages
- Content-Layout Integration: Analyze real text length, image purpose, data complexity BEFORE structuring

### Phase 4: Style System Selection
Choose typeface, palette, radius language, and motion character from the classified intent (Phase 2) and any references (1.2). This phase MUST override the Section 8 scaffold values — never design from habit or statistical defaults.

### Phase 5: Complete System Execution
Build using the full design system. Every decision considers: spacing, typography, color, motion, accessibility, responsive behavior, performance, component consistency. Final output must BEHAVE correctly, not just look correct.

### Phase 6: Final QA Gate (mandatory before delivery)
Do not deliver until every item below is true. If any item fails, fix it before responding — do not describe the fix as a "future step."
- [ ] No token from Section 8 was shipped unchanged if the brief implied a distinct brand identity (see 1.1 enforcement note)
- [ ] Every interactive element has hover, focus-visible, active, disabled, and (if async) loading states
- [ ] Contrast ratios are calculated, not asserted — state the actual computed ratio for text/background pairs
- [ ] Touch targets ≥ 44×44px on any touch-capable surface
- [ ] No `<div>` standing in for a button, link, or form control
- [ ] Status is never conveyed by color alone (icon + text required)
- [ ] Animations use only `transform`/`opacity`; nothing animates `width`/`height`/`top`/`left`
- [ ] No Lorem Ipsum, placeholder image, or "Coming soon" block unless explicitly requested
- [ ] Every CSS custom property referenced in component code is actually defined in `:root`
- [ ] Spacing values map onto the 8pt scale (or a documented 4px exception)

## 3. Design System Specifications

### 3.1 Spacing: 8pt Mathematical Grid
- Primary scale: 4, 8, 16, 24, 32, 48, 64, 96, 128, 160px
- 4px exceptions ONLY for: icon alignment, border adjustments, micro-typography corrections
- Spatial Rhythm: Small (connected elements), Medium (component groups), Large (section separation)
- Whitespace is an ACTIVE design element for focus, hierarchy, calmness, premium perception
- ❌ Bad: `margin:17px padding:29px gap:13px`
- ✅ Good: `margin:16px padding:32px gap:16px`

### 3.2 Typography: Structural System
- Modular Scale 1.250 (Major Third) from a 16px base: 12 / 14 / 16 / 20 / 25 / 31 / 39 / 49 / 61 / 76px
- Line Length: 45–75ch, `max-width: 65ch` for body text
- Line Height: Body 1.5–1.6, Headings 1.1–1.2, Dense UI 1.2
- Tracking: Large headings −0.02em, Body normal, Small caps +0.02em
- Adapt to intent: Luxury (elegant proportions), Technical (clarity/density), Playful (expressive rhythm), Editorial (reading comfort)

### 3.3 Color: Functional OKLCH System
- Use OKLCH/HSL for token definition. Hex only as an implementation fallback for tooling that lacks OKLCH support.
- 60/30/10 Rule: 60% neutral background, 30% secondary/brand, 10% accent (primary actions/status ONLY)
- Dark Mode ≠ Inverted Light Mode:
  - No pure black (`#000`)
  - Reduce saturation 20–30%
  - Maintain readable contrast (calculate, don't guess)
  - Create depth via surface layers, NOT uniform shade
  - Shadows require higher opacity, careful blur

### 3.4 Motion: Purpose-Driven Communication
Every animation must: explain relationship, provide feedback, guide attention, improve understanding, confirm action, OR create emotional alignment.
- Micro-interactions: 150–250ms (hover, toggle, input feedback)
- Page Transitions: 300–500ms (navigation, section reveals)
- Easing: Enter = ease-out, Exit = ease-in, NEVER linear for organic movement
- Performance: GPU-friendly ONLY (`transform`, `opacity`). ❌ animating `width`/`height`/`top`/`left`
- Adapt: Premium (smooth/subtle), Playful (bouncy/expressive), Futuristic (precise/crisp), Gaming (fast/energetic)

### 3.5 Layout & Composition
Apply Gestalt Principles: Proximity, Similarity, Continuity, Closure, Figure-Ground.
Verify spatial mathematics: 8pt consistency, type scale adherence, line length, alignment, rhythm, proportion.

### 3.6 Cognitive Load Engineering
- Hick's Law: Reduce unnecessary choices/options/navigation
- Miller's Law: Group information meaningfully (chunking)
- Progressive Disclosure: Reveal complexity gradually, on-demand
- Hierarchy Validation: Is the primary action obvious? Can the interface be scanned in <3s? Does the eye follow the correct path?

### 3.7 Data Visualization (When Applicable)
Charts serve understanding, NOT decoration.
- Comparison → Bar | Trends → Line | Distribution → Histogram | Relationships → Scatter
- Rules: Consistent axes, clear units, helpful legends, accessible contrast, meaningful labels, accurate scales
- ❌ No decorative charts, misleading scales, excessive colors, confusing effects

## 4. Component Engineering Standards

### 4.1 Component Definition Requirements
Every component MUST specify: Purpose, Sizes, Variants, States, Spacing, Radius, Shadows, Typography, Interactions, Accessibility Behavior.

### 4.2 Interactive States (Complete)

| State | Behavior | Visual Implementation |
|-------|----------|----------------------|
| Default | Normal appearance | Token defaults |
| Hover | Subtle feedback | `brightness(1.08)` OR `translateY(-1px) + shadow-md` |
| Focus | Keyboard visibility | `0 0 0 2px bg, 0 0 0 4px accent`, 2px offset |
| Active | Press confirmation | `scale(0.98)` + darkened accent |
| Disabled | Non-interactive | `opacity:0.5`, `pointer-events:none`, `aria-disabled` |
| Loading | Progress feedback | Spinner + `aria-busy="true"` |

### 4.3 Button Hierarchy
- Primary: Main conversions, core user goals
- Secondary: Alternative/supporting actions
- Tertiary: Low-priority, navigation-like actions
- Sizes: sm (32h / 12px pad), md (40–44h / 16–20px pad), lg (48–56h / 24px pad)
- Required states: hover, focus-visible, active, disabled, loading

### 4.4 Semantic HTML & Accessibility
- Use semantic elements: `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`, `<button>`
- ❌ NEVER use `<div>` as an interactive-element replacement
- Touch Targets: Minimum 44×44 CSS pixels
- Color Independence: Status = Color + Icon + Text (❌ Red = Error alone → ✅ Red + ⚠️ + "Invalid email")
- Contrast: Calculate WCAG 2.2 AA ratios mathematically. State the calculated value, don't just claim compliance.

## 5. Responsive & Platform Engineering
- Support 320px → 2560px+ viewports
- Adapt hierarchy, navigation, density, spacing, interactions per breakpoint
- Mobile: Larger touch targets, clear priorities, reduced complexity, efficient nav
- Desktop: Higher density, advanced controls, multi-column, keyboard shortcuts
- Consider: Mouse vs touch, keyboard nav, screen readers, safe areas, container queries, fluid typography

## 6. Performance as UX
Beautiful + slow = bad UX. Performance IS user experience.
- LCP: Optimize images/fonts/server response/critical resources
- CLS: Reserve space for dynamic content, explicit image dimensions
- INP: Efficient JS/event handling/animation/component rendering
- Assets: SVG for icons/simple graphics, WebP/AVIF for photos, responsive sizing, lazy loading
- Fonts: `font-display:swap`, max 3–4 weights, variable fonts, proper fallbacks
- Animation: `transform`/`opacity` ONLY, avoid layout-triggering properties

## 7. UX Writing & Content Design
Text IS interface. Apply clarity, conciseness, consistency, tone, action-orientation.
Content and layout are interdependent. Analyze real text length, image purpose, data complexity, and reading behavior BEFORE structuring. The interface adapts to content, NOT vice versa.

## 8. Starter Token Scaffold (OKLCH + Fallbacks)

> These are a runnable *starting point*, not a brand system. Phase 4 must override typeface, accent hue, and radius language for any real deliverable — see the 1.1 enforcement note.

```css
:root {
  /* Spacing - 8pt base + 4pt micro */
  --space-0: 0px;
  --space-1: 4px; --space-2: 8px; --space-3: 12px; --space-4: 16px;
  --space-5: 20px; --space-6: 24px; --space-8: 32px; --space-10: 48px;
  --space-12: 64px; --space-14: 96px; --space-15: 128px; --space-16: 160px;

  /* Radius */
  --radius-xs: 4px; --radius-sm: 8px; --radius-md: 12px; --radius-lg: 16px;
  --radius-xl: 20px; --radius-2xl: 24px; --radius-full: 9999px;

  /* Shadows - Multi-layer realism */
  --shadow-xs: 0 1px 2px oklch(0 0 0 / 0.06);
  --shadow-sm: 0 1px 3px oklch(0 0 0 / 0.08), 0 1px 2px -1px oklch(0 0 0 / 0.08);
  --shadow-md: 0 4px 6px -1px oklch(0 0 0 / 0.1), 0 2px 4px -2px oklch(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px oklch(0 0 0 / 0.1), 0 4px 6px -4px oklch(0 0 0 / 0.1);
  --shadow-xl: 0 20px 25px -5px oklch(0 0 0 / 0.1), 0 8px 10px -6px oklch(0 0 0 / 0.1);
  --shadow-focus: 0 0 0 2px var(--bg-surface), 0 0 0 4px var(--accent);

  /* Typography */
  /* Replace with a project-specific typeface per Phase 4 — this stack is a
     functional fallback only, not a default to ship (see 1.1). */
  --font-sans: ui-sans-serif, system-ui, -apple-system, 'Segoe UI', sans-serif;
  --font-display: ui-serif, Georgia, 'Times New Roman', serif;
  --font-mono: ui-monospace, 'SFMono-Regular', Menlo, monospace;

  --text-xs: 12px; --text-sm: 14px; --text-base: 16px; --text-lg: 20px;
  --text-xl: 25px; --text-2xl: 31px; --text-3xl: 39px;
  --text-4xl: 49px; --text-5xl: 61px; --text-6xl: 76px;
  --leading-tight: 1.1; --leading-snug: 1.2; --leading-normal: 1.5; --leading-relaxed: 1.65;
  --tracking-tight: -0.02em; --tracking-normal: 0em; --tracking-wide: 0.02em;

  /* Colors - Light Mode OKLCH + Hex Fallbacks
     Neutral scaffold only — swap accent hue and neutrals in Phase 4. */
  --bg-base: oklch(0.985 0.002 0); /* #fafafa */
  --bg-surface: oklch(1 0 0); /* #ffffff */
  --bg-surface-hover: oklch(0.98 0 0); /* #f5f5f5 */
  --bg-subtle: oklch(0.965 0.002 0); /* #f0f0f0 */
  --text-primary: oklch(0.15 0 0); /* #1a1a1a */
  --text-secondary: oklch(0.45 0 0); /* #666666 */
  --text-tertiary: oklch(0.60 0 0); /* #999999 */
  --border-default: oklch(0.91 0 0); /* #e5e5e5 */
  --accent: oklch(0.60 0.20 250); /* #2563eb */
  --accent-hover: oklch(0.55 0.20 250); /* #1d4ed8 */
  --accent-active: oklch(0.50 0.20 250); /* #1e40af */
  --accent-subtle: oklch(0.95 0.04 250); /* #eff6ff */
  --success: oklch(0.65 0.15 145); --warning: oklch(0.80 0.14 85);
  --danger: oklch(0.60 0.20 25); --info: oklch(0.65 0.15 230);

  /* Motion */
  --duration-micro: 150ms; --duration-fast: 200ms; --duration-base: 250ms;
  --duration-moderate: 350ms; --duration-slow: 500ms;
  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);

  /* Z-Index Scale */
  --z-base: 0; --z-dropdown: 10; --z-sticky: 20; --z-overlay: 30;
  --z-modal: 40; --z-popover: 50; --z-toast: 60; --z-tooltip: 70;
}

/* Dark Mode - Engineered, Not Inverted */
@media (prefers-color-scheme: dark) {
  :root {
    --bg-base: oklch(0.12 0 0); /* #1a1a1a */
    --bg-surface: oklch(0.17 0 0); /* #262626 */
    --bg-surface-hover: oklch(0.20 0 0); /* #333333 */
    --bg-subtle: oklch(0.20 0.005 0); /* #2d2d2d */
    --text-primary: oklch(0.96 0 0); /* #f5f5f5 */
    --text-secondary: oklch(0.70 0 0); /* #aaaaaa */
    --text-tertiary: oklch(0.55 0 0); /* #808080 */
    --border-default: oklch(0.24 0 0); /* #3d3d3d */
    --accent: oklch(0.68 0.15 250); /* #3b82f6 */
    --accent-hover: oklch(0.72 0.15 250); /* #60a5fa */
    --accent-active: oklch(0.76 0.15 250); /* #93c5fd */
    --accent-subtle: oklch(0.22 0.05 250); /* #1e3a5f */
    --shadow-sm: 0 1px 3px oklch(0 0 0 / 0.5);
    --shadow-md: 0 8px 24px oklch(0 0 0 / 0.5);
  }
}

/* Component Example - Production Ready */
.btn-primary {
  background: var(--accent); color: white; border-radius: var(--radius-md);
  padding: 0 var(--space-6); height: 44px; font-weight: 500;
  transition: all var(--duration-micro) var(--ease-out);
}
.btn-primary:hover { background: var(--accent-hover); transform: translateY(-1px); box-shadow: var(--shadow-md); }
.btn-primary:active { transform: scale(0.98); background: var(--accent-active); }
.btn-primary:focus-visible { box-shadow: var(--shadow-focus); outline: none; }
.btn-primary:disabled { opacity: 0.5; pointer-events: none; }
```
