# Design Guidelines: Professional Biolink Platform

## Design Approach

**Reference-Based Strategy**: Draw inspiration from guns.lol's customization depth and solo.to's sleek minimalism. Create a platform that balances creative expression with ease of use.

**Key References**:
- guns.lol: Custom effects, gradient backgrounds, profile customization depth
- solo.to: Clean typography, professional layouts, embedded content support
- Linktree: Simple link card patterns

**Design Principles**:
1. Customization-first: Every visual element should be user-controllable
2. Mobile-native: Design for vertical mobile screens primarily
3. Performance: Smooth, fast-loading profiles regardless of effects
4. Creator-friendly: Empower self-expression without overwhelming options

---

## Typography

**Font Strategy**: Use Google Fonts with 2 font pairings

**Primary Pairing** (Default):
- Headers: Inter (700, 600) - modern, clean, highly legible
- Body: Inter (400, 500) - consistent with headers
- Links: Inter (500) - medium weight for emphasis

**Alternative Pairing** (User selectable):
- Headers: Playfair Display (700) - elegant serif for creators
- Body: Inter (400) - readable sans for links

**Scale**:
- Profile Name: text-3xl md:text-4xl font-bold
- Bio Text: text-base md:text-lg
- Link Titles: text-base font-medium
- Section Headers: text-xl md:text-2xl font-semibold
- Dashboard UI: text-sm to text-base

---

## Layout System

**Spacing Primitives**: Use Tailwind units of 2, 4, 6, 8, 12, 16, 20

**Profile Page Structure**:
- Container: max-w-md mx-auto (centered, mobile-optimized)
- Vertical spacing: space-y-6 between major sections
- Card padding: p-4 md:p-6
- Link spacing: gap-3 between individual links

**Landing Page Structure**:
- Hero: Full viewport height (min-h-screen) with centered content
- Content sections: py-20 md:py-32 for breathing room
- Container: max-w-7xl mx-auto px-4
- Grid layouts: grid-cols-1 md:grid-cols-2 lg:grid-cols-3

**Dashboard Layout**:
- Sidebar: w-64 fixed on desktop, collapsible on mobile
- Main content: max-w-4xl mx-auto
- Settings panels: max-w-2xl

---

## Component Library

### Navigation (Landing Page)
- Sticky header with backdrop blur (backdrop-blur-md bg-white/80)
- Logo left, navigation center, CTA buttons right
- Mobile: Hamburger menu with slide-out drawer
- Height: h-16 md:h-20

### Profile Card (User Biolink Page)
**Profile Header**:
- Avatar: Circular or square (user choice), w-24 h-24 md:w-32 md:h-32
- Name + verification badge if applicable
- Bio text: max 150 characters, text-center
- Optional background image with gradient overlay

**Link Buttons**:
- Full-width rounded cards: rounded-xl md:rounded-2xl
- Height: min-h-14 md:min-h-16
- Icon left (w-5 h-5), text centered or left-aligned
- Hover: subtle scale transform (scale-105) and shadow increase
- Support for custom thumbnails (square, 48x48px)

**Social Icons Row**:
- Horizontal scroll on mobile
- Icon size: w-10 h-10
- Circular backgrounds with platform brand colors
- Fixed gap: gap-3

### Form Elements (Dashboard)
- Input fields: h-12 rounded-lg border-2
- Focus states: ring-4 ring-opacity-20
- Toggle switches: Modern iOS-style toggles
- Color pickers: Native input with preview swatch
- Upload zones: Dashed border with drag-drop indication

### Cards & Sections
- Dashboard cards: rounded-xl border shadow-sm p-6
- Landing page feature cards: p-8 with icon (w-12 h-12) at top
- Stats cards: Centered numbers (text-4xl font-bold) with labels below

### Buttons
**Primary CTA**:
- Solid fill with brand gradient
- Height: h-12 md:h-14
- Padding: px-8 md:px-12
- Rounded: rounded-full
- Shadow on hover: shadow-lg

**Secondary**:
- Border style with transparent background
- Same dimensions as primary
- Border width: border-2

**Link Buttons (Profile)**:
- Glass morphism option: backdrop-blur-md bg-white/10
- Solid option: Solid background with user-selected accent
- Border option: border-2 with transparent fill

### Modals & Overlays
- Backdrop: bg-black/50 backdrop-blur-sm
- Modal: max-w-lg rounded-2xl p-8
- Exit: Top-right X button (w-8 h-8 rounded-full)

---

## Images

### Landing Page Hero
**Large Hero Image**: Yes - Full-width background image with gradient overlay
- Placement: Hero section background
- Style: Abstract gradient mesh or creator workspace scene
- Overlay: Linear gradient (black/50 to transparent) for text readability
- Buttons over image: Blurred background (backdrop-blur-md bg-white/10)

### Profile Showcase Grid
- 3x3 or 4x4 grid of example profile screenshots
- Each: aspect-square with rounded corners
- Images show diverse profile styles (minimal, maximal, creative)

### Feature Section Icons
- Custom illustrated icons (64x64px) for each feature
- Style: Line art or duotone
- Placement: Top of feature cards

### Dashboard UI
- Upload placeholder images for profile picture, background, banner
- Preview panels showing live customization changes

### Example Profiles (Marketing)
- Real user profile screenshots in iPhone mockups
- Showcase variety: musician, artist, business, creator
- Grid display: 2 columns mobile, 4 columns desktop

---

## Visual Effects

**Gradients** (User-customizable):
- Linear gradients for backgrounds
- Radial gradients for glow effects
- Support for 2-4 color stops

**Blur Effects**:
- Backdrop blur for glass morphism cards
- Profile background blur intensity slider (0-100%)

**Animations** (Minimal):
- Page transitions: Fade in on load (duration-300)
- Link hover: Scale and shadow (duration-200)
- No parallax, no continuous animations, no scroll-triggered effects

**Shadows**:
- Soft shadows for cards: shadow-md
- Strong shadows for hover states: shadow-xl
- Glow effects: Colored box-shadow with blur radius

---

## Accessibility

- Minimum contrast ratio: 4.5:1 for all text
- Focus indicators: ring-4 ring-offset-2 on all interactive elements
- Keyboard navigation: Full support for tab navigation
- Screen reader labels: aria-label on icon-only buttons
- Color customization warnings: Alert users if contrast is too low