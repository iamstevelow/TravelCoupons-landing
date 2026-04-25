# TravelCoupons - Landing Page Spec

## Concept & Vision
A premium, editorial-style landing page for **TravelCoupons** — an e-commerce platform selling exclusive coupons for travelers. The experience feels like a high-end travel magazine: warm, aspirational, and trustworthy. Every interaction should feel tactile and considered, like flipping through a beautifully designed catalog.

## Design Language

### Aesthetic Direction
**Editorial Luxury** — Warm cream backgrounds (#FDFBF7), muted sage accents, deep espresso text tones. Feels like premium travel collateral, not a generic SaaS product.

### Color Palette
- **Background:** `#FDFBF7` (warm cream)
- **Primary Text:** `#1A1A1A` (near black)
- **Secondary Text:** `#6B6B6B` (warm gray)
- **Accent:** `#2D5A4A` (deep sage/forest)
- **Accent Light:** `#E8F0ED` (sage tint)
- **Highlight:** `#D4A853` (warm gold)
- **Card Background:** `#FFFFFF`

### Typography
- **Headings:** DM Serif Display (elegant serif with personality)
- **Body:** DM Sans (clean, readable companion)
- **Accent/Labels:** DM Sans Medium, uppercase tracking

### Spatial System
- Section padding: `py-24` to `py-40`
- Card radius: `rounded-3xl` (24px+)
- Component gaps: `gap-8` to `gap-12`
- Max content width: `max-w-7xl`

### Motion Philosophy
- Spring-based hover physics on buttons (slight scale press)
- Staggered fade-up reveals on scroll (IntersectionObserver)
- Smooth cubic-bezier transitions: `cubic-bezier(0.32, 0.72, 0, 1)`
- No linear or generic ease-in-out

### Visual Assets
- Icons: Phosphor Icons (thin line style)
- Images: High-quality travel photography (via Unsplash)
- Texture: Subtle CSS noise overlay for editorial feel

## Layout & Structure

### Hero Section
- Large headline with serif typography
- Subheadline with value proposition
- Two CTAs: primary (Get Coupons) and secondary (How It Works)
- Featured travel destination image as visual anchor

### Features Section (Bento Grid)
- Asymmetric card layout: large feature card + stacked smaller cards
- Icons with warm accent colors
- Clear benefit statements

### How It Works
- 3-step process with numbered badges
- Connected by subtle visual line
- Clean, scannable layout

### Popular Coupons Section
- Card grid showing example coupons
- Destination imagery, discount badge, terms preview

### Testimonials
- Large quote typography
- User avatar and travel history
- Warm, personal feel

### CTA Section
- Strong conversion focus
- Email capture or browse button
- Atmospheric travel imagery

### Footer
- Minimal, clean
- Essential links only
- Social icons

## Features & Interactions

### Navigation
- Floating glass pill navbar (not sticky to top)
- Smooth hamburger morph to X on mobile
- Staggered menu item reveal

### Buttons
- Pill-shaped with generous padding
- Button-in-button trailing icon pattern
- Magnetic hover with scale physics

### Cards
- Double-bezel architecture (nested containers)
- Soft ambient shadows (no harsh drops)
- Image + content + CTA structure

### Scroll Animations
- Elements fade up and blur on viewport entry
- 800ms+ duration with staggered delays
- GPU-safe (transform + opacity only)

## Component Inventory

### NavBar
- Floating pill container
- Logo left, nav links center, CTA right
- Mobile: hamburger → full overlay menu

### HeroSection
- Full viewport height (100dvh)
- Split layout: text left, image right
- Eyebrow tag above headline

### FeatureCard
- Icon + title + description
- Rounded container with shadow
- Hover lift effect

### CouponCard
- Destination image header
- Discount badge overlay
- Title, description, terms
- "Get Deal" CTA

### TestimonialCard
- Large quote marks
- Quote text in serif
- Avatar + name + location

### CTASection
- Background image with overlay
- Centered headline + button
- Subtle parallax on scroll

### Footer
- Dark background option or matching cream
- 3-column layout on desktop
- Minimal links

## Technical Approach
- Single HTML file with embedded CSS and JavaScript
- Tailwind CSS via CDN for utility classes
- Vanilla JavaScript for interactions
- No build step required
- IntersectionObserver for scroll animations
- CSS custom properties for theming