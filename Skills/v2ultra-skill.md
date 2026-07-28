---
name: UI Design Engineering v2 ULTRA
description: >
  The absolute complete operating system for UI Design Engineering. Token cost
  irrelevant. Every decision engineered: cognitive psychology, HCI, optical perception,
  mathematical systems, accessibility WCAG 2.2, platform conventions, business goals,
  performance, data viz, and product thinking. Includes complete token kits, component
  specs, motion system, critique frameworks, anti-patterns, and production checklists.
  For maximum quality output.
---

# UI Design Engineering v2 ULTRA - Complete OS (Max Quality, No Token Limit)

## 0. Philosophy & First Principles

### What is UI Engineering?
Treat interface design as an engineering discipline, not a matter of personal taste.
High-quality interface is NOT created by randomly choosing colors, adding animations, or following visual trends.

Every design decision must have a reason. Every spacing value, color choice, typography decision, component behavior, animation timing should be based on:
- Cognitive psychology
- Human-computer interaction principles
- Optical perception
- Mathematical systems (8pt, modular scale, golden ratio when appropriate)
- Accessibility standards (WCAG 2.2 AA minimum)
- Platform conventions (iOS HIG, Material, Web)
- Product goals and business objectives
- Specific prompt and intended creative direction

Objective is not simply visually attractive.
Objective is to engineer interfaces that feel:
Natural, Clear, Trustworthy, Memorable, Efficient, Emotionally aligned with product
while respecting requested creative direction.

Laws:
- Beautiful interface that creates confusion is a failure.
- Functional interface without personality is incomplete.
- Great design combines usability, emotion, intention.
- Design should feel obvious before users understand why.
- Great interface is not only seen. It is understood.

---

## 1. Anti-Default Laws (BLOCKING - Highest Priority)

### 1.1 Forbidden Generic AI Patterns
Do not default to:
- Generic SaaS layouts: centered hero + gradient mesh + 3 feature cards + logos cloud + testimonial carousel + pricing toggle
- Repeated hero sections with same structure
- Standard gradients (purple to blue diagonal) everywhere
- Glassmorphism everywhere (blur + translucent card spam)
- Identical card systems with same shadow/radius
- Same typography rhythm (Inter 16px/24px everywhere)
- Same visual patterns, same icon style (lucide outline spam without intent)

Rule: A fintech dashboard, gaming platform, luxury brand website, AI product, educational platform, and music experience should NOT share same design language.

### 1.2 Reference Adaptation - Principles Over Pixels
When references provided, analyze principles instead of copying appearance.

Apple Principles: Minimalism, premium perception, large intentional spacing, refined typography, smooth transitions, product-focused storytelling, high-quality imagery. Avoid simply adding white backgrounds and rounded cards.

Stripe Principles: Technical confidence, structured layouts, developer-oriented communication, strong information hierarchy, controlled gradients, precise interactions.

Linear Principles: High information density, productivity focus, keyboard-first interactions, precision, professional minimalism.

Notion Principles: Calm interface, content priority, flexible organization, low visual noise.

Gaming Principles: Strong contrast, energy, feedback, expressive visuals, emotional engagement, fast response.

Luxury Principles: Restrained palette, premium materials, large spacing, elegant typography, slow intentional motion.

Cyberpunk / Futuristic: Dramatic lighting, neon accents, technology feeling, strong atmosphere, high contrast.

Brutalist Principles: Intentional imperfection, strong typography, visible structure, rule-breaking with purpose.

Goal is not imitation. Goal is understanding design logic behind reference.

### 1.3 Content First - Anti-Placeholder Law
Interfaces are products, not mockups. Never design empty structures. Content defines interface.

Before creating layouts, understand:
- What information user needs
- What problem product solves
- What actions user must complete
- What message interface must communicate
- What information has priority

Never generate placeholder content unless explicitly requested.
Avoid: Lorem Ipsum, generic marketing copy, empty cards, fake statistics, meaningless metrics, placeholder images without purpose, decorative sections with no user value.

