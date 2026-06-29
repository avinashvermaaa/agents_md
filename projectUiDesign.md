# Design System Inspired by FundedHive

## 1. Visual Theme & Atmosphere

FundedHive embodies a modern fintech aesthetic rooted in luxury, transparency, and digital innovation.
The design merges the sophistication of high-end trading platforms with the approachability of contemporary Web3 interfaces.
A deep charcoal-to-black foundation conveys stability and trust, while a striking gold accent creates visual hierarchy and signals opportunity.
Subtle hexagonal patterns in the background evoke blockchain networks and digital infrastructure.
The overall mood is premium yet accessible — conveying authority and speed without intimidating new traders.
Every element is designed to communicate reliability, instant gratification, and seamless execution.

**Key Characteristics**

- Premium dark theme with gold accents for maximum contrast and visual impact
- Clean, geometric typography hierarchy emphasizing speed and clarity
- Minimal visual noise with strategic use of negative space
- Gold highlights breaking dark backgrounds to draw attention to critical CTAs
- Responsive, mobile-first design that maintains luxury feel at all scales
- Blockchain-inspired visual elements (hexagons) reinforcing Web3 positioning

## 2. Color Palette & Roles

### Primary

- **Gold** (`#FECC58`): Primary brand accent, CTAs, highlights, and interactive elements. Most prominent color establishing brand identity.
- **Gold Alt** (`#FECC56`): Alternate primary gold for consistency across touch points.
- **Warning Gold** (`#F6C000`): Warning states and secondary accent emphasis.

### Accent Colors

- **Dark Slate** (`#26272F`): Deep accent for secondary buttons and UI components requiring visual distinction.
- **Card Dark** (`#363843`): Elevated dark surface for contained components.
- **Ultra Dark** (`#1B1C22`): Darkest accent layer for highest contrast scenarios.

### Interactive

- **Gold Border** (`#FECC58`): Interactive element borders and outlines on dark backgrounds.
- **Gray Interactive** (`#808290`): Secondary interactive state indicators.
- **Gray Tertiary** (`#636674`): Tertiary interaction feedback and disabled states.

### Neutral Scale

- **Light Off-White** (`#F5F5F5`): Primary text on dark backgrounds, body copy, and high-contrast content.
- **Pure White** (`#FFFFFF`): Maximum contrast backgrounds, cards, and premium surfaces.
- **Off-White Secondary** (`#F9F9F9`): Subtle differentiation for grouped content.
- **Dark Gray** (`#4A4A4A`): Secondary body text and supporting information.
- **Medium Gray** (`#9A9A9A`): Disabled text and tertiary labels.
- **Light Gray** (`#BABBBC`): Borders and subtle dividers.
- **Mid Gray** (`#666666`): Alternative secondary text weight.

### Surface & Borders

- **Jet Black** (`#000000`): Primary background and button fill.
- **Gray Border** (`#9A9CAE`): Subtle borders and dividers on dark surfaces.

## 3. Typography Rules

### Font Family

**Primary:** Space Grotesk (`font-family: 'Space Grotesk', 'Courier New', monospace`) — Used for all headings and display text. Modern geometric sans-serif evoking digital precision.

**Secondary:** Onest (`font-family: 'Onest', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif`) — Used for body text, buttons, and UI labels. Clean, accessible humanist sans-serif.

### Hierarchy

| Role | Font | Size | Weight | Line Height | Letter Spacing | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| Display / H1 | Space Grotesk | 60px | 600 | 72px | 0px | Hero headline, maximum impact |
| Display Alt / H2 | Space Grotesk | 64px | 600 | 76.8px | 0px | Alternative display, key messaging |
| Heading / H3 | Space Grotesk | 30px | 600 | 36px | 0px | Section headings, subsections |
| Body | Onest | 30px | 400 | 39px | 0px | Large body paragraphs, descriptions |
| Button / Label | Onest | 13px | 400 | 19.5px | 0px | Button text, interactive labels |
| Badge / Code | Onest | 14px | 700 | 14px | 0px | Badges, promo codes, emphasis |
| Link / Caption | Onest | 12px | 700 | 12px | 0px | Navigation links, captions, small CTA |

### Principles

- **Contrast-First:** Dark backgrounds paired with light text (`#F5F5F5` or `#FFFFFF`) ensures 7:1+ WCAG AAA compliance.
- **Semantic Weight:** Font weight progresses from 400 (body) through 600 (headings) for clear hierarchy without size alone.
- **Rhythm & Scale:** Line heights set to 1.2x–1.3x font size creating breathing room and readability at high contrast.
- **Digital Precision:** Space Grotesk's geometric nature reinforces tech/fintech positioning; Onest's friendliness balances authority.
- **Speed Communication:** Size jumps (60px → 30px → 13px) allow rapid visual scanning of page priority.

