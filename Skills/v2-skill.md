---
name: UI Design Engineering v2
description: >
  Treat interface design as an engineering discipline, not taste. Every decision
  justified by cognitive psychology, HCI, optical perception, mathematical systems,
  accessibility, platform conventions, and business goals. Adapts design language to
  brand, audience, and creative direction while engineering production-ready,
  emotionally-aligned interfaces. Complete system with tokens, components, motion,
  responsive, and validation.
---

# UI Design Engineering v2 - Production Standard

## 0. Philosophy - The Law
A good interface is not decoration. It is a system where:
- Every spacing value has meaning
- Every color has a purpose (brand / hierarchy / state)
- Every type choice affects trust and reading speed
- Every animation communicates relationship or feedback
- Every component behaves predictably

Laws:
- Beautiful but confusing = failure.
- Functional but bland = incomplete.
- Great = Usable + Emotional + Intentional.
- Design should feel obvious before users understand why.

## 1. Anti-Default & Anti-Generic (BLOCKING - Enforce First)

### 1.1 Forbidden Defaults
Never force same visual language onto every project. Unless explicitly requested:
FORBIDDEN:
- Generic SaaS: centered hero, gradient mesh, 3 feature cards, logos cloud
- Glassmorphism everywhere + purple/blue glow + dark bg + white cards
- Same Inter / Geist / identical 16px/24px rhythm
- Identical card shadows, identical radius, identical animations
- Hero -> Features -> Testimonials -> Pricing -> FAQ clone

Test: Can you swap your design from fintech to gaming and it still works? Then you failed.

### 1.2 Reference Adaptation - Extract Principles, Not Pixels
When prompt says "like Apple/Stripe/Linear" etc:

Apple: minimalism, premium perception, large intentional spacing, refined typography, smooth transitions, product-focused storytelling, high-quality imagery. Avoid just white bg + rounded cards.

Stripe: technical confidence, structured layouts, developer-oriented communication, strong information hierarchy, controlled gradients, precise interactions.

Linear: high information density, productivity focus, keyboard-first, precision, professional minimalism.

Notion: calm interface, content priority, flexible organization, low visual noise.

Gaming: strong contrast, energy, feedback, expressive visuals, emotional engagement.

Luxury: restrained palette, premium materials, large spacing, elegant typography, slow intentional motion.

Cyberpunk/Futuristic: dramatic lighting, neon accents, technology feeling, strong atmosphere, high contrast.

Brutalist: intentional imperfection, strong typography, visible structure, purposeful rule-breaking.

Goal is not imitation. Goal is understanding design logic behind reference.

## 2. Workflow - Mandatory 5 Phases

### Phase 1: Context Analysis (Do this in thinking, 30s)
User: target audience, knowledge level, expectations, main problems, emotional state.
Platform: Web / Mobile Web / iOS / Android / Desktop / Tablet - each changes density, nav, touch targets.
Product: category, main objective, business model, conversion goal, north star metric.
Experience: cognitive friction points, required emotional response (trust? excitement? calm?), creativity level needed, expected interaction style.

Example: Enterprise analytics dashboard and mobile game store cannot use same hierarchy, density, or interaction model.

### Phase 2: Intent Detection
Classify before visuals:
- Design style: Professional, Premium, Futuristic, Playful, Experimental, Corporate, Artistic, Minimal, Dense, Editorial
- Visual atmosphere: calm, energetic, premium, technical, warm, cold
- Creativity level: low (banking) to high (portfolio, game)
- Technical req: high density? keyboard-first? touch-first?

Never assume minimalism is answer. Correct design language depends on product.

### Phase 3: Structural Blueprint (Before ANY color/gradient/shadow)
Define:
- User goals: what users see first, understand first, need to complete
- Information hierarchy:
  Primary: value prop, primary action, core status, main objective - strongest position/contrast
  Secondary: features, benefits, explanations, comparisons
  Tertiary: docs, resources, secondary links, advanced options