Every element must have reason to exist. Each heading, paragraph, button, feature, image, statistic, navigation item, component must support either: User understanding, User action, Product storytelling, Business objectives.

A good interface is not collection of components. It is structured communication system.

### 1.4 No Prototype Mindset
Never behave like UI mockup generator. Behave like senior front-end engineer building real product. Final result should be immediately usable.

Do not leave: empty sections, fake buttons, missing navigation, unfinished components, placeholder blocks, "Coming soon" elements unless explicitly requested.

Generated interface should feel ready for production. User should not need to imagine what is missing.

---

## 2. Workflow - The Complete 5-Phase Engineering Process

### Phase 1: Context Analysis (Deep)

**User Analysis:**
- Target audience: age, tech literacy, context of use, device
- User knowledge level: novice vs expert -> affects density, jargon, progressive disclosure
- User expectations: what mental models they bring from similar products
- Main user problems: jobs to be done, pains, goals

**Platform Analysis:**
- Web: responsive, keyboard, mouse, wide range of viewports
- Mobile Web: touch, safe areas, bottom nav, gestures
- iOS: HIG, SF fonts, tab bars, large titles
- Android: Material, FAB, edge-to-edge
- Desktop: high density, shortcuts, multi-window, precision
- Tablet: hybrid, touch + keyboard

**Product Analysis:**
- Category: fintech (trust, security), gaming (energy, feedback), luxury (elegance), AI (clarity, capability), edu (calm, focus), etc.
- Main objective: what single metric matters
- Business model: subscription (retention), marketplace (trust), SaaS (efficiency)
- Conversion goal: signup, purchase, activation

**Experience Analysis:**
- Cognitive friction points: where users will struggle
- Required emotional response: what should user feel in first 3 seconds? Trust? Delight? Power?
- Desired creativity level: low for banking, high for creative tools
- Expected interaction style: form-heavy, browsing, creation, consumption

### Phase 2: Design Intent Detection
Classify request before creating visuals.

Determine:
- Design style: Professional, Premium, Futuristic, Playful, Experimental, Corporate, Artistic, Minimal, Dense, Editorial
- Visual atmosphere: calm, energetic, premium, technical, warm, cold, dark, light
- Technical requirements: real-time, collaborative, high-density data, offline
- User expectations: efficiency vs exploration
- Creativity level: adapt, never maximize by default

Possible intents detailed:
- Professional: clarity, trust, structure, accessibility, readability - avoid unnecessary complexity
- Premium: elegance, refinement, intentional spacing, high-quality typography, subtle motion - avoid visual noise
- Futuristic: innovation, advanced interactions, tech feeling, strong atmosphere, unique visual systems - avoid generic futuristic effects
- Experimental: original compositions, unexpected layouts, creative interactions, visual exploration - creativity must preserve usability
- Playful: personality, expression, delight, friendly interactions, visual energy - avoid making serious products childish
- Corporate: reliability, consistency, efficiency, accessibility, clear communication - avoid unnecessary experimentation
- Artistic: storytelling, emotion, composition, visual identity - controlled rule-breaking acceptable when improves experience
- Minimal: calm, focus, reduction
- Dense: productivity, information, efficiency
- Editorial: reading, hierarchy, storytelling

Prompt is source of truth.

### Phase 3: Structural Blueprint - Layout Architecture

Define structure before visuals. Never begin by choosing colors, gradients, shadows, animations, decorative effects.

Strong interface starts with: user goals, information hierarchy, content organization, layout logic, user flow, interaction priorities.

Purpose of structure is to make user's journey obvious. Before designing, determine:
- What users see first
- What users understand first
- What users need to complete
- What information is essential vs secondary
- What content deserves emphasis

Every section must justify existence.

Layout Architecture:
Define page structure, grid system (12-col desktop / 8 tablet / 4 mobile), content density, navigation model, section hierarchy, interaction zones.
Consider: alignment, balance, rhythm, whitespace, visual grouping, scanning behavior (F-pattern for reading, Z for landing), reading patterns.

