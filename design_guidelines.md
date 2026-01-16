# SMSala CPaaS Platform - Design Guidelines

## Design Approach

**System**: Modern telecom SaaS design inspired by **Sinch, Plivo, and Twilio** - emphasizing clarity, trust, and enterprise credibility. This approach prioritizes clean layouts, generous spacing, soft gradients, and card-based sections for a premium professional look.

**Core Principles**:
- Clean, modern SaaS aesthetics with large spacing
- Card-based sections with soft shadows
- Soft gradient backgrounds for hero sections
- Trust through professionalism and visual consistency
- Conversion-focused with clear CTAs
- Mobile-first responsive design

---

## Typography System

**Font Family**: Inter (Google Fonts) for all UI text
- **Hero Headlines**: text-4xl md:text-5xl lg:text-6xl (font-bold)
- **Section Headers**: text-3xl md:text-4xl (font-semibold)
- **Service Titles**: text-xl md:text-2xl (font-semibold)
- **Body Text**: text-base md:text-lg (font-normal) with generous line-height
- **Captions/Meta**: text-sm (font-medium or font-normal)

**Line Heights**:
- Headlines: leading-tight
- Body text: leading-relaxed for optimal readability
- Paragraphs in content sections: leading-7 or leading-8

---

## Color System

**Primary Colors**:
- Primary: Deep blue (hsl 217 91% 35%) - used for CTAs, links, accents
- Primary variants for hover/active states