- Content organization: text length, image purpose, data complexity, reading behavior
- Layout: page structure, grid system (12-col desktop, 4-col mobile), content density, nav model, section hierarchy, interaction zones
- Flow: Discovery > Understanding > Exploration > Decision > Action > Feedback > Return usage

Every section must justify existence. If it doesn't support user understanding, user action, storytelling, or business -> delete.

### Phase 4: Style Matching
Choose visual system FROM prompt, not habit. Must match brand identity, audience, product category, emotional objective, platform requirements, business goals.

### Phase 5: Production Engineering
Build as senior front-end engineer. Final result immediately usable. No empty sections, fake buttons, missing navigation, unfinished components, placeholder blocks, "coming soon" unless explicitly requested.

---

## 3. Design System - Complete

### 3.1 Spacing Engineering - 8pt System
Primary: 4, 8, 16, 24, 32, 48, 64, 96, 128
Exception 4px: only for icon alignment, border adjustments, micro typography corrections. Never to compensate poor structure.

Rules:
- Small 4-8px: closely connected (icon+label, input+helper, button icon+text)
- Medium 16-32px: component organization (card sections, form groups, nav items)
- Large 48-128px: major separation (page sections, hero areas, different content groups)

Whitespace is active design element. Creates focus, hierarchy, calmness, premium perception.

Bad: margin: 17px; padding: 29px; Good: margin: 16px; padding: 32px;

### 3.2 Typography Engineering
Typography is structural system, not decoration. Affects trust, reading speed, brand perception, hierarchy, emotion.

Modular Scale: Default 1.25 Major Third
12px Caption, 14px Small, 16px Body, 20px H4, 25px H3, 31px H2, 39px H1, 52px Display
Adapt scale depending on platform, brand personality, content density, audience.

Readability:
- Line length: 45-75 chars, ideal max-width 65ch
- Body: 1.5-1.6 line-height
- Headings: 1.1-1.2 line-height
- Dense interfaces: 1.2
Avoid: extremely wide blocks, tiny unreadable text, poor contrast, walls of text.

Typography Adaptation:
- Luxury: elegant proportions, large titles, refined spacing, light weights
- Technical: clear hierarchy, efficient density, strong readability, mono accents
- Playful: expressive, strong personality, dynamic rhythm
- Editorial: strong composition, comfortable reading, storytelling focus
- Corporate: consistent, reliable, neutral

### 3.3 Color Engineering
Colors must have functional purpose: brand identity, importance, emotion, interaction, status. Never decoration only.

System: Prefer OKLCH / HSL for token definition (perceptual), Hex for final implementation.
60/30/10 Rule: 60% neutral background, 30% secondary/brand, 10% accent.

Accent Usage: primary actions, important states, key information, interactive elements ONLY. Overuse removes hierarchy.

Adaptation:
- Premium: lower saturation, restrained palette, subtle contrast
- Energetic: stronger chroma, clear accents, high impact
- Calm: soft neutrals, lower contrast, relaxed rhythm
- Experimental: unusual combos, strong contrast, controlled balance

Dark Mode Engineering:
Dark mode is NOT inverted light mode. Needs own design.
Rules: avoid pure black everywhere, reduce saturated colors 20-30%, maintain readable contrast, avoid vibration, use shadows carefully, preserve hierarchy.
Create depth using: background layers, surface elevation, borders, contrast differences. Avoid making every element same shade.

### 3.4 Motion Design - Communication Tool
Motion is communication, not decoration. Every animation must: explain relationship, provide feedback, guide attention, improve understanding, create emotional alignment, confirm user actions.

Timing System:
- Micro: 150-250ms - buttons, hover, small transitions, toggles, input feedback
- Page: 300-500ms - navigation changes, large content transitions, section reveals

Easing:
- Entering: ease-out (decelerate, feels natural)
- Leaving: ease-in
- Avoid linear (mechanical)

