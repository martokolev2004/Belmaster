---
name: ui-ux-pro-max
description: UI/UX design intelligence. 67 styles, 161 palettes, 57 font pairings, 25 charts, 16 stacks (React, Next.js, Vue, Svelte, Astro, SwiftUI, React Native, Flutter, Nuxt, Nuxt UI, Tailwind, shadcn/ui, Jetpack Compose, Three.js, Angular, Laravel). Actions: plan, build, create, design, implement, review, fix, improve, optimize, enhance, refactor, check UI/UX code. Projects: website, landing page, dashboard, admin panel, e-commerce, SaaS, portfolio, blog, mobile app, .html, .tsx, .vue, .svelte. Elements: button, modal, navbar, sidebar, card, table, form, chart. Styles: glassmorphism, claymorphism, minimalism, brutalism, neumorphism, bento grid, dark mode, responsive, skeuomorphism, flat design. Topics: color palette, accessibility, animation, layout, typography, font pairing, spacing, hover, shadow, gradient. Integrations: shadcn/ui MCP for component search and examples.
---

# UI/UX Pro Max - Design Intelligence

Comprehensive design guide for web and mobile applications. Contains 67 styles, 161 color palettes, 57 font pairings, 99 UX guidelines, and 25 chart types across 16 technology stacks. Searchable database with priority-based recommendations.

## When to Apply

Use this Skill when the task involves **UI structure, visual design decisions, interaction patterns, or UX quality control**.

### Must Use

- Designing new pages (Landing Page, Dashboard, Admin, SaaS, Mobile App)
- Creating or refactoring UI components (buttons, modals, forms, tables, charts)
- Selecting color schemes, font systems, spacing, or layout systems
- Reviewing UI code for UX, accessibility, or visual consistency
- Implementing navigation structure, animations, or responsive behavior
- Making product-level design decisions (style, information hierarchy, brand expression)
- Improving perceived quality, clarity, or usability of an interface

### Recommended

- UI looks "unprofessional" but cause is unclear
- Received usability or experience feedback
- Pre-launch UI quality optimization
- Cross-platform design alignment (Web / iOS / Android)
- Building a design system or reusable component library

### Skip

- Pure backend logic development
- API or database design only
- Performance optimizations unrelated to UI
- Infrastructure or DevOps work
- Non-visual scripts or automation tasks

**Rule of thumb**: If the task changes how something **looks, feels, moves, or is interacted with**, use this Skill.

---

## Key Workflow

**Step 1: Analyze Requirements**
Extract product type, target audience, style keywords, and tech stack from user requests.

**Step 2: Apply Design System**
Use the priority table below to select the right rules for the context.

**Step 3: Apply Stack Guidelines**
Apply platform-specific best practices (React, React Native, SwiftUI, Flutter, etc.).

**Step 4: Enforce Professional Standards**
- Icons: Use vector-based icons (Phosphor, Heroicons, Lucide) — never emojis for structural elements
- Touch targets: Minimum 44×44pt (iOS) or 48×48dp (Android)
- Contrast: 4.5:1 ratio for primary text in both light and dark modes
- Animation timing: 150–300ms micro-interactions with native-feeling easing
- Safe areas: Respect device safe areas for fixed headers, tab bars, and content

---

## Rule Categories by Priority

