# Claude Design prompt - Cabos Mexican Restaurant

Design a complete, production website theme for **Cabos Mexican Restaurant**, a single-location
family Mexican restaurant in Nolensville, Tennessee. I need three fully designed pages that together
define the whole system so nothing else has to be designed later:

1. **Home page** (this is also the location page - one location)
2. **Menu page**
3. **VIP club page** ("Become a VIP")

Deliver them as self-contained static HTML with one shared inline design language (no external CSS/JS
frameworks, no build step). I will wire in real content, forms, and assets myself.

## Brand identity (use the REAL brand - do not invent a new one)
Cabos is named for Cabo San Lucas. The real logo is an oval beach badge: the iconic **El Arco** rock
arch rising out of a turquoise sea under a bright blue sky, the word **CABOS** across it in an elegant
teal/turquoise serif with a white outline and a small spiral swirl inside the "O", and "MEXICAN
RESTAURANT" beneath, all ringed by a beaded border of lime-green and golden-yellow dots.

Translate that into the site:
- **Palette:** turquoise/teal as the primary, ocean + sky blue, warm sandy tan / off-white paper as the
  base, with lime-green and golden-yellow as celebratory accents. Bright, sunny, coastal - NOT dark,
  NOT rustic-stone. Think Baja beach daylight.
- **Motifs (use sparingly, tasteful):** the arch silhouette, gentle waves, sun, the beaded-dot border as
  a divider or frame element. Draw these as inline SVG; do not use the photographic logo as a texture.
- **Type:** a friendly, characterful display face for headings that echoes the logo's warmth (rounded or
  humanist), paired with a clean, highly legible sans for body. Self-host both as woff2 (see performance).
- **Tone:** welcoming neighborhood cantina by the sea. Confident, fun, appetizing.

## Pages and sections

### Home
- **Text-forward hero** (large brand headline as the largest text element - see performance note; do
  NOT make a full-bleed background image the LCP). Headline, one-line subhead, two primary CTAs:
  "Order Online" and "Join the VIP Club". Room for a small supporting dish image as an accent, lazy-loaded.
- **Intro / welcome** short paragraph about fresh, made-daily Mexican food, Baja spirit.
- **Featured dishes** - a grid of 6 dish cards (image + name + short description). I will drop in real
  photos (chimichanga, diablo shrimp, chicken tacos, birria tacos, guacamole, enchiladas, quesadilla).
- **Reviews** - a horizontal, swipeable card scroller of customer reviews (stars + quote + name). Must
  not cause page-level horizontal scroll on mobile (contain it).
- **Visit us** - address, phone, hours, and a **click/scroll-to-load map placeholder** (a styled facade
  that upgrades to a Google Maps embed; keep Google Maps off the initial critical path).
- **Contact** - a "Get in Touch" form (First name, Last name, Email, Phone, Message). Design the form
  states (default, loading, success, error). Also design a reusable modal version if easy.
- Sticky header (logo left, nav, an "Order Online" CTA, mobile hamburger + menu). Footer with hours,
  address, social links, and a "Powered by Chowdown" line.

### Menu
- Full-menu layout for a LARGE menu (20-30 categories, 150+ items) - this is real, dense content.
- A **sticky category filter bar** (horizontally scrollable pills) that shows one category at a time,
  plus an "All" view. Clean two/three-column masonry of items (name, price, description; optional dish
  photo). Design must stay readable and fast with hundreds of items. Include an allergen/footnote style.

### VIP club
- Beachy, celebratory hero ("Join the Cabos VIP Club"), 3 perks with icons, and a signup form
  (First name, Last name, Phone, Email, Date of birth) with a "Get My Pass" button, plus a success state
  that reveals "Add to Apple Wallet / Google Wallet" buttons. Design a marquee/announcement band if it fits.

## Hard requirements (these are non-negotiable, please build them in)
- **Mobile-first.** Every layout must be flawless at 390px wide with zero horizontal page scroll. Any wide
  element (menu filter, review scroller, tables) scrolls inside its own container, never the page body.
- **Performance (target Lighthouse mobile 95-100).** Self-host fonts as woff2 with `font-display:swap`
  and NO preload; do not put a heavy image or map as the LCP element - the hero headline text should be
  the LCP. Lazy-load all below-the-fold images and the map. Keep JS minimal and inline.
- **Accessibility (target 100).** Proper heading order (single h1, then h2/h3), a `<main>` landmark, all
  color pairs pass AA contrast (careful with turquoise/yellow on light backgrounds), labeled form fields,
  focus states, alt text placeholders.
- **No em dashes or en dashes anywhere** in copy or code (use commas/periods; restructure instead).
- **No emojis anywhere.** Use inline SVG icons only.
- Give me clean, semantic HTML with the design as one inline `<style>` block per page, using CSS custom
  properties (design tokens) so the palette/spacing/type scale are centralized and reusable.
- Include the section structure and class names consistently across all three pages so the header,
  footer, buttons, cards, and forms are shared components.

## What to hand back
Three HTML files (home, menu, VIP) plus the woff2 font files (or links to the exact Google Fonts families
and weights you used so I can self-host them). Keep everything self-contained and copy-paste runnable.