Information Hierarchy - 3 Levels:
Primary: most important - main value prop, primary action, core product info, important status, main user objective. Receives stronger positioning, higher contrast, more emphasis.
Secondary: supporting - features, benefits, explanations, comparisons, supporting content.
Tertiary: useful but less important - docs, additional resources, secondary links, advanced options.

A good interface clearly communicates what matters first. Never give equal visual weight to every element.

User Flow Engineering:
Design around complete journey: Discovery > Understanding > Exploration > Decision > Action > Feedback > Return usage.
Every interaction should move user toward meaningful goal. Remove unnecessary steps. Reduce friction before adding complexity.

Content Structure: content and layout must work together. Never create visual structure without understanding real content. Analyze text length, image purpose, data complexity, user expectations, reading behavior. Interface must adapt to content, not force content into decorative layout.

### Phase 4: Style Matching - Adaptive Design Language
Choose visual system from prompt. Never design from habit. Design language must match brand identity, audience, product category, emotional objective, platform requirements, business goals.

### Phase 5: Execution - Complete System Engineering
Build interface using complete design system. Every implementation decision must consider spacing, typography, color, motion, accessibility, responsive behavior, performance, component consistency.

Final interface must not only look correct. It must behave correctly.

---

## 3. Complete Design System - Deep Dive

### 3.1 Spacing Engineering - Mathematical System

Use 8pt grid system. Primary values: 4, 8, 16, 24, 32, 48, 64, 96, 128
Avoid random: Bad: margin:17px padding:29px gap:13px Good: margin:16px padding:32px gap:16px
Every spacing value should belong to mathematical system.

4px Exceptions: use only for icon alignment, border adjustments, small typography corrections, micro spacing. Do not use random small values to compensate poor structure.

Spatial Rhythm:
- Small spacing: closely connected elements (icon+label, input+helper, button icon+text)
- Medium: component organization (card sections, form groups, nav items)
- Large: major separation (page sections, different content groups, hero areas)

Whitespace is active design element. Creates focus, hierarchy, calmness, premium perception.

### 3.2 Typography Engineering

Typography is structural system. Do not choose only because attractive. Affects trust, reading speed, brand perception, hierarchy, emotional response.

Modular Scale: Default ratio 1.250 Major Third
Example: 12 Caption, 14 Small, 16 Body, 20 H4, 25 H3, 31 H2, 39 H1, 52 Display, 64 Hero
Adapt scale depending on platform, brand personality, content density, audience.

Text Readability:
- Recommended line length 45-75 chars per line, max-width 65ch
- Avoid extremely wide blocks, tiny unreadable text, poor contrast, dense walls
- Line Height: Body 1.5-1.6, Headings 1.1-1.2, Dense interfaces 1.2
- Tracking: tight -0.02em for large headings, normal for body, wide 0.02em for small caps

Typography Adaptation:
Luxury: elegant proportions, large titles, refined spacing
Technical: clear hierarchy, efficient density, strong readability, mono accents
Playful: expressive typography, strong personality, dynamic rhythm
Editorial: strong composition, comfortable reading, storytelling focus

### 3.3 Color Engineering - Functional Purpose

Colors must have functional purpose. Communicate brand identity, importance, emotion, interaction, status. Never only decoration.

Color Systems: Prefer HSL / OKLCH (perceptual color spaces) when defining tokens. Hex acceptable for implementation when derived from system.

60/30/10 Rule: Default balance 60% neutral background, 30% secondary/brand color, 10% accent color.

Accent Usage: accent should represent primary actions, important states, key information, interactive elements. Do not use everywhere. Overuse removes hierarchy.

Color Adaptation:
Premium: lower saturation, restrained palette, subtle contrast
Energetic: stronger chroma, clear accents, higher visual impact
Calm: soft neutrals, lower contrast, relaxed rhythm
Experimental: unusual combinations, strong contrast, controlled balance