| Priority | Category | Impact | Key Checks (Must Have) | Anti-Patterns (Avoid) |
|----------|----------|--------|------------------------|------------------------|
| 1 | Accessibility | CRITICAL | Contrast 4.5:1, Alt text, Keyboard nav, Aria-labels | Removing focus rings, Icon-only buttons without labels |
| 2 | Touch & Interaction | CRITICAL | Min size 44×44px, 8px+ spacing, Loading feedback | Reliance on hover only, Instant state changes (0ms) |
| 3 | Performance | HIGH | WebP/AVIF, Lazy loading, Reserve space (CLS < 0.1) | Layout thrashing, Cumulative Layout Shift |
| 4 | Style Selection | HIGH | Match product type, Consistency, SVG icons (no emoji) | Mixing flat & skeuomorphic randomly, Emoji as icons |
| 5 | Layout & Responsive | HIGH | Mobile-first breakpoints, Viewport meta, No horizontal scroll | Horizontal scroll, Fixed px container widths, Disable zoom |
| 6 | Typography & Color | MEDIUM | Base 16px, Line-height 1.5, Semantic color tokens | Text < 12px body, Gray-on-gray, Raw hex in components |
| 7 | Animation | MEDIUM | Duration 150–300ms, Motion conveys meaning, Spatial continuity | Decorative-only animation, Animating width/height, No reduced-motion |
| 8 | Forms & Feedback | MEDIUM | Visible labels, Error near field, Helper text, Progressive disclosure | Placeholder-only label, Errors only at top, Overwhelm upfront |
| 9 | Navigation Patterns | HIGH | Predictable back, Bottom nav ≤5, Deep linking | Overloaded nav, Broken back behavior, No deep links |
| 10 | Charts & Data | LOW | Legends, Tooltips, Accessible colors | Relying on color alone to convey meaning |

---

## Quick Reference

### 1. Accessibility (CRITICAL)

- `color-contrast` — Minimum 4.5:1 ratio for normal text (large text 3:1)
- `focus-states` — Visible focus rings on interactive elements (2–4px)
- `alt-text` — Descriptive alt text for meaningful images
- `aria-labels` — aria-label for icon-only buttons; accessibilityLabel in native
- `keyboard-nav` — Tab order matches visual order; full keyboard support
- `form-labels` — Use label with for attribute
- `skip-links` — Skip to main content for keyboard users
- `heading-hierarchy` — Sequential h1→h6, no level skip
- `color-not-only` — Don't convey info by color alone (add icon/text)
- `dynamic-type` — Support system text scaling; avoid truncation as text grows
- `reduced-motion` — Respect prefers-reduced-motion; reduce/disable animations
- `voiceover-sr` — Meaningful accessibilityLabel/accessibilityHint; logical reading order
- `escape-routes` — Provide cancel/back in modals and multi-step flows
- `keyboard-shortcuts` — Preserve system and a11y shortcuts

### 2. Touch & Interaction (CRITICAL)

- `touch-target-size` — Min 44×44pt (Apple) / 48×48dp (Material); extend hit area beyond visual bounds
- `touch-spacing` — Minimum 8px/8dp gap between touch targets
- `hover-vs-tap` — Use click/tap for primary interactions; don't rely on hover alone
- `loading-buttons` — Disable button during async operations; show spinner or progress
- `error-feedback` — Clear error messages near problem
- `cursor-pointer` — Add cursor-pointer to clickable elements (Web)
- `tap-delay` — Use touch-action: manipulation to reduce 300ms delay (Web)
- `standard-gestures` — Use platform standard gestures consistently
- `system-gestures` — Don't block system gestures (Control Center, back swipe, etc.)
- `press-feedback` — Visual feedback on press (ripple/highlight)
- `haptic-feedback` — Use haptic for confirmations; avoid overuse
- `safe-area-awareness` — Keep primary touch targets away from notch, Dynamic Island, gesture bar
- `no-precision-required` — Avoid requiring pixel-perfect taps on small icons

### 3. Performance (HIGH)

- `image-optimization` — Use WebP/AVIF, responsive images (srcset/sizes), lazy load non-critical assets
- `image-dimension` — Declare width/height or use aspect-ratio to prevent layout shift (CLS)
- `font-loading` — Use font-display: swap/optional to avoid invisible text (FOIT)
- `critical-css` — Prioritize above-the-fold CSS
- `lazy-loading` — Lazy load non-hero components via dynamic import / route-level splitting
- `bundle-splitting` — Split code by route/feature (React Suspense / Next.js dynamic)
- `reduce-reflows` — Avoid frequent layout reads/writes; batch DOM reads then writes
- `virtualize-lists` — Virtualize lists with 50+ items
- `main-thread-budget` — Keep per-frame work under ~16ms for 60fps
- `progressive-loading` — Use skeleton screens / shimmer for >1s operations
- `input-latency` — Keep input latency under ~100ms for taps/scrolls
- `debounce-throttle` — Use debounce/throttle for high-frequency events

### 4. Style Selection (HIGH)

- `style-match` — Match style to product type
- `consistency` — Use same style across all pages
- `no-emoji-icons` — Use SVG icons (Heroicons, Lucide), not emojis
- `color-palette-from-product` — Choose palette from product/industry
- `effects-match-style` — Shadows, blur, radius aligned with chosen style
- `platform-adaptive` — Respect platform idioms (iOS HIG vs Material)
- `state-clarity` — Make hover/pressed/disabled states visually distinct
- `elevation-consistent` — Use a consistent elevation/shadow scale
- `dark-mode-pairing` — Design light/dark variants together
- `icon-style-consistent` — Use one icon set/visual language across the product
- `primary-action` — Each screen should have only one primary CTA

### 5. Layout & Responsive (HIGH)

- `viewport-meta` — width=device-width initial-scale=1 (never disable zoom)
- `mobile-first` — Design mobile-first, then scale up to tablet and desktop
- `breakpoint-consistency` — Use systematic breakpoints (375 / 768 / 1024 / 1440)
- `readable-font-size` — Minimum 16px body text on mobile (avoids iOS auto-zoom)
- `line-length-control` — Mobile 35–60 chars per line; desktop 60–75 chars
- `horizontal-scroll` — No horizontal scroll on mobile
- `spacing-scale` — Use 4pt/8dp incremental spacing system
- `container-width` — Consistent max-width on desktop (max-w-6xl / 7xl)
- `z-index-management` — Define layered z-index scale
- `fixed-element-offset` — Fixed navbar/bottom bar must reserve safe padding
- `viewport-units` — Prefer min-h-dvh over 100vh on mobile
- `visual-hierarchy` — Establish hierarchy via size, spacing, contrast — not color alone

### 6. Typography & Color (MEDIUM)

- `line-height` — Use 1.5-1.75 for body text
- `font-pairing` — Match heading/body font personalities
- `font-scale` — Consistent type scale (e.g. 12 14 16 18 24 32)
- `contrast-readability` — Darker text on light backgrounds
- `weight-hierarchy` — Bold headings (600–700), Regular body (400), Medium labels (500)
- `color-semantic` — Define semantic color tokens (primary, secondary, error, surface)
- `color-dark-mode` — Dark mode uses desaturated / lighter tonal variants, not inverted colors
- `color-accessible-pairs` — Foreground/background pairs must meet 4.5:1 (AA) or 7:1 (AAA)
- `truncation-strategy` — Prefer wrapping over truncation; when truncating use ellipsis
- `whitespace-balance` — Use whitespace intentionally to group related items

### 7. Animation (MEDIUM)

- `duration-timing` — Use 150–300ms for micro-interactions; complex transitions ≤400ms
- `transform-performance` — Use transform/opacity only; avoid animating width/height/top/left
- `loading-states` — Show skeleton or progress indicator when loading exceeds 300ms
- `excessive-motion` — Animate 1-2 key elements per view max
- `easing` — Use ease-out for entering, ease-in for exiting
- `motion-meaning` — Every animation must express a cause-effect relationship
- `state-transition` — State changes should animate smoothly, not snap
- `continuity` — Page/screen transitions should maintain spatial continuity
- `spring-physics` — Prefer spring/physics-based curves for natural feel
- `exit-faster-than-enter` — Exit animations shorter than enter (~60–70% of enter duration)
- `interruptible` — Animations must be interruptible by user tap/gesture
- `no-blocking-animation` — Never block user input during an animation
- `scale-feedback` — Subtle scale (0.95–1.05) on press for tappable cards/buttons

### 8. Forms & Feedback (MEDIUM)

- `input-labels` — Visible label per input (not placeholder-only)
- `error-placement` — Show error below the related field
- `submit-feedback` — Loading then success/error state on submit
- `required-indicators` — Mark required fields (e.g. asterisk)
- `empty-states` — Helpful message and action when no content
- `toast-dismiss` — Auto-dismiss toasts in 3-5s
- `confirmation-dialogs` — Confirm before destructive actions
- `input-helper-text` — Provide persistent helper text below complex inputs
- `disabled-states` — Disabled elements use reduced opacity (0.38–0.5) + cursor change
- `progressive-disclosure` — Reveal complex options progressively
- `inline-validation` — Validate on blur (not keystroke)
- `input-type-keyboard` — Use semantic input types (email, tel, number)
- `password-toggle` — Provide show/hide toggle for password fields
- `autofill-support` — Use autocomplete / textContentType attributes
- `undo-support` — Allow undo for destructive or bulk actions
- `error-recovery` — Error messages must include a clear recovery path
- `multi-step-progress` — Multi-step flows show step indicator or progress bar
- `error-clarity` — Error messages must state cause + how to fix

### 9. Navigation Patterns (HIGH)

- `bottom-nav-limit` — Bottom navigation max 5 items; use labels with icons
- `drawer-usage` — Use drawer/sidebar for secondary navigation, not primary actions
- `back-behavior` — Back navigation must be predictable and consistent
- `deep-linking` — All key screens must be reachable via deep link / URL
- `tab-bar-ios` — iOS: use bottom Tab Bar for top-level navigation
- `top-app-bar-android` — Android: use Top App Bar with navigation icon
- `nav-label-icon` — Navigation items must have both icon and text label
- `nav-state-active` — Current location must be visually highlighted
- `modal-escape` — Modals and sheets must offer a clear close/dismiss affordance
- `search-accessible` — Search must be easily reachable
- `state-preservation` — Navigating back must restore previous scroll position, filter state
- `gesture-nav-support` — Support system gesture navigation (iOS swipe-back, Android predictive back)
- `adaptive-navigation` — Large screens (≥1024px) prefer sidebar; small screens use bottom/top nav
- `avoid-mixed-patterns` — Don't mix Tab + Sidebar + Bottom Nav at the same hierarchy level
- `modal-vs-navigation` — Modals must not be used for primary navigation flows
- `focus-on-route-change` — After page transition, move focus to main content region

### 10. Charts & Data (LOW)

- `chart-type` — Match chart type to data type (trend → line, comparison → bar, proportion → pie/donut)
- `color-guidance` — Use accessible color palettes; avoid red/green only pairs for colorblind users
- `data-table` — Provide table alternative for accessibility
- `legend-visible` — Always show legend; position near the chart
- `tooltip-on-interact` — Provide tooltips/data labels on hover (Web) or tap (mobile)
- `axis-labels` — Label axes with units and readable scale
- `responsive-chart` — Charts must reflow or simplify on small screens
- `empty-data-state` — Show meaningful empty state when no data exists
- `loading-chart` — Use skeleton or shimmer placeholder while chart data loads
- `animation-optional` — Chart entrance animations must respect prefers-reduced-motion
- `large-dataset` — For 1000+ data points, aggregate or sample; provide drill-down
- `no-pie-overuse` — Avoid pie/donut for >5 categories; switch to bar chart
- `contrast-data` — Data lines/bars vs background ≥3:1; data text labels ≥4.5:1
- `sortable-table` — Data tables must support sorting with aria-sort
- `screen-reader-summary` — Provide a text summary describing the chart's key insight