## 4. Component Stylings

### Buttons

#### Primary CTA Button

- **Background:** `#000000`
- **Text Color:** `#FECC58`
- **Border:** `1px solid #FECC58`
- **Padding:** `12px 20px`
- **Border Radius:** `50px`
- **Font:** Onest, 13px, weight 700
- **Line Height:** `19.5px`
- **Height:** `40px` (minimum)
- **Hover State:** Background `#1B1C22`, border `#F6C000`, text `#F6C000`
- **Active State:** Background `#363843`, text `#FECC58`
- **Disabled State:** Background `#4A4A4A`, border `#9A9A9A`, text `#9A9A9A`

#### Secondary Button (Outline)

- **Background:** `transparent`
- **Text Color:** `#FECC58`
- **Border:** `1px solid #FECC58`
- **Padding:** `12px 20px`
- **Border Radius:** `50px`
- **Font:** Onest, 13px, weight 700
- **Line Height:** `19.5px`
- **Height:** `40px` (minimum)
- **Hover State:** Background `rgba(254, 204, 88, 0.1)`, border `#F6C000`, text `#F6C000`
- **Active State:** Background `rgba(254, 204, 88, 0.2)`, text `#FECC58`

#### Small Badge Button

- **Background:** `#000000`
- **Text Color:** `#FECC58`
- **Border:** `1px solid #FECC58`
- **Padding:** `4px 12px`
- **Border Radius:** `4px`
- **Font:** Onest, 12px, weight 700
- **Line Height:** `12px`
- **Height:** `22px`
- **Hover State:** Background `#1B1C22`, text `#F6C000`

#### Ghost Button (Text Only)

- **Background:** `transparent`
- **Text Color:** `#F5F5F5`
- **Border:** `none`
- **Padding:** `0px`
- **Font:** Onest, 12px, weight 700
- **Hover State:** Text color `#FECC58`
- **Underline:** Optional on hover for clarity

### Cards & Containers

#### Standard Card (Dark)

- **Background:** `rgba(27, 28, 34, 0.5)`
- **Border:** `1px solid #9A9CAE`
- **Border Radius:** `3px`
- **Padding:** `24px`
- **Text Color:** `#F5F5F5`
- **Box Shadow:** `rgba(255, 255, 255, 0.1) -1px -2px 2px 0px inset, rgba(255, 255, 255, 0.3) 1px 1px 2px 0px inset`
- **Font:** Onest, 13px, weight 400
- **Line Height:** `19.5px`

#### Elevated Card (Premium)

- **Background:** `rgba(27, 28, 34, 0.8)`
- **Border:** `1px solid #363843`
- **Border Radius:** `3px`
- **Padding:** `32px`
- **Text Color:** `#F5F5F5`
- **Box Shadow:** `rgba(0, 0, 0, 0.35) 0px 8px 32px 0px, rgba(255, 255, 255, 0.08) 0px 1px 0px 0px inset, rgba(0, 0, 0, 0.25) 0px -1px 0px 0px inset`
- **Hover State:** Border `#FECC58`, shadow brightens slightly

#### Light Surface Card

- **Background:** `#FFFFFF`
- **Border:** `1px solid #BABBBC`
- **Border Radius:** `3px`
- **Padding:** `24px`
- **Text Color:** `#000000`
- **Box Shadow:** `rgba(0, 0, 0, 0.1) 0px 6.5px 13px 0px`

### Inputs & Forms

#### Text Input

- **Background:** `#000000`
- **Border:** `1px solid #9A9CAE`
- **Border Radius:** `4px`
- **Padding:** `12px 16px`
- **Text Color:** `#F5F5F5`
- **Font:** Onest, 13px, weight 400
- **Line Height:** `19.5px`
- **Placeholder Color:** `#636674`
- **Focus State:** Border `#FECC58`, box-shadow `0 0 0 3px rgba(254, 204, 88, 0.1)`
- **Error State:** Border `#F6C000`, text-decoration underline red

#### Select Dropdown

- **Background:** `#000000`
- **Border:** `1px solid #9A9CAE`
- **Border Radius:** `4px`
- **Padding:** `12px 16px`
- **Text Color:** `#F5F5F5`
- **Font:** Onest, 13px, weight 400
- **Hover State:** Border `#FECC58`
- **Open State:** Box-shadow `rgba(0, 0, 0, 0.1) 4px 4px 20px 0px`

