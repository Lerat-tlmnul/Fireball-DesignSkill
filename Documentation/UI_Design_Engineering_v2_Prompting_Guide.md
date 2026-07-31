# Master Prompting Guide: UI Design Engineering v2 Frameworks

## Executive Overview
The **UI Design Engineering v2** framework suite transforms interface generation from an arbitrary aesthetic effort into a deterministic engineering discipline. Designed around cognitive psychology, human-computer interaction (HCI), spatial mathematics, and modern web accessibility (WCAG 2.2), this operating system eliminates generic, AI-default aesthetics in favor of context-aware, production-ready design systems.

The framework exists in three specialized tiers:
1. **v2 Standard (UI Design Engineering v2)**: The balanced, production-standard operating model.
2. **v2 ULTRA (UI Design Engineering v2 ULTRA)**: The zero-compromise, comprehensive OS for maximal detail, full design systems, and rigorous component specifications.
3. **v2 ECO (UI Design Engineering v2 ECO)**: The token-efficient, condensed variant designed for rapid iteration, budget token constraints, or lower context-window capacity.

---

## 1. System Architecture & Tier Comparison

| Dimension | v2 ECO | v2 Standard | v2 ULTRA |
| :--- | :--- | :--- | :--- |
| **Token Footprint** | Extremely Low (~35 lines) | Medium (~250 lines) | High (~600 lines) |
| **Primary Focus** | Speed, token budget, direct rules | Complete end-to-end design engineering | Deep systemization, complete token kits, WCAG 2.2, audit checklists |
| **Workflow Phases** | 4 Condensed Steps | 5 Structured Phases | 5 Deeply Engineered Phases |
| **Design Tokens** | Basic scalar tables (Spacing, Radius, Motion) | CSS Variable Kit (OKLCH/HSL) | Full Design Token OS (Light/Dark OKLCH, layered depth, typography ratios) |
| **Component Specs** | Core states & touch targets | Standard interactive states & basic layouts | Granular state matrix, component anatomy, accessible micro-interactions |
| **Auditing / Critique** | 8-Point Fast Checklist | Section 10/11 Review Criteria | 16-Point Blocking Checklist & Self-Audit Framework |
| **Best Used For** | Quick components, simple cards, rapid prototypes, API budget saving | Full web pages, complex apps, design systems, balanced code generation | Enterprise-grade applications, multi-page flows, zero-placeholder code generation |

---

## 2. Core Operational Mechanics

Across all tiers, the engine operates on **Blocking Laws** that govern output generation. Understanding these mechanics is essential for crafting optimal input prompts.

### 2.1 The Anti-Default Engine (Blocking Rules)
When presented with a generic prompt (e.g., *"Design a dashboard"*), unguided LLMs default to predictable visual patterns:
* Centered hero sections with translucent cards (glassmorphism spam).
* Diagonal purple-to-blue gradients on dark backgrounds.
* Identical Inter font set at `16px/24px` line rhythm.
* Generic 3-column card layouts with identical dropped shadows.

The **UI Design Engineering v2** engine explicitly blocks these defaults. If a gaming dashboard, a luxury e-commerce site, and a high-frequency trading platform look visually identical, the output is classified as a system failure.

### 2.2 Reference Adaptation Logic
When you reference major design languages, the system extracts **underlying architectural principles**, not direct visual imitation:
* **Apple**: Large intentional spacing, visual calm, product-focused storytelling, refined typography hierarchy.
* **Stripe**: Technical authority, structured layouts, developer-centric information density, controlled accents.
* **Linear**: High information density, keyboard-first navigation patterns, crisp precision, extreme contrast.
* **Notion**: Calm interfaces, content primacy, low visual noise, structural flexibility.
* **Luxury**: Restrained color palettes, wide spatial breathing room, elegant serif display ratios, slow motion curves.
* **Technical / Trading**: Mono-spaced numeric alignment, high data density, immediate functional feedback.

### 2.3 The Content-First Law
Placeholders (e.g., *Lorem Ipsum*, "Heading Text", fake statistics, empty cards) degrade design decisions. Spatial choices, typography line-lengths, and layout grids must respond to real content context. Input prompts should supply or request production-grade copy and domain-specific data.

---

## 3. The 5-Phase Prompting Methodology

To maximize output quality, structure your prompt inputs to feed the framework's internal execution pipeline.

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        THE 5-PHASE PIPELINE                             │
├──────────────┬──────────────┬──────────────┬──────────────┬─────────────┤
│   Phase 1    │   Phase 2    │   Phase 3    │   Phase 4    │   Phase 5   │
│   Context    │    Intent    │ Structural   │    Style     │ Production  │
│  Analysis    │  Detection   │  Blueprint   │  Matching    │ Engineering │
└──────────────┴──────────────┴──────────────┴──────────────┴─────────────┘
```

### Phase 1: Context Analysis
Specify the user persona, platform target, product category, and cognitive environment:
* **Target Audience**: Expert traders, first-time users, elderly patients, enterprise admins.
* **Platform Context**: Mobile touch (44px min targets), Desktop density, iOS HIG, Web.
* **Cognitive State**: Fast decision-making under stress, relaxed discovery, focused reading.

### Phase 2: Intent Classification
Explicitly declare the **Design Intent** to trigger the engine's adaptation matrix:
* **Professional**: Clarity, trust, structured 8pt grid, restrained visual hierarchy.
* **Premium**: Generous whitespace, refined ratios, muted OKLCH palettes, subtle elevation.
* **Technical**: High information density, monospace numeric alignment, functional status accents.
* **Playful**: High-chroma accents, expressive dynamic rhythm, elastic motion curves.
* **Editorial**: Reading optimization (45-75 character line length, 1.6 leading), storytelling layout.
* **Futuristic / Cyberpunk**: Dramatic environmental contrast, crisp atmospheric lighting, high-impact focus state.

### Phase 3: Structural Blueprinting
Define content hierarchy prior to styling:
* **Primary (60%)**: Key performance indicator, main value proposition, primary call to action.
* **Secondary (30%)**: Supporting trends, list items, comparative metrics.
* **Tertiary (10%)**: Metadata, documentation links, secondary utility navigation.

### Phase 4 & 5: Style Tokens & Production Engineering
Instruct the engine to generate complete token variables (OKLCH, 8pt spacing system) and fully responsive, semantically correct markup (`<main>`, `<nav>`, `<section>`, `<article>`, `<button>`).

---

## 4. Prompt Engineering Templates

### 4.1 Master Template (Full / Production Use)
Use this comprehensive structure when prompting for complete web applications, dashboards, or design systems.

```markdown
### 1. PRODUCT CONTEXT
- **Product Name/Type**: [e.g., ApexMetrics - B2B Financial Risk Analytics]
- **Primary Goal**: [e.g., Enable risk officers to audit portfolio exposure in real time]
- **Target Audience**: [e.g., Financial analysts working on multi-monitor desktop setups]
- **Primary Action (CTA)**: [e.g., "Execute Rebalance"]

### 2. DESIGN INTENT & VISUAL SYSTEM
- **Intent Keyword**: [Professional | Premium | Technical | Playful | Editorial | Luxury]
- **Theme Mode**: [Dark Mode Native | Light Mode | System Adaptive]
- **Inspiration Principles**: [e.g., Linear precision with Stripe technical trust]
- **Color Rules**: Follow 60/30/10 ratio. Primary neutral background, subtle surface elevations, functional status colors (Success/Warning/Danger in OKLCH).

### 3. CONTENT & STRUCTURE (Anti-Placeholder)
- **Primary Focus Area**: [e.g., Real-time exposure value ($4,821,090.00) with 24h delta (+2.4%)]
- **Secondary Content**: [e.g., Risk breakdown table (Asset, Exposure, VaR, Status)]
- **Tertiary Content**: [e.g., Audit trail log, export trigger, timestamp badge]
- **Copy Mandate**: No Lorem Ipsum. Generate domain-accurate financial terminology.

### 4. TECHNICAL SPECIFICATIONS
- **Grid System**: Strict 8pt spatial distribution (4, 8, 16, 24, 32, 48, 64px).
- **Typography**: Modular scale 1.250 (Major Third), tabular figures (`font-variant-numeric: tabular-nums`) for financial data, line length bounded to 65ch max for blocks.
- **Interactive States**: Full implementation of Default, Hover (`brightness 1.08` or `translateY(-1px)`), Focus-visible (`2px ring + offset`), Active (`scale(0.98)`), Disabled (`opacity 0.5`), and Loading states.
- **Accessibility**: WCAG 2.2 AA compliant contrast ratios, min 44px touch targets, semantic HTML elements.

### 5. DELIVERABLE FORMAT
- [Production-ready HTML + Tailwind CSS / Fully self-contained HTML with CSS Variables]
```

---

### 4.2 Compact Template (Quick Iterations & Components)
Use this streamlined structure for single components, modals, or fast UI blocks.

```markdown
**Task**: Build a [Component Name, e.g., Multi-Factor Authentication Modal] using UI Design Engineering v2.

- **Design Intent**: [e.g., Technical / High Trust]
- **Platform**: [Desktop / Mobile Responsive]
- **Key Elements**: [Header, 6-digit pin input with auto-focus ring, Resend code countdown timer, Primary 'Verify' button, Secondary 'Cancel' button]
- **Execution Rules**:
  1. Enforce strict 8pt grid spacing.
  2. Implement interactive states (Hover, Focus-Visible ring, Active scale-down, Disabled).
  3. Use OKLCH color variables for dark mode surface depth.
  4. Provide real UX copy (no placeholder text).
```

---

## 5. Tier-Specific Prompting Strategies

### 5.1 Prompting for v2 ECO
* **Objective**: Fast generation, minimal context token usage, concise code.
* **Strategy**: Use direct intent triggers and reference the compact token table directly.

```markdown
[Skill System: UI Design Engineering v2 ECO]
Target: E-commerce Product Card
Intent: Premium
Parameters: 8pt spacing (16px padding, 24px gap), 45-75ch readability, 60/30/10 color rule.
Content: Real product data for an artisanal espresso machine ($1,299).
Deliverable: Clean HTML/CSS with hover transform and active click feedback.
```

### 5.2 Prompting for v2 Standard
* **Objective**: Balanced production code, complete page structures, clear visual hierarchy.
* **Strategy**: Provide structured domain context and demand explicit 5-phase execution.

```markdown
[Skill System: UI Design Engineering v2 Standard]
Apply Phase 1 to Phase 5 workflow to design a SaaS User Management Settings Page.
- Intent: Professional
- Key Flow: User Discovery > Role Assignment > Access Confirmation
- Requirements: 
  - Standard CSS variables with dark mode support.
  - Interactive table with sticky headers, status badges, and pagination.
  - Complete accessible button variants (Primary, Secondary, Danger).
```

### 5.3 Prompting for v2 ULTRA
* **Objective**: Enterprise systems, bulletproof accessibility, complete component states, zero-compromise quality.
* **Strategy**: Trigger the 16-point blocking checklist and demand full token systems.

```markdown
[Skill System: UI Design Engineering v2 ULTRA]
Execute full UI Engineering OS for an AI Prompt Execution Dashboard.
- Intent: Technical / Futuristic
- Required Outputs:
  1. Full Root Design Tokens (OKLCH color system, typography scale, layered shadow elevation).
  2. Complete HTML structure using semantic landmarks (<main>, <nav>, <section>, <aside>).
  3. Interactive state matrix for all UI components (Default, Hover, Focus-visible, Active, Disabled, Loading, Error).
  4. Perform strict Self-Audit against the 16-Point Blocking Checklist prior to output finalization.
```

---

## 6. Real-World Prompting Examples

### Example 1: High-Density Fintech Dashboard (v2 ULTRA)

#### Input Prompt
```markdown
[System: UI Design Engineering v2 ULTRA]

I need a high-density foreign exchange (FX) trading workspace for professional currency traders.

1. CONTEXT & INTENT
- Intent: Technical
- Audience: Professional FX traders monitoring high-volatility currency pairs.
- Spatial Requirement: High information density, compact 8pt spacing (4px micro gaps, 8px element padding, 16px container padding).

2. CONTENT REQUIREMENTS (Real Data)
- Pair Header: EUR/USD | Spot: 1.08452 | 24h High: 1.08910 | 24h Low: 1.08120 | Delta: +0.31%
- Interactive Order Form: Buy/Sell toggle, Order Type (Market, Limit, Stop-Loss), Quantity field (Lots), Calculated Margin Requirement.
- Open Positions Table: Ticket ID, Pair, Type (BUY/SELL), Size, Entry Price, Mark Price, UnPKL ($), Action buttons (Close, Modify).

3. SYSTEM CONSTRAINTS
- Typography: Monospace numerical tabular figures for pricing to eliminate layout jitter.
- Color System: Dark mode native. Neutral dark surfaces (`oklch(0.14 0 0)`), high-contrast text (`oklch(0.96 0 0)`), green status (`oklch(0.68 0.18 145)`), red status (`oklch(0.62 0.22 25)`).
- Accessibility: Focus-visible rings must pass WCAG 2.2 AA on dark surfaces.
- Output: Production-ready single-file HTML/CSS.
```

---

### Example 2: Minimalist Editorial Article Reader (v2 Standard)

#### Input Prompt
```markdown
[System: UI Design Engineering v2 Standard]

Design an editorial reading layout for an architectural long-form essay.

1. CONTEXT & INTENT
- Intent: Editorial / Minimal
- Audience: Design professionals and architectural historians.
- Core Goal: Maximize reading focus and cognitive comfort over 10-minute sessions.

2. SPECIFICATIONS
- Line Length: Bound main body copy strict max-width to 65ch, centered layout.
- Typography: Modular scale 1.250. Serif display headers paired with clean sans-serif body copy. Line height 1.65.
- Spacing: Large spatial breathing room (32px paragraph separation, 64px section dividers, 96px header top margin).
- Palette: Light mode warm cream palette (`--bg-base: oklch(0.985 0.005 80)`), deep charcoal text (`--text-primary: oklch(0.20 0.005 80)`).
- Details: Include estimated reading time indicator, progress indicator bar, and subtle pull-quote callouts.
```

---

## 7. Troubleshooting & Quality Tuning

When reviewing output from the framework, evaluate it against the **Self-Audit Criteria**. Use these targeted follow-up prompts to refine output if issues arise:

### Issue: Layout looks generic or resembles standard SaaS
* **Correction Prompt**: *"The generated layout uses default SaaS card structures. Re-apply Section 1.1 Anti-Default Laws. Shift the Design Intent to [Technical / Editorial / Premium] and rebuild the spatial system using non-standard grid compositions."*

### Issue: Inconsistent spacing or alignment
* **Correction Prompt**: *"Audit spatial metrics against Section 3.1 (8pt Grid System). Eliminate all non-system values (e.g., 13px, 17px, 29px) and replace them with standard token steps (4, 8, 16, 24, 32, 48px)."*

### Issue: Missing interactive component states
* **Correction Prompt**: *"The primary action button lacks interactive depth. Implement the complete interactive state matrix from Section 4: Default, Hover (brightness boost), Focus-visible (2px offset ring), Active (scale 0.98), and Disabled (opacity 0.5)."*

---

## Summary Checklist for Prompt Creators

Before issuing a prompt to any **UI Design Engineering v2** tier, verify:
- [ ] Have I declared an explicit **Design Intent** (e.g., Technical, Premium, Editorial)?
- [ ] Is the prompt populated with **real domain copy** rather than placeholders?
- [ ] Have I specified the target **platform and interaction model** (Touch vs. Desktop)?
- [ ] Is the desired **deliverable format** (HTML/Tailwind, CSS Variables, Component code) clear?
- [ ] Have I chosen the appropriate **framework tier** (ECO, Standard, ULTRA) for my context limit?