Adaptation:
- Premium: smooth, controlled, refined, subtle effects, avoid excessive
- Playful: slightly bouncy, expressive, unexpected
- Futuristic: precise, crisp, tech-inspired
- Editorial: minimal motion, elegant reveals, low distraction
- Gaming: fast feedback, strong reactions, energetic

Performance: Prefer transform + opacity (GPU). Avoid animating width/height/top/left excessively.

### 3.5 Layout Architecture
Define: page structure, grid system, content density, navigation model, section hierarchy, interaction zones.
Consider: alignment, balance, rhythm, whitespace, visual grouping, scanning behavior (F-pattern, Z-pattern), reading patterns.
Layout should naturally guide attention. Users should not need to search for important information.

Responsive:
- Mobile requires larger touch targets, clear priorities, reduced complexity, efficient navigation
- Desktop can support higher density, advanced controls, multi-column, keyboard shortcuts
- Never simply shrink desktop. Adapt hierarchy, navigation, density, spacing, interactions.

### 3.6 Gestalt & Composition
- Proximity: related elements visually close
- Similarity: similar elements look consistent
- Continuity: guide eye naturally
- Closure: allow understanding incomplete patterns
- Figure-Ground: separate important elements from backgrounds

Evaluate alignment, balance, whitespace, rhythm, proportion, grouping, symmetry/asymmetry. Layout is not decoration, composition controls attention.

## 4. Component Engineering - Production Spec

Design systems must work at component level. Should be consistent, reusable, predictable, accessible, scalable.

Every component defines: purpose, sizes, variants, states, spacing, radius, shadows, typography, interactions, a11y behavior.

### 4.1 Buttons
Must communicate importance, action, state.

Primary: main actions, conversions, main user goals - highest contrast, filled
Secondary: alternative actions, supporting choices - outlined or low fill
Tertiary: low-priority, navigation-like - text only

States mandatory:
- Default: normal
- Hover: subtle brightness increase (filter: brightness 1.08) or y:-1px
- Focus: visible keyboard outline 2px solid + offset
- Active: scale(0.98) feedback
- Disabled: 40-50% opacity, cursor not-allowed
- Loading: skeleton or spinner, disable interaction

Sizes: sm 32px, md 40-44px (default), lg 48-52px. Min touch 44x44.

### 4.2 Inputs & Forms
Types: text, select, textarea, checkbox, radio, switch.
Anatomy: label (always visible), input, helper text, error (icon+text+color), optional icon.
States: default, hover, focus (ring), active, disabled, error, success, loading.
Accessibility: label linked via for/id, aria-describedby for helper/error, never placeholder as label.

### 4.3 Cards, Tables, Navigation
Cards: consistent radius/shadow/type. Avoid random redesign. Define header/body/footer, spacing internal 16-24px, hover if interactive.
Tables: header sticky, row hover, density options, sortable indicators, empty state.
Navigation: clear active state, keyboard accessible, mobile drawer pattern.

### 4.4 Feedback Components
Badges, Toasts, Modals, Empty states, Loading states, Error states - all require design, not afterthought.

## 5. Design Tokens - Production Kit

### 5.1 Token Principles
Must be consistent, reusable, scalable, easy to modify. Never scatter random values.

Use: spacing, radius, shadows, fonts, colors, transitions, surfaces, borders, focus rings, elevation levels.

Example:
Bad: border-radius: 14px; Good: radius-md
Bad: color: #ff5500; Good: color-accent-primary

### 5.2 Complete Token Set - Copy/Paste Ready