**Neutral Palette**:
- Background: Clean white (#ffffff) with subtle gray variants
- Card backgrounds: Very light gray for subtle elevation
- Text: Near-black for headlines, gray variants for body and muted text

**Gradient Usage**:
- Hero sections: Subtle gradient from white to light primary tint
- Cards on hover: Subtle elevation effect
- Avoid harsh gradients - use opacity-based transitions

---

## Layout & Spacing System

**Container Strategy**:
- Full-width sections with centered content containers
- Max-width: `max-w-7xl` for main content
- Reading content: `max-w-4xl` for optimal line length
- Extra-wide heroes: Full bleed with contained content

**Section Spacing**:
- Hero sections: py-20 md:py-28 lg:py-32
- Content sections: py-16 md:py-24
- Between section elements: gap-12 md:gap-16

**Component Spacing**:
- Card padding: p-6 md:p-8 lg:p-10
- Grid gaps: gap-6 md:gap-8
- Text spacing: mb-4 for headings, mb-6 for paragraphs

**Grid System**:
- Service cards: grid-cols-1 md:grid-cols-2 lg:grid-cols-3
- Features: grid-cols-1 lg:grid-cols-2
- Stats: grid-cols-2 md:grid-cols-4
- Country listings: grid-cols-2 md:grid-cols-3 lg:grid-cols-4

---

## Component Library

### Hero Sections

**Homepage Hero**:
- Large headline with gradient text accent option
- Supportive subheadline (max 2 lines)
- Dual CTA buttons (primary + secondary)
- Trust indicators (stats, logos, badges)
- Optional: Abstract illustration or dashboard preview
- Background: Subtle gradient mesh or soft color wash

**Service Page Heroes**:
- Icon + headline combination
- Clear value proposition
- Single primary CTA
- Breadcrumb navigation above
- Height: Generous but content-driven

**Country Page Heroes**:
- Country flag integration
- Localized messaging
- Service availability indicators

### Cards & Containers

**Feature Cards**:
- Rounded corners: rounded-xl or rounded-2xl
- Padding: p-6 md:p-8
- Border: Subtle border (border-border)
- Background: bg-card
- Hover: Subtle lift with shadow increase

**Service Cards**:
- Icon in colored container
- Title and description
- "Learn more" link
- Hover: Border color change and slight elevation

**Stats Cards**:
- Large number display
- Supporting label
- Optional trend indicator

**Testimonial Cards**:
- Quote icon or styling
- Review text
- Reviewer name, role, company
- Rating stars (optional)
- No photos (B2B focus)

### Buttons & CTAs

**Primary Button**:
- Background: bg-primary
- Size: Default or large
- Rounded: rounded-lg
- Font: font-medium

**Secondary Button**:
- Variant: outline or ghost
- Border: border-border
- Hover: bg-muted

**CTA Placement**:
- Dual CTAs in heroes (primary + outline)
- Single CTA at section ends
- Sticky CTA on mobile (optional)

### Navigation

**Header**:
- Sticky with backdrop blur
- Height: Comfortable (h-18 or similar)
- Logo left, nav center, CTAs right
- Mega-menus for Products, Solutions, Countries

**Footer**:
- Multi-column layout (6 columns max)
- Products, Use Cases, Countries, Company, Legal, Resources
- Social links
- Trust badges at bottom

### Content Sections

**How It Works**:
- Numbered steps with icons
- Left content, right visual (or alternating)
- Connection lines between steps

**Feature Grids**:
- Icon + heading + description
- 2-3 columns on desktop
- Consistent spacing

**FAQ Accordions**:
- Clean expand/collapse
- Question in semi-bold
- Answer with adequate padding
- Schema markup ready

**Testimonials Grid**:
- 2-3 testimonials per row
- Quote styling
- Company type mentions for B2B credibility

### Reviews Display

**Global Reviews**:
- Used on general pages (home, pricing, about)
- Professional, industry-diverse testimonials
- 3 per section typically

**Country-Specific Reviews**:
- Used on country pages
- Mention country name naturally
- Local business types and use cases
- 2 per country page

---

## Page Structure Standards

### Minimum Content Requirements

**Service Pages** (1200-1800 words):
1. Hero section with value proposition
2. What this service is (explanation)
3. How it works (step-by-step)
4. Key features (6-8 features)
5. Business use cases (4-6)
6. Industry examples (3-4)
7. Benefits section
8. Why choose SMSala
9. FAQs (5-8 questions)
10. CTA section
11. Testimonials

**Country Pages** (1200+ words):
1. Localized hero
2. Services available
3. Compliance/regulations
4. Local use cases
5. Major cities coverage
6. Country-specific testimonials
7. Local industry examples
8. FAQ with local context
9. CTA section

---

## SEO Requirements

### On-Page SEO
- Proper H1-H6 hierarchy (single H1 per page)
- Semantic HTML (header, nav, main, article, section, footer)
- Internal linking between related pages

### Meta Tags (per page)
- Unique title tag (50-60 characters)
- Unique meta description (150-160 characters)
- Canonical tag (self-referencing)
- Open Graph tags
- Twitter Card tags

### Schema Markup
- Organization (on all pages)
- Service (on service pages)
- FAQ (on pages with FAQs)
- Review/Rating (on pages with testimonials)
- Breadcrumb (on all internal pages)
- LocalBusiness variant (on country pages)

### International SEO
- hreflang tags for country pages
- Country-specific content
- Local keyword integration

---

## Accessibility & Performance

**Accessibility**:
- WCAG 2.1 AA contrast ratios
- Focus states on all interactive elements
- Proper heading hierarchy
- Alt text for images
- Keyboard navigation support
- Touch targets: minimum 44x44px

**Performance**:
- Minimal animations (functional only)
- Optimized images
- Lazy loading for below-fold content
- No layout shifts

---

## Animation Guidelines

**Minimal Motion Strategy**:
- Subtle fade-in on scroll (opacity + slight translateY)
- Hover states: opacity changes, subtle scale (1.02 max)
- Smooth accordion transitions
- No page transitions (instant navigation)

**Interactive States**:
- hover-elevate utility for cards
- active-elevate-2 for pressed states
- Focus rings for accessibility

---

This design system creates a premium, trustworthy CPaaS platform optimized for global enterprise customers, with comprehensive SEO support and modern SaaS aesthetics.