#### Checkbox / Toggle

- **Unchecked Background:** `#1B1C22`
- **Checked Background:** `#FECC58`
- **Border:** `1px solid #9A9CAE` (unchecked), `1px solid #FECC58` (checked)
- **Border Radius:** `4px`
- **Size:** `20px x 20px`
- **Checkmark Color:** `#000000`

### Navigation

#### Top Navigation Bar

- **Background:** `#000000`
- **Border Bottom:** `1px solid #363843`
- **Padding:** `20px 40px`
- **Height:** `80px` (with logo and menu items)

#### Navigation Link

- **Text Color:** `#F5F5F5`
- **Font:** Onest, 12px, weight 700
- **Hover State:** Color `#FECC58`
- **Active State:** Color `#FECC58`, border-bottom `2px solid #FECC58`
- **Padding:** `12px 16px`

#### Dropdown Menu

- **Background:** `#1B1C22`
- **Border:** `1px solid #363843`
- **Border Radius:** `4px`
- **Box Shadow:** `rgba(0, 0, 0, 0.1) 4px 4px 20px 0px`
- **Item Padding:** `12px 16px`
- **Item Hover:** Background `#363843`, text `#FECC58`
- **Text Color:** `#F5F5F5`
- **Font:** Onest, 12px, weight 400

#### Mobile Hamburger Menu

- **Icon Color:** `#FECC58`
- **Size:** `24px x 24px`
- **Active State:** Color `#F6C000`

## 5. Layout Principles

### Spacing System

**Base Unit:** `4px`

**Scale:**

- `4px` — Micro spacing (inline icon gaps, tight component padding)
- `8px` — Extra small (compact padding, minimal margins)
- `12px` — Small (form control padding, button padding)
- `16px` — Medium (gap between components, standard margin)
- `20px` — Large (card padding, section spacing)
- `24px` — Extra large (major section gaps, container padding)
- `28px` — Extra extra large (heading spacing)
- `32px` — Premium spacing (major block spacing, elevated containers)
- `36px` — Spacious (vertical rhythm between sections)
- `40px` — Large section spacing (major layout divisions)
- `44px` — Extra spacious (hero section margins)
- `52px` — Maximum (top-level section spacing, full-width padding)

**Usage Context:**

- Component internal padding: `12px–20px`
- Gap between inline elements: `16px`
- Card margins: `20px–24px`
- Section breaks: `32px–52px`
- Top/bottom padding on full-width blocks: `40px–52px`

### Grid & Container

**Max Container Width:** `1400px`

**Column Strategy:**

- Desktop: 12-column grid with `16px` gutters
- Tablet: 8-column grid with `12px` gutters
- Mobile: 4-column grid with `8px` gutters

**Section Patterns:**

- Full-width hero sections with centered content (max 1000px inner width)
- Two-column layouts for comparison content (50% | 50% on desktop, stacked on tablet)
- Three-column card grids (33.33% each on desktop, 50% on tablet, 100% on mobile)
- Asymmetric layouts (60% | 40% or 70% | 30%) for feature + image combinations

### Whitespace Philosophy

FundedHive employs generous whitespace to convey premium positioning and reduce cognitive load.
Sections are separated by substantial gaps (40px minimum) allowing the eye to rest.
Card-based layouts maintain breathing room around content rather than edge-to-edge fills.
Negative space is intentional — absence of visual clutter reinforces trust and speed.
Dark backgrounds amplify the effect of whitespace, making white and light gray text pop with exceptional clarity.

### Border Radius Scale

- `2px` — Minimal buttons, micro-interactions, technical precision
- `3px` — Cards, containers, general UI surfaces
- `4px` — Form inputs, badges, small buttons
- `6.175px` — Medium buttons, slightly rounded edges
- `20px` — Large buttons, rounded badges, pill-shaped components
- `50px` — Fully rounded buttons (primary CTAs), pill-style containers

## 6. Depth & Elevation

| Level | Treatment | Use |
| --- | --- | --- |
| Flat (None) | No shadow, border only | Text-heavy cards, ghost buttons, minimal UI |
| Raised (Inset) | `rgba(255, 255, 255, 0.1) -1px -2px 2px 0px inset, rgba(255, 255, 255, 0.3) 1px 1px 2px 0px inset` | Standard dark cards, containers, pressed states |
| Elevated (Soft) | `rgba(0, 0, 0, 0.1) 0px 6.5px 13px 0px` | Light cards, modals on bright backgrounds |
| High (Medium) | `rgba(0, 0, 0, 0.35) 0px 8px 32px 0px, rgba(255, 255, 255, 0.08) 0px 1px 0px 0px inset, rgba(0, 0, 0, 0.25) 0px -1px 0px 0px inset` | Premium dark cards, interactive elements, hover states |
| Maximum (Strong) | `rgba(0, 0, 0, 0.1) 4px 4px 20px 0px` | Dropdown menus, overlays, highest-z components |

**Shadow Philosophy:**

FundedHive's shadow system reinforces depth through dual-layer inset and outset shadows on dark backgrounds, creating a subtle 3D embossment effect.
This communicates clickability and interactive surfaces without introducing harsh drop shadows that would conflict with the premium aesthetic.
Light backgrounds use softer outer shadows with minimal inset treatment.
The stratified approach (inset light edge + inset dark bottom + outset dark shadow) mimics physical depth, making buttons and cards feel slightly raised or recessed depending on context.

## 7. Do's and Don'ts

### Do

- **Use gold** (`#FECC58`) for all primary calls-to-action and interactive highlights to maintain brand consistency.
- **Maintain dark backgrounds** as the default for all major surfaces to preserve the premium, night-trading aesthetic.
- **Pair light text** (`#F5F5F5` or `#FFFFFF`) with dark backgrounds consistently — never reverse for legibility.
- **Apply 50px border-radius** to large primary buttons and prominent CTAs for modern, premium feel.
- **Use generous spacing** (40px+ between sections) to emphasize content importance and reduce visual fatigue.
- **Implement full-width hero sections** with centered content zones (max 1000px) for dramatic impact.
- **Leverage the gold-on-black contrast** for visual hierarchy — gold draws the eye to critical actions.
- **Reserve `#FFFFFF` backgrounds** for premium feature cards or high-contrast content zones requiring maximum visibility.
- **Use Space Grotesk** for all headings to reinforce tech/fintech positioning and geometric brand language.
- **Stack buttons vertically** on mobile (<768px) to ensure safe touch targets (minimum 44px height).

### Don't

- **Never use the accent colors** (`#9A9CAE`, `#636674`) as primary CTAs — these are reserved for secondary interactions and borders.
- **Avoid placing gold text directly on white backgrounds** — the contrast degrades and feels jarring (use dark text on white instead).
- **Don't mix fonts excessively** — limit to Space Grotesk (headings) and Onest (body/UI) only.
- **Don't apply multiple shadow layers** to every element — reserve elevated shadows for highest-priority interactive surfaces.
- **Avoid thin font weights** (<400) in body copy — the 30px body size already provides emphasis; lighter weights reduce readability.
- **Don't shrink primary buttons below 40px height or 12px font** — mobile users require safe, accessible touch targets.
- **Never disable the hover state** on interactive elements — users expect visual feedback on desktop.
- **Avoid low-contrast gray-on-gray text** combinations — always test for minimum 4.5:1 WCAG AA compliance.
- **Don't justify text alignment** in paragraph content — prefer left-align for better readability on dark backgrounds.
- **Avoid animated backgrounds or busy patterns** that compete with content — hexagons should remain subtle and faded.

## 8. Responsive Behavior

### Breakpoints

| Breakpoint Name | Width | Key Changes |
| --- | --- | --- |
| Mobile | 320px–767px | Single column layout, 4-column grid, stacked navigation, 8px–12px spacing, 100% card width |
| Tablet | 768px–1023px | Two-column primary, 8-column grid, slide-out menu, 12px–16px spacing, 50% card width |
| Desktop | 1024px–1399px | Full three-column, 12-column grid, horizontal nav, 16px–20px spacing, 33.33% card width |
| Large Desktop | 1400px+ | Max container 1400px, centered layout, generous side margins, 20px–52px spacing |

### Touch Targets

- **Minimum Tap Area:** `44px x 44px` for all interactive elements (buttons, links, form inputs)
- **Spacing Between Targets:** `12px` minimum vertical/horizontal gap to prevent accidental activation
- **Button Sizing:** Primary buttons `40px–48px` height, secondary buttons `40px` height, icon buttons `44px x 44px`
- **Form Input Height:** `40px–44px` for text inputs and selects (includes padding)
- **Link Padding:** `12px` internal padding on navigation links to expand touch area

### Collapsing Strategy

**Mobile (320px–767px):**

- Navigation collapses to hamburger menu icon (top-right corner)
- Hero headline reduces to H2 size (48px vs. 60px) for screen fit
- Two-column layouts stack to single column
- Card grids reduce to 1 column (100% width with 12px margin)
- Form labels stack above inputs instead of side-by-side
- Padding on containers reduces from 40px to 20px
- Modal/dropdown max-width set to 90vw
- Images scale to 100% of container

**Tablet (768px–1023px):**

- Navigation remains visible (may condense spacing to 12px)
- Hero headline stays H2 size (60px)
- Two-column layouts remain 50% | 50%
- Card grids display 2 columns (50% each)
- Modal/dropdown max-width set to 85vw
- Padding on containers standardizes to 24px
- Large hero images reduce to 80% of desktop size

**Desktop (1024px+):**

- Full navigation bar with all items visible
- Hero headline full H1 size (60px) with extended line height
- Three-column card grids display at 33.33% each
- Asymmetric layouts display at designed ratios (60% | 40%)
- Full padding and spacing applied (40px–52px)
- Images and content display at 100%

## 9. Agent Prompt Guide

### Quick Color Reference

- **Primary CTA:** Gold (`#FECC58`) — Used for all main call-to-action buttons, highlights, and interactive focus states
- **Button Background:** Jet Black (`#000000`) — Primary button fill, form input backgrounds, navigation
- **Text on Dark:** Light Off-White (`#F5F5F5`) — Default body text, labels, and high-contrast content on dark backgrounds
- **Secondary Text:** Dark Gray (`#4A4A4A`) — Supporting copy, secondary labels, disabled states
- **Card Background Dark:** Dark Slate (`#26272F`) or `rgba(27, 28, 34, 0.5)` — Premium cards and containers
- **Card Border:** Gray Interactive (`#9A9CAE`) — Subtle borders separating card sections
- **Disabled/Inactive:** Medium Gray (`#9A9A9A`) — Grayed-out buttons, disabled form states
- **Accent Highlight:** Warning Gold (`#F6C000`) — Hover states, emphasis, secondary accent
- **Maximum Contrast Backgrounds:** Pure White (`#FFFFFF`) — Light backgrounds for feature sections, premium cards
- **Secondary Button Outline:** Gold Border (`#FECC58`) — Secondary outline buttons, icon borders

### Iteration Guide

1. **All buttons default to black background with gold text and gold border** (`#000000` bg, `#FECC58` text/border). Hover states shift to lighter gold (`#F6C000`). Primary buttons use 50px border-radius; smaller buttons use 4px.

2. **Dark backgrounds are law** — Use `#000000` for main surfaces, `#1B1C22` for elevated dark surfaces, `#363843` for secondary accents. Never reverse to light backgrounds unless explicitly requiring maximum contrast feature highlight.

3. **Typography is a two-font system:** Space Grotesk (headings: 60px/64px H1/H2, 30px H3) and Onest (body 30px, buttons 13px, captions 12px). All headings bold 600, body regular 400, UI labels bold 700.

4. **Spacing cascades in 4px increments:** Base padding 12px–20px (components), gaps 16px (inline), section breaks 32px–52px. Never use arbitrary spacing; consult the scale.

5. **Light text on dark backgrounds is the default:** `#F5F5F5` for body, `#FFFFFF` for maximum contrast, `#4A4A4A` for secondary. All must maintain 4.5:1 WCAG AA minimum contrast.

6. **Shadow system uses inset + outset dual layers** for dark cards (`rgba(255, 255, 255, 0.1) -1px -2px 2px inset, rgba(255, 255, 255, 0.3) 1px 1px 2px inset`). Apply only to interactive or premium surfaces; most elements use borders instead.

7. **Mobile-first responsive rules:** Breakpoints at 768px (tablet) and 1024px (desktop). Touch targets never below 44px height. Collapse to single column below 768px. Buttons stack vertically on mobile.

8. **Borders are minimal and gray** (`#9A9CAE` or `#BABBBC`). Use sparingly. Cards primarily differentiated by background opacity and shadow, not thick borders.

9. **Gold accent draws attention** — use `#FECC58` exclusively for CTAs, hover states, and visual hierarchy. Never overuse; it's the brand signal. Warning gold (`#F6C000`) is a slight shift for secondary emphasis.

10. **Interactive feedback is mandatory:** Every button/link has a hover state (color/border shift), focus state (border highlight), and active state (darker background). Disabled state uses `#9A9A9A` gray across text, border, and background.