```css
:root{
  /* Spacing - 8pt */
  --space-1: 4px; --space-2: 8px; --space-3: 16px; --space-4: 24px;
  --space-5: 32px; --space-6: 48px; --space-7: 64px; --space-8: 96px; --space-9: 128px;

  /* Radius */
  --radius-xs: 6px; --radius-sm: 8px; --radius-md: 16px; --radius-lg: 24px; --radius-xl: 32px; --radius-full: 999px;

  /* Shadows - layered for elevation */
  --shadow-xs: 0 1px 2px hsla(0 0% 0% / 0.06);
  --shadow-sm: 0 2px 8px hsla(0 0% 0% / 0.06), 0 1px 2px hsla(0 0% 0% / 0.04);
  --shadow-md: 0 4px 16px hsla(0 0% 0% / 0.08), 0 2px 6px hsla(0 0% 0% / 0.06);
  --shadow-lg: 0 12px 32px hsla(0 0% 0% / 0.12), 0 4px 12px hsla(0 0% 0% / 0.08);
  --shadow-xl: 0 24px 64px hsla(0 0% 0% / 0.16);

  /* Typography */
  --font-sans: Inter, ui-sans, system-ui, -apple-system, sans-serif;
  --font-mono: JetBrains Mono, ui-monospace, monospace;
  --text-xs: 12px; --text-sm: 14px; --text-base: 16px; --text-lg: 20px; --text-xl: 25px; --text-2xl: 31px; --text-3xl: 39px; --text-4xl: 48px;
  --leading-tight: 1.1; --leading-snug: 1.2; --leading-normal: 1.5; --leading-relaxed: 1.65;
  --tracking-tight: -0.02em; --tracking-normal: 0em; --tracking-wide: 0.02em;

  /* Colors - OKLCH for perceptual consistency */
  --bg-base: oklch(0.985 0 0); --bg-surface: oklch(1 0 0); --bg-subtle: oklch(0.97 0 0);
  --text-primary: oklch(0.18 0 0); --text-secondary: oklch(0.48 0 0); --text-tertiary: oklch(0.62 0 0);
  --border-default: oklch(0.92 0 0); --border-strong: oklch(0.88 0 0);
  --accent: oklch(0.62 0.22 250); --accent-hover: oklch(0.58 0.22 250); --accent-subtle: oklch(0.95 0.04 250);
  --success: oklch(0.65 0.15 145); --warning: oklch(0.78 0.15 85); --danger: oklch(0.62 0.22 25);

  /* Motion */
  --duration-micro: 150ms; --duration-base: 250ms; --duration-page: 400ms;
  --ease-out: cubic-bezier(.16,1,.3,1); --ease-in: cubic-bezier(.4,0,1,1); --ease-spring: cubic-bezier(.34,1.56,.64,1);
  --focus-ring: 0 0 0 2px var(--bg-surface), 0 0 0 4px var(--accent);
}
@media (prefers-color-scheme: dark){
  :root{
    --bg-base: oklch(0.16 0 0); --bg-surface: oklch(0.20 0 0); --bg-subtle: oklch(0.23 0 0);
    --text-primary: oklch(0.96 0 0); --text-secondary: oklch(0.70 0 0); --text-tertiary: oklch(0.55 0 0);
    --border-default: oklch(0.26 0 0); --border-strong: oklch(0.32 0 0);
    --accent: oklch(0.68 0.16 250); --accent-hover: oklch(0.72 0.16 250);
    --shadow-md: 0 8px 24px hsla(0 0% 0% / 0.4);
  }
}
```

## 6. Cognitive Load & Hierarchy

### Hick's Law: Too many choices increase decision time. Reduce unnecessary options, confusing navigation, duplicate actions.
### Miller's Law: Users have limited short-term memory (7±2). Organize into meaningful groups. Avoid overwhelming unstructured lists.
### Progressive Disclosure: Show complexity gradually. Reveal advanced options only when needed. Don't expose everything immediately.

Visual Hierarchy via size, contrast, position, spacing, typography, motion.
Questions: Is primary action obvious? Does user know where to look first? Are important elements prioritized? Can interface be scanned quickly?

## 7. Accessibility - Non-Negotiable

A11y is part of design quality. Never sacrifice unless explicitly requested for artistic experimentation, and even then creative must still be usable.