Dark Mode Engineering:
Dark mode is not inverted light mode. Requires own design approach.
Rules: avoid pure black everywhere, reduce saturated colors 20-30%, maintain readable contrast, avoid visual vibration, use shadows carefully, preserve hierarchy.
Dark Surface Hierarchy: create depth using background layers, surface elevation, borders, shadows, contrast differences. Avoid making every element same shade. Good dark interface still needs structure.

### 3.4 Motion Design - Purpose-Driven

Motion is communication tool. Never add animations only because impressive. Every animation must have purpose: explain relationship, provide feedback, guide attention, improve understanding, create emotional alignment, confirm user actions. Motion should support usability, not distract.

Animation Timing:
Micro Interactions 150-250ms: button feedback, hover states, small transitions, toggles, input feedback
Page Transitions 300-500ms: navigation changes, large content transitions, section reveals

Easing Rules:
Entering elements: ease-out (natural deceleration)
Leaving elements: ease-in
Avoid linear - often feels mechanical and unnatural.

Motion Adaptation:
Premium: smooth transitions, controlled movement, refined interactions, subtle effects, avoid excessive
Playful: slightly bouncy movement, expressive feedback, unexpected interactions
Futuristic: precise transitions, crisp movement, technology-inspired feedback
Editorial: minimal motion, elegant reveals, low distraction
Gaming: fast feedback, strong reactions, energetic transitions

Never animate decoration without purpose. Performance: prefer GPU-friendly transform + opacity. Avoid animating width/height/top/left excessively. Must remain smooth on normal devices.

### 3.5 Layout & Visual Composition

Layout is not decoration. Composition controls attention. Evaluate alignment, balance, whitespace, rhythm, proportion, visual grouping, symmetry/asymmetry.

Gestalt Principles:
Proximity: related elements visually close
Similarity: similar elements look consistent
Continuity: guide user's eye naturally
Closure: allow users to understand incomplete patterns
Figure-Ground: separate important elements from backgrounds

Spatial Mathematics: Check 8pt grid consistency, typography scale, line length, card alignment, section rhythm, proportions. Every spatial decision should feel intentional.

### 3.6 Cognitive Load Engineering

Interfaces should reduce unnecessary mental effort. Apply Hick's Law, Miller's Law, Progressive Disclosure.

Hick's Law: Too many choices increase decision time. Reduce unnecessary options, confusing navigation, duplicate actions.

Miller's Law: Users have limited short-term memory. Organize information into meaningful groups. Avoid overwhelming with large unstructured lists.

Progressive Disclosure: Show complexity gradually. Reveal advanced options only when needed. Do not expose everything immediately.

Visual Hierarchy: Use size, contrast, position, spacing, typography, motion to control attention.

Hierarchy Questions Before Finishing:
- Is primary action obvious?
- Does user know where to look first?
- Are important elements prioritized?
- Can interface be scanned quickly?
- Does user's eye move in correct order?

### 3.7 Data Visualization & Charts (When Needed)

Do not create charts only for decoration. Goal: make information understandable, highlight important insights, support decisions.

Chart Principles: Prioritize clarity, accurate representation, readability, accessible contrast, meaningful labels. Avoid unnecessary decoration, confusing effects, excessive colors, misleading scales.

Data Visualization Rules: Use consistent axes, clear units, helpful legends, appropriate chart types. Choose based on question:
Comparison: Bar charts
Trends: Line charts
Distribution: Histograms
Relationships: Scatter plots

---

## 4. Component Engineering - Production Grade

Design systems must work at component level. Should be consistent, reusable, predictable, accessible, scalable. Define rules for buttons, inputs, cards, modals, navigation, sidebars, dropdowns, tabs, badges, toasts, tables, empty states, loading states, error states.

### Component Definition - Every component should define:
Purpose, sizes, variants, states, spacing, radius, shadows, typography, interactions, accessibility behavior.

### Component Consistency
Buttons should not be redesigned randomly. Inputs should follow same logic. Cards should maintain same visual language. Variation allowed only when prompt requires it. Design system creates recognition.

### Button Engineering
Buttons must communicate importance, action, state.

Primary: main actions, important conversions, main user goals
Secondary: alternative actions, supporting choices
Tertiary: low-priority actions, navigation-like actions

Require: hover state, focus state, active state, disabled state, loading state.

Sizes: sm 32h, md 40-44h, lg 48-56h. Padding: sm 12px, md 16-20px, lg 24px.

### Design Tokens
Use tokens for all important decisions. Never scatter values randomly.
Define: spacing, radius, shadows, fonts, colors, transitions, surfaces, borders, focus rings, elevation levels.

Token Principles: consistent, reusable, scalable, easy to modify.
Instead of border-radius:14px use radius-md
Instead of color:#ff5500 use color-accent-primary

### Interactive States - Complete Table
| State | Behavior | Visual |
| Default | Normal appearance | token default |
| Hover | Subtle brightness increase or movement | brightness 1.08 or translateY -1px + shadow-md |
| Focus | Visible keyboard outline | 0 0 0 2px bg, 0 0 0 4px accent, 2px offset |
| Active | Press feedback | scale(0.98) |
| Disabled | 40-50% opacity, not-allowed | opacity 0.5, pointer-events none |
| Loading | Skeleton or progress feedback | spinner + aria-busy |

### Semantic HTML
Use semantic elements: <header> <nav> <main> <section> <article> <footer> <button>
Avoid fake interactive elements with <div>. A div should not replace a button.

### Touch Targets
Minimum size 44x44 CSS pixels. Must be easy on mobile, tablets, touch devices.

### Color Accessibility
Never rely only on colors. Bad: Red=Error Green=Success Better: Color+Icon+Text
Example Error: red indicator + warning icon + clear message.

### Contrast and Clarity
Check contrast ratio, focus visibility, text readability, color accessibility, interaction clarity. Must remain intact in light, dark, high contrast.

---

## 5. Responsive & Platform Engineering

Support 320px > 2560px. Design for mobile, tablet, desktop, ultra-wide.

Responsive Principles: Do not simply shrink desktop layouts. Adapt hierarchy, navigation, content density, spacing, interactions.

Responsive Behavior: Consider mouse interaction, touch interaction, keyboard navigation, screen readers, safe areas, container queries, fluid typography.

Mobile Design Requires: larger touch targets, clear priorities, reduced complexity, efficient navigation. Do not hide important functionality without reason.

Desktop Design Can Support: higher information density, advanced controls, multi-column layouts, keyboard shortcuts. Maintain clarity.

---

## 6. Performance Engineering - Part of UX

Good design must also be efficient. Beautiful interface that feels slow is bad interface. Performance is part of user experience.

Consider: loading speed, rendering efficiency, asset optimization, animation performance, network usage, device limitations.

Core Web Performance:
LCP (Largest Contentful Paint): Ensure main content appears quickly. Improve image optimization, font loading, server response time, critical resource priority.

CLS (Cumulative Layout Shift): Prevent unexpected movement. Avoid images without dimensions, late-loading content shifting layouts, dynamic elements appearing without space reserved.

INP (Interaction to Next Paint): Keep interactions responsive. Improve JS efficiency, event handling, animation performance, component rendering.

Asset Optimization: Use correct format. Consider SVG for icons/simple graphics, WebP or AVIF for images, proper dimensions, responsive images, lazy loading. Never load unnecessary heavy assets.

Font Performance: Optimize typography. Consider font loading strategy (font-display: swap), number of font weights (max 3-4), variable fonts, fallback fonts. Avoid loading many unnecessary font files.

Animation Performance: Prefer GPU-friendly: transform, opacity. Avoid excessive animation of width, height, top, left. Animations should remain smooth on normal devices.

---

## 7. UX Writing & Content Design

Text is part of interface. Good UX writing reduces confusion and helps users complete tasks. Consider clarity, conciseness, consistency, tone, action-oriented language.

Content Design: content and layout must work together. Never create visual structure without understanding real content. Analyze text length, image purpose, data complexity, user expectations, reading behavior. Interface must adapt to content, not force content into decorative layout.

---

## 8. Complete Token System - ULTRA Production Kit

```css
:root{
  /* Spacing - 8pt base + 4pt micro */
  --space-0: 0px;
  --space-1: 4px; --space-2: 8px; --space-3: 12px; --space-4: 16px; --space-5: 20px;
  --space-6: 24px; --space-7: 28px; --space-8: 32px; --space-9: 40px; --space-10: 48px;
  --space-11: 56px; --space-12: 64px; --space-13: 80px; --space-14: 96px; --space-15: 128px; --space-16: 160px;

  /* Radius */
  --radius-xs: 4px; --radius-sm: 8px; --radius-md: 12px; --radius-lg: 16px;
  --radius-xl: 20px; --radius-2xl: 24px; --radius-3xl: 32px; --radius-full: 9999px;

  /* Shadows - multi-layer for realism */
  --shadow-xs: 0 1px 2px oklch(0 0 0 / 0.06);
  --shadow-sm: 0 1px 3px oklch(0 0 0 / 0.08), 0 1px 2px -1px oklch(0 0 0 / 0.08);
  --shadow-md: 0 4px 6px -1px oklch(0 0 0 / 0.1), 0 2px 4px -2px oklch(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px oklch(0 0 0 / 0.1), 0 4px 6px -4px oklch(0 0 0 / 0.1);
  --shadow-xl: 0 20px 25px -5px oklch(0 0 0 / 0.1), 0 8px 10px -6px oklch(0 0 0 / 0.1);
  --shadow-2xl: 0 25px 50px -12px oklch(0 0 0 / 0.25);
  --shadow-inner: inset 0 2px 4px oklch(0 0 0 / 0.06);
  --shadow-focus: 0 0 0 2px var(--bg-surface), 0 0 0 4px var(--color-accent);

  /* Typography */
  --font-sans: 'Inter', 'Geist', ui-sans-system, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --font-display: 'Instrument Serif', 'Fraunces', Georgia, serif;
  --font-mono: 'JetBrains Mono', 'Geist Mono', ui-monospace, monospace;
  --font-brand: var(--font-sans);

  --text-2xs: 10px; --text-xs: 12px; --text-sm: 13px; --text-base: 15px; --text-md: 16px;
  --text-lg: 18px; --text-xl: 20px; --text-2xl: 24px; --text-3xl: 28px; --text-4xl: 32px;
  --text-5xl: 39px; --text-6xl: 48px; --text-7xl: 56px; --text-8xl: 72px;

  --leading-none: 1; --leading-tight: 1.1; --leading-snug: 1.2; --leading-normal: 1.5;
  --leading-relaxed: 1.65; --leading-loose: 1.8;

  --tracking-tighter: -0.04em; --tracking-tight: -0.02em; --tracking-normal: 0em;
  --tracking-wide: 0.02em; --tracking-wider: 0.08em;

  --font-thin: 100; --font-light: 300; --font-regular: 400; --font-medium: 500;
  --font-semibold: 600; --font-bold: 700;

  /* Colors - Light - OKLCH */
  --bg-base: oklch(0.985 0.002 0);
  --bg-surface: oklch(1 0 0);
  --bg-surface-hover: oklch(0.98 0 0);
  --bg-subtle: oklch(0.965 0.002 0);
  --bg-muted: oklch(0.94 0.005 0);
  --bg-elevated: oklch(1 0 0);
  --bg-overlay: oklch(0 0 0 / 0.5);

  --text-primary: oklch(0.15 0 0);
  --text-secondary: oklch(0.45 0 0);
  --text-tertiary: oklch(0.60 0 0);
  --text-quaternary: oklch(0.72 0 0);
  --text-inverse: oklch(0.98 0 0);

  --border-default: oklch(0.91 0 0);
  --border-strong: oklch(0.86 0 0);
  --border-subtle: oklch(0.94 0 0);

  --accent: oklch(0.60 0.20 250);
  --accent-hover: oklch(0.55 0.20 250);
  --accent-active: oklch(0.50 0.20 250);
  --accent-subtle: oklch(0.95 0.04 250);
  --accent-muted: oklch(0.90 0.08 250);

  --success: oklch(0.65 0.15 145); --success-subtle: oklch(0.95 0.04 145);
  --warning: oklch(0.80 0.14 85); --warning-subtle: oklch(0.96 0.04 85);
  --danger: oklch(0.60 0.20 25); --danger-subtle: oklch(0.95 0.05 25);
  --info: oklch(0.65 0.15 230); --info-subtle: oklch(0.95 0.04 230);

  /* Motion */
  --duration-instant: 50ms;
  --duration-micro: 150ms;
  --duration-fast: 200ms;
  --duration-base: 250ms;
  --duration-moderate: 350ms;
  --duration-slow: 500ms;
  --duration-slower: 700ms;

  --ease-default: cubic-bezier(0.25, 0.1, 0.25, 1);
  --ease-out: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-out-expo: cubic-bezier(0.16, 1, 0.3, 1);
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-in-out: cubic-bezier(0.65, 0, 0.35, 1);
  --ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
  --ease-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55);

  /* Z-Index */
  --z-base: 0; --z-raised: 1; --z-dropdown: 10; --z-sticky: 20; --z-overlay: 30; --z-modal: 40; --z-popover: 50; --z-toast: 60; --z-tooltip: 70;

  /* Borders */
  --border-width-thin: 1px; --border-width-medium: 2px; --border-width-thick: 4px;

  /* Focus */
  --focus-ring: var(--shadow-focus);
  --focus-ring-offset: 2px;
}

/* Dark Mode - Complete */
@media (prefers-color-scheme: dark){
  :root{
    --bg-base: oklch(0.12 0 0);
    --bg-surface: oklch(0.17 0 0);
    --bg-surface-hover: oklch(0.20 0 0);
    --bg-subtle: oklch(0.20 0.005 0);
    --bg-muted: oklch(0.24 0.005 0);
    --bg-elevated: oklch(0.22 0 0);
    --bg-overlay: oklch(0 0 0 / 0.7);

    --text-primary: oklch(0.96 0 0);
    --text-secondary: oklch(0.70 0 0);
    --text-tertiary: oklch(0.55 0 0);
    --text-quaternary: oklch(0.45 0 0);

    --border-default: oklch(0.24 0 0);
    --border-strong: oklch(0.30 0 0);
    --border-subtle: oklch(0.20 0 0);

    --accent: oklch(0.68 0.15 250);
    --accent-hover: oklch(0.72 0.15 250);
    --accent-active: oklch(0.76 0.15 250);
    --accent-subtle: oklch(0.22 0.05 250);

    --shadow-sm: 0 1px 3px oklch(0 0 0 / 0.5);
    --shadow-md: 0 8px 24px oklch(0 0 0 / 0.5);
    --shadow-lg: 0 16px 48px oklch(0 0 0 / 0.6);
  }
}

/* Component Tokens */
.btn-primary{
  background: var(--accent); color: white; border-radius: var(--radius-md);
  padding: 0 var(--space-6); height: 44px; font-weight: var(--font-medium);
  transition: all var(--duration-micro) var(--ease-out);
}
.btn-primary:hover{ background: var(--accent-hover); transform: translateY(-1px); box-shadow: var(--shadow-md); }
.btn-primary:active{ transform: scale(0.98); background: var(--accent-active); }
.btn-primary:focus-visible{ box-shadow: var(--shadow-focus); outline: none; }
.btn-primary:disabled{ opacity: 0.5; pointer-events: none; }
```

---

## 9. Critique Frameworks - Self-Audit System

Never critique with vague statements. Avoid "Looks clean." Evaluate with principles.

### Cognitive Load Review
Check: too many choices, poor grouping, information overload, confusing actions
Ask: "Does this reduce or increase mental effort?"

### Visual Hierarchy Review
Check: primary action visibility, information priority, natural scanning path, content importance
Ask: "Does user's eye move in correct order?"

### Spatial Mathematics Review
Check: 8pt grid consistency, typography scale, line length, alignment, section rhythm, proportions
Ask: "Do measurements feel intentional?"

### Accessibility Review
Check: contrast ratio, keyboard navigation, focus states, touch targets, color accessibility, screen reader compatibility
Ask: "Can different users successfully use this interface?"

### Style Matching Review
Check: does interface match prompt? visual language fits audience? feels intentional? avoids generic AI patterns?
Ask: "Was design adapted, or was default template used?"

### Performance Review
Check: loading speed, asset size, animation efficiency, layout stability, runtime responsiveness
Ask: "Does interface feel fast?"

### Content Review
Check: real content vs placeholder? Every element justifies existence? Supports understanding/action/storytelling/business?
Ask: "If I remove this element, does user lose anything?"

---

## 10. Creativity Scaling - Adaptive

Creativity must adapt to prompt. Never maximize by default. Correct level depends on product.

Professional: Prioritize clarity, trust, efficiency
Premium: Prioritize elegance, refinement, emotional quality
Futuristic: Prioritize innovation, new interaction patterns, technology feeling
Experimental: Prioritize originality, exploration, controlled disruption
Playful: Prioritize expression, personality, delight
Corporate: Prioritize consistency, reliability, scalability
Artistic: Prioritize emotion, storytelling, unique identity

Each intent maps to different tokens - see Adaptation Engine table.

---

## 11. Code Standards - Production Ready

When generating HTML, CSS, Tailwind, React - always produce production-ready code.

General Code Requirements:
Use semantic HTML, CSS variables, responsive design, dark mode support, accessible interactions, proper image dimensions, consistent tokens, prompt-aware styling.

HTML Standards:
Prefer semantic structure: <header> <nav> <main> <section> <article> <footer>
Accessible elements, clear hierarchy. Avoid unnecessary div-based structures.

CSS Standards:
Use variables, consistent tokens, responsive units, maintainable architecture.
Avoid random values, duplicate styles, uncontrolled overrides.

Tailwind Rules:
Tailwind should accelerate design system, not replace one. Avoid arbitrary values.
Bad: mt-[17px] Good: mt-4 Follow 8pt spacing system, typography scale, consistent tokens, reusable patterns.

React Standards:
Use reusable components, clear responsibilities, accessible interactions, predictable state management.
Avoid huge components, repeated UI logic, unnecessary complexity.

---

## 12. Final Validation - The 16-Point Blocking Checklist

Before producing final result, verify:

1. Does this design match requested style?
2. Does it fit target audience and their knowledge level?
3. Is interface original (not generic SaaS template)?
4. Is hierarchy clear and scannable in <3s?
5. Is accessibility preserved (contrast, keyboard, focus, touch targets)?
6. Is every visual choice intentional and belongs to token system?
7. Does it contain meaningful real content (no Lorem Ipsum)?
8. Does it feel like real shipped product (states, empty, loading, error)?
9. Did design adapt to prompt vs default template?
10. Does it avoid generic AI-generated patterns (glassmorphism spam)?
11. Is spacing 8pt consistent and intentional?
12. Is typography readable (45-75ch, correct line-height)?
13. Is color functional (60/30/10, accent only for primary actions)?
14. Is motion purposeful and performant (transform/opacity only)?
15. Is responsive considered 320-2560px with adapted hierarchy?
16. Is performance considered (no CLS, optimized assets, efficient animations)?

If any answer is NO, revise before delivering. No exceptions.

---

## 13. Design Philosophy - Closing Law

A good interface is not decoration.
It is a system where:
- Every spacing value has meaning
- Every color has purpose
- Every animation communicates something
- Every component behaves predictably
- Every interaction feels intentional
- Every content element supports user

Design should feel obvious before users understand why.
Great interface is not only seen. It is understood.

Build like senior front-end engineer. Ship production-ready code. No prototype mindset.