- Interactive States: Default / Hover / Focus / Active / Disabled / Loading - all mandatory
- Semantic HTML: Use <button>, <nav>, <main>, <section>, <article>, <footer>. Avoid div as button.
- Touch Targets: Minimum 44x44 CSS pixels. Easy on mobile/tablet/touch.
- Color A11y: Never rely only on color. Error = red indicator + warning icon + clear message.
- Contrast: Check contrast ratio, focus visibility, text readability in light, dark, high contrast.
- Keyboard: All interactive elements reachable, logical order, visible focus.

## 8. Performance Engineering
Good design must be efficient. Beautiful slow interface = bad interface. Performance is part of UX.

Consider: loading speed, rendering efficiency, asset optimization, animation performance, network usage, device limitations.

Core Web Vitals:
- LCP: Ensure main content appears quickly. Optimize images, font loading, server response, critical resource priority.
- CLS: Prevent unexpected movement. Avoid images without dimensions, late-loading shifting layouts, dynamic elements without reserved space.
- INP: Keep interactions responsive. Improve JS efficiency, event handling, animation performance, component rendering.

Assets: SVG for icons/simple graphics, WebP/AVIF for images, proper dimensions, responsive images, lazy loading. Never load unnecessary heavy assets.
Fonts: loading strategy, limit weights, variable fonts, fallback fonts. Avoid many unnecessary font files.

## 9. Content First & UX Writing
Interfaces are products, not mockups. Never design empty structures. Content defines interface.

Before layouts, understand: what info user needs, what problem solves, what actions must complete, what message must communicate, what info has priority.

Never generate placeholder unless explicitly requested. Avoid: Lorem Ipsum, generic marketing copy, empty cards, fake statistics, meaningless metrics, placeholder images without purpose, decorative sections with no value.

Every element must support either: user understanding, user action, product storytelling, business objectives.

UX Writing: text is part of interface. Good writing reduces confusion and helps users complete tasks. Voice must match brand, be clear, concise, action-oriented.

## 10. Critique Frameworks - Self Review Before Ship

Never critique with vague "Looks clean." Evaluate with principles.

Cognitive Load Review: too many choices? poor grouping? info overload? confusing actions? Ask: Does this reduce or increase mental effort?

Visual Hierarchy Review: primary action visibility? information priority? natural scanning path? content importance? Ask: Does user's eye move in correct order?

Spatial Mathematics Review: 8pt grid consistency? typography scale? line length? alignment? section rhythm? proportions? Ask: Do measurements feel intentional?

Accessibility Review: contrast ratio? keyboard navigation? focus states? touch targets? color a11y? screen reader? Ask: Can different users use this?

Style Matching Review: does interface match prompt? visual language fits audience? feels intentional? avoids generic AI patterns? Ask: Was design adapted or default template used?

Performance Review: loading speed? asset size? animation efficiency? layout stability? responsiveness? Ask: Does interface feel fast?

## 11. Final Validation - BLOCKING
Before producing final result, verify YES to all:
- Does design match requested style?
- Does it fit target audience?
- Is interface original (not template)?
- Is hierarchy clear?
- Is accessibility preserved?
- Is every visual choice intentional and tokenized?
- Does it contain meaningful real content?
- Does it feel like a real product?
- Did design adapt to prompt?
- Does it avoid generic AI-generated patterns?
- All states present (hover/focus/active/disabled/loading/empty/error/success)?
- Responsive 320-2560px considered?
- Performance considered?

If any NO -> revise before delivering.

## 12. Creativity Scaling
Never maximize creativity by default. Correct level depends on product.

Professional: clarity, trust, efficiency
Premium: elegance, refinement, emotional quality
Futuristic: innovation, new interaction patterns, technology feeling
Experimental: originality, exploration, controlled disruption
Playful: expression, personality, delight
Corporate: consistency, reliability, scalability
Artistic: emotion, storytelling, unique identity
