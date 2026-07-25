# ACADIO.AGENCY — Complete Design System Analysis

> **URL:** https://acadio.agency  
> **Platform:** WordPress 7.0.1 / Harington Theme v7.0.1 (Child Theme)  
> **Analysis Date:** July 2026

---

## 1. Brand Identity

**Brand Personality:** Bold, Brave, Iconic, Simple, Louder — these five words are literally the first thing a user sees (the preloader cycles through them). The brand positions itself as a confident, no-nonsense agency that marries creative ambition with strategic clarity.

**Luxury / Premium / Modern / Minimal / Creative:** Acadio sits at the intersection of **Premium Minimal** and **Bold Modern**. It is aspirational without being inaccessible. The phrase "Raise Your Empire" and "We make it trendy" signal self-assuredness. The overall tone is **corporate-creative** — credible enough for real estate developers and banks, visually bold enough for a creative agency.

**Tone of Voice:** Direct, declarative, slightly provocative. Uses short commanding phrases: "Raise Your Empire", "We make it trendy", "Cutting-edge digital services". No jargon, no fluff. The voice positions Acadio as a partner who gets things done.

**Target Audience:** C-suite executives and marketing directors at real estate developers, banks, hospitality groups, and retail brands in Egypt and the GCC. 50+ client logos on the homepage (Tatweer Misr, Palm Hills, Vodafone, Bank Audi, Al-Futtaim) confirm a B2B focus on established enterprises.

**Emotional Feeling:** Ambitious, trustworthy, premium, avant-garde. The user feels they are in the presence of a market leader.

**Trust Signals:** 500+ clients claim, 50+ recognizable brand logos, case studies with concrete deliverables, Google Analytics + Ads + Tag Manager + Site Kit integration, Rank Math SEO, Google site verification, physical office address in First Settlement Cairo.

---

## 2. Design Style

### Colors

| Token | Value | Usage |
|-------|-------|-------|
| Primary accent | `#ff0f0f` | Theme primary color (set in body data attribute) |
| Background light | `#eeeeee` | Main page background (home, about, services) |
| Background white | `#ffffff` | Client logos section, contrast sections |
| Text dark | `#171717` / `#222` | Body text, header menu color |
| Text light | `#ffffff` | On dark/overlay sections |
| Logo dark | Custom dark | Default logo |
| Logo white | Custom light | Inverted header state |

**Why:** The `#eeeeee` near-white background is a deliberate move away from pure white. It softens the canvas, reduces eye strain, and gives the site a tactile, editorial quality — like luxury magazine paper. The red `#ff0f0f` is used sparingly as a dynamic accent (cursor ball, hover states). This restraint makes the red feel intentional and powerful when it appears.

### Typography

| Role | Font Family | Weight | Size | Case |
|------|-------------|--------|------|------|
| Hero heading | `basis_grotesque_promedium` | 500 | 9vw (scales down to 14vw on mobile) | Uppercase |
| Hero subtitle | `basis_grotesque_promedium` | 400 | 20px (14px mobile) | Uppercase |
| Body / Navigation | `Poppins` | 300-700 | 14px base | Uppercase (global setting) |
| Display / Numbers | `Six Caps` | 400 | Large | Uppercase |
| Section numbers | Theme default | — | Small, faded | — |

**Font Hierarchy:**

- **H1 (Hero):** 9vw, `basis_grotesque_promedium`, uppercase — massive, commanding
- **H2 (Section Titles):** `Six Caps` or `basis_grotesque_promedium`, large uppercase
- **H3-H4 (Service names, body headings):** Poppins, various weights
- **H5-H6 (Subtitles, metadata):** Smaller Poppins, uppercase
- **Body:** Poppins, regular weight

**Why:** The pairing of `basis_grotesque_promedium` (a geometric grotesque — modern, clean, slightly condensed) with `Poppins` (warm, rounded geometric) creates tension between modernity and approachability. `Six Caps` (all-caps display face) adds a third texture for numerals and section indicators — decorative but not distracting. The **global uppercase** setting (`<body class="uppercase-text">`) is a bold choice: it makes everything feel official, monumental, and designed. Trade-off: reduced readability for long paragraphs, but Acadio keeps copy short.

### White Spacing

Generous. Hero section has `padding-top: 220px` (160px on tablet, 120px on mobile). Content sections use `80px` horizontal padding (scales to 60px → 40px → 30px → 20px). Vertical spacing between sections uses `100px+` via `row_padding_bottom`, `row_padding_top` classes.

**Why:** Luxury brands breathe. The spacing signals confidence — no need to cram information. Each section is a distinct visual rest.

### Grid System

- **Layout containers:** `content-max-width` (max-width: 1320px + 80px padding) and `content-full-width` (100% width + 80px padding)
- **Content:** Columns use WordPress block editor's `wp-block-columns` with flexbox
- **Portfolio/Projects:** CSS Grid-like layout via `flex-grid` class, powered by Isotope.js for filtering
- **Showcase:** Horizontal list layout with hover-reveal thumbnails

**Why:** A hybrid approach — constrained content width for readability, full-width for immersive sections (hero, portfolio grid, marquee titles). This creates dynamic rhythm between contained and expansive.

### Layout Philosophy

**Asymmetrical balance + generous negative space + anchor typography.** Titles live in the top-left or span full-width. Text content often sits in narrow columns (~30-40% width). The hero has an indented last word (the "Empire" in "Raise Your Empire" is offset `left: 400px`).

**Why:** Editorial asymmetry keeps the eye moving and prevents monotony. The indented hero word is a signature gesture — it adds visual surprise and emphasizes the final word.

### Border Radius

Effectively **0** or near-zero throughout. Buttons use `rounded` class sparingly (small border radius). The cursor ball is circular. Everything else is sharp-edged.

**Why:** Sharp corners communicate precision, modernity, and seriousness. Rounded corners would soften the brand's bold personality.

### Shadows

No noticeable drop shadows. The design uses **layering, opacity, and parallax depth** instead of CSS shadows. The hover-reveal thumbnail in the showcase is a pure overlay, not a shadow.

**Why:** Shadows belong to skeuomorphic eras. This is a flat/modern design that creates depth through motion (parallax, scale transitions).

### Cards

The portfolio items are essentially **image cards** with overlay text. Each consists of:

- Full-bleed image (sometimes with video)
- Title overlay on hover
- Category tags
- Color data attribute for hover state
- Parallax movement on scroll

**Why:** Image-first, text-second. The work speaks louder than words. Cards are designed for browsing, not reading.

### Icons

**Font Awesome 6** (free/regular/brands). Used sparingly: social media icons, arrow-down for scroll indicator, share icon in footer. No decorative icon sets for features — they use text lists instead.

**Why:** Semantic minimalism. Icons are functional only (navigation, social), never ornamental.

### Illustrations

**None.** The site uses zero illustrations. All visual storytelling is through photography and video.

**Why:** Photography of real work builds more trust with B2B clients than abstract illustrations would.

### Images

High-resolution, professional photography. Images use `srcset` for responsive loading. Galleries use Magnific Popup for lightbox viewing. The portfolio uses a `grid__item-img` + `grid__item-img--large` pair (small thumbnail + large reveal image) for smooth zoom transitions.

**Why:** Investment in professional imagery signals investment in quality work.

### Backgrounds

Almost exclusively `#eeeeee` (light gray). White (`#ffffff`) used selectively to break sections. No textures, no patterns, no noise overlays. The marquee text section uses large text as a background element itself.

**Why:** The near-white gray is a signature background color — distinctive enough to be memorable, subtle enough to not compete with content.

### Gradients

None on the site itself. The GS Logo Slider plugin has tooltip gradients (`#ff5f6d` to `#ffc371`) but these are plugin defaults, not intentional design choices.

**Why:** Gradients would conflict with the flat, bold, editorial aesthetic.

---

## 3. Overall Structure

### Pages

| # | Page | Purpose |
|---|------|---------|
| 1 | **Home** | Convert visitors into leads / showcase top work |
| 2 | **About Us** | Build trust, tell origin story |
| 3 | **Services** | Detail offerings, drive inbound inquiries |
| 4 | **Work/Projects** | Portfolio with filtering, prove capability |
| 5 | **Project Single** | Deep-dive case study |
| 6 | **Clients** | Social proof via logo wall |
| 7 | **Stories** | Blog / thought leadership |
| 8 | **Contact** | Lead capture |
| 9 | **Careers** | Recruitment |

### Page Deep-Dives

**HOME**

- **Sections:** Preloader → Header → Hero ("Raise Your Empire") → Portfolio Grid (3 featured projects) → Services list → Client logos carousel → Marquee "Our Success Partners" → More works showcase (hover-reveal list with video) → Page nav (About link) → Footer
- **Hierarchy:** Tagline → Featured work → What we offer → Who trusts us → More proof
- **CTAs:** "Scroll To Explore", Portfolio item clicks, "Check our services", "View Our Success Partners", "SEE ALL" (projects), "Read About Us"
- **Journey:** Visitor scans massive hero → sees work → sees services → sees recognizable client logos —> trusts → clicks either to services or work

**ABOUT US**

- **Sections:** Hero "We are ACADIO!" → Story / overview → "500+ clients" stat → Values (Approach, Mission, Vision) → Contact CTA
- **Purpose:** Humanize the agency, explain the "why"

**SERVICES**

- **Sections:** Hero "Cutting-edge digital services" → 6 service blocks (Branding, Media Production, Social Media, Digital Advertising, PR, Events) → Closing CTA
- **Each service block:** Numbered section (01-06) → Title → Description paragraph → Deliverable list
- **Purpose:** SEO-optimized service pages, answer client questions

**WORK (Projects)**

- **Sections:** Hero "We Make it Trendy" → Filter bar (All, Branding, Digital, Outdoor, Video, Web) → Infinite/masonry project grid → CTA
- **Filter:** Isotope-powered category filtering
- **Purpose:** Show don't tell

**PROJECT SINGLE (e.g. Capital Elite)**

- **Sections:** Hero with title → Gallery grid → Project description → Deliverables → Concept/story section → Press conference details → Full gallery → Next project navigation
- **Purpose:** Complete case study for convincing leads

**CLIENTS**

- **Sections:** Hero "Our Clients" → "500+ clients" statement → Logo grid (50 logos) → Contact CTA
- **Purpose:** Maximum social proof

**STORIES (Blog)**

- **Sections:** Hero "Read All News" → Featured stories → Paginated article grid with images, dates, categories
- **Purpose:** SEO content, thought leadership

**CONTACT**

- **Sections:** Hero "Get In Touch" → Contact form → Office address → Social links → Map
- **Purpose:** Lead capture

**CAREERS**

- **Sections:** Hero "Join our team" → Pitch paragraph → Application form
- **Purpose:** Recruitment

---

## 4. Components

### Reusable Components

**1. Header / Navigation**

- Sticky header with logo (dual-state: black/white logo swap on scroll or section change)
- Full-screen menu overlay triggered by burger icon
- Menu items have hover underline animation (`<span data-hover="Home">`)
- `data-type="page-transition"` on all links for AJAX navigation
- 8 items: Home, Projects, About, Clients, Services, Stories, Contact, Careers

**2. Hero Section**

- Massive typography (9vw, uppercase)
- Indented last word effect
- Optional background image/video
- "Scroll To Explore" footer indicator
- Animated title spans (translateY 160px → 0 on load)
- Subtitle with max-width 30%

**3. Preloader**

- Full-screen overlay on initial load
- Cycles through 5 words: bold, brave, iconic, simple, louder
- Progress bar + percentage counter
- "Loaded" text completion indicator

**4. Buttons (3 variants)**

- **Arrow button:** `button-wrap` with `icon-wrap` + `button-text`. Has parallax micro-motion on hover. Icon is a diagonal arrow.
- **Border button:** `clapat-button` with `button-border rounded`. Used for "SEE ALL".
- **Text link:** Inline text links with `data-hover` attribute for hover swap effect.

**5. Portfolio Grid Item**

- `item` div with data-category attributes
- Parallax wrapper for scroll-based movement
- Image with `grid__item-img` + `grid__item-img--large` for hover zoom transition
- Overlay caption on hover (title + category)
- AJAX link to project page
- Optional video background

**6. Showcase List Item**

- Horizontal list layout
- Hover-reveal thumbnail (image smoothly scales up and follows cursor)
- Title + subtitle text
- Color data attribute for background tint on hover
- AJAX link

**7. Marquee Text**

- Full-width scrolling text (`marquee-text`)
- Used for section titles like "OUR SUCCESS PARTNERS •"
- Continuous horizontal scroll via CSS/JS

**8. Client Logo Carousel**

- GS Logo Slider plugin
- Swiper.js driven
- Autoplay with 2s delay
- 5 logos per row desktop, 3 tablet, 2 mobile
- Tooltip on hover with client name

**9. Page Navigation**

- Full-width section at bottom of each page
- Links to next logical page (About, Work, Contact)
- "Next page" title with underline animation
- Subtitle beneath ("We would love to hear from you.")
- Marquee effect on title

**10. Footer**

- Hidden footer (minimal)
- Back to top button with `arrow-icon-up`
- Copyright center: "Acadio © 2024"
- Social icons: Facebook, Instagram, LinkedIn, TikTok, Vimeo

**11. Custom Cursor**

- `#magic-cursor` with `#ball`
- Follows mouse with smooth lag
- Changes state for drag, load, click
- Parallax micro-motion on interactive elements

**12. Contact Form**

- Contact Form 7 plugin
- Fields: Name, Email, Subject, Message
- AJAX submission
- Google Site Kit event tracking

**13. Section Number Indicators**

- Numbers like "01", "02" used as decorative section markers
- Small, light weight, positioned above section titles
- Consistent across Services, About, Contact pages

**14. Image Gallery (Lightbox)**

- Magnific Popup integration
- Grid layout of project images
- Click to open full-screen gallery navigation

---

## 5. Animations

### Complete Animation Inventory

| Animation | Implementation | Duration | Easing | Purpose |
|-----------|---------------|----------|--------|---------|
| **Preloader** | Custom JS + CSS | ~2-3s | Linear | Brand imprinting, perceived performance |
| **Hero title entrance** | GSAP | ~1.2s | Custom ease | Dramatic reveal — each line translates from 160px below |
| **Hero subtitle entrance** | GSAP | ~0.8s | Custom ease | Follows title, staggered |
| **Hero footer fade-in** | CSS/JS | ~0.6s | Ease-out | Delayed fade + slide up |
| **Page transition** | AJAX + GSAP | ~0.6s | Cubic bezier | Cover-layer wipe between pages |
| **Smooth scroll** | Smooth Scrollbar library | Continuous | Custom | Parallax-enabled, inertia-based scrolling |
| **Parallax scroll** | ScrollMagic + GSAP | Scroll-driven | Linear | Depth illusion on images and content |
| **Portfolio item hover** | CSS + JS | ~0.4s | Ease-out | Image zoom (scale), caption overlay slide |
| **Showcase hover reveal** | GSAP | ~0.3s | Power2.out | Thumbnail follows cursor, smooth scale-up |
| **Menu open/close** | GSAP | ~0.5s | Ease-in-out | Full-screen menu slide/opacity |
| **Menu item stagger** | GSAP | ~0.05s each | — | Sequential reveal of nav items |
| **Marquee scroll** | CSS translateX | Continuous | Linear | Infinite horizontal text scroll |
| **Scroll-triggered text reveal** | ScrollMagic + GSAP | ~0.8s | Power2.out | Text mask-fill animation (clip-path or opacity) |
| **Button parallax** | GSAP (on mousemove) | Real-time | — | Micro-interaction on icon/text within buttons |
| **Custom cursor** | JS (requestAnimationFrame) | Real-time | Smooth linear | Mouse follower with ball |
| **Image zoom on scroll** | ScrollMagic + scale | Scroll-driven | Linear | Background image scale (1→1.02) |
| **Loading state** | Ball-loader | Spinning | — | Shows during AJAX transitions |
| **Scroll progress bar** | JS | Scroll-driven | Linear | 2px progress bar on project pages |
| **Next project auto-scroll** | JS timer | ~5s delay | — | Auto-advance to next project on scroll pause |

### Animation Philosophy

Every animation serves a narrative purpose:

- **Hero entrance is slow and grand** — this is the first impression
- **Parallax is subtle** (not gimmicky) — adds depth without distracting
- **Hover effects are fast** (0.3-0.4s) — responsive, not sluggish
- **Page transitions are smooth and opaque** — the cover-layer wipe creates continuity between pages without the flash of full page loads
- **Text reveals use motion + opacity** — never just opacity alone, always with translateY for physicality

---

## 6. UX Analysis

### Navigation

- **Primary:** Full-screen hamburger menu. 8 items, no dropdowns. This is intentionally flat — every page is equally important, and the agency wants you to explore freely.
- **Secondary:** On-page links ("View Our Success Partners", "SEE ALL", "Read About Us") guide flow.
- **Tertiary:** Project-to-project navigation via auto-advance + manual next/prev.

**Strength:** Minimalist nav reduces cognitive load. **Weakness:** No dropdown means services are hidden behind one click; the Services page has to do heavy lifting.

### Visual Hierarchy

- Massive hero headlines (9vw) dominate — this is intentional brand-first messaging
- Section headers use `has-mask-fill` (GSAP text reveal) to draw attention
- Body content stays narrow (30-40% width) for readability

### Readability

The global `uppercase-text` setting reduces readability for long text. However, Acadio compensates by keeping body copy **short**. On the about page, paragraphs are 1-3 sentences. The longest text is on project case studies, which is lowercase in the content area.

### Accessibility

- Skip nav? Not present
- Alt texts: Present on images (descriptive alt attributes)
- Color contrast: High contrast (dark text on `#eeeeee`) — good
- Focus indicators: Relying on custom cursor, keyboard focus not clearly styled
- ARIA: Not heavily used
- **Issue:** The custom cursor may interfere with standard pointer events

### Call to Action Placement

CTAs follow a predictable pattern:

1. **Above fold:** Scroll prompt (soft CTA)
2. **Mid-page:** Text links to services/work (medium CTA)
3. **End of section:** Border buttons ("Check our services", "SEE ALL")
4. **End of page:** Full-width "Read About Us" / "Get in Touch" (strong CTA)
5. **Footer:** Back to top + social (utility)

**Strategy:** No aggressive CTAs. The site assumes the visitor is evaluating and needs to be convinced through portfolio quality, not sales pressure.

### Scrolling Behavior

- Smooth scroll with inertia (Scrollbar plugin)
- Content sections are full-viewport or near-full-viewport tall
- Parallax creates depth while scrolling
- Portfolio items trigger on scroll reveal

### Mobile Experience

- Hero text scales from 9vw → 14vw (even larger on mobile — bold choice)
- Menu switches to full-screen overlay
- Padding scales from 80px → 20px
- Footer button text hidden on mobile
- Swiper for client logos adjusts to 2 per row
- Portfolio grid stacks to single column

### Conversion Optimization

- **Every page leads to Contact** via bottom nav or explicit "Get in Touch" links
- Social proof is everywhere: clients, case studies, 500+ stat
- Form on Contact page, form on Careers page (CF7)
- No popups, no exit intent — high trust, low pressure
- Page transitions keep user in the experience (no jarring reloads)

### User Flow (Typical)

```
Land on Home → See hero → Scroll to featured projects → Click project → Read case study → Navigate to Services → Read → Click Contact → Fill form
```

OR:

```
Land on Home → See client logos → Click to Clients page → See 50+ known brands → Click Contact
```

---

## 7. Responsive Strategy

### Breakpoints (from CSS)

| Breakpoint | Type | Padding | Hero Size | Changes |
|------------|------|---------|-----------|---------|
| >1537px | Desktop | 80px | 9vw | Full experience |
| 1466px | Small desktop | 60px | 8vw | Reduced hero height |
| 1024px | Tablet landscape | 40px | 10vw | Indent removed, footer padding reduced |
| 767px | Tablet portrait | 30px | 12vw | Button text hidden in hero, single column |
| 479px | Mobile | 20px | 14vw | Minimal padding, maximum text size |

### Navigation Changes

- **Desktop:** Nav links hidden behind burger menu (always full-screen menu)
- **All sizes:** Same full-screen menu approach — no breakpoint change in nav pattern

### Spacing Scale

- 80px → 60px → 40px → 30px → 20px (horizontal padding)
- 220px → 160px → 120px (hero top padding)
- 100px → 60px → 40px (section vertical spacing)

### Typography Scaling

- Hero: 9vw → 8vw → 10vw → 12vw → 14vw (it *grows* on mobile — deliberate emphasis)
- Subtitle: 20px → 14px (tablet+)
- Content: Unchanged (body text stays readable)

### Component Behavior

- Portfolio grid: Multi-column → single column
- Client logos: 5 per row → 3 → 2
- Showcase list: Horizontal scroll → stacked
- Content columns: Side-by-side → stacked

---

## 8. Technical Analysis

### Platform

- **CMS:** WordPress 7.0.1
- **Theme:** Harington (by Clapat) v7.0.1 with child theme
- **Page Builder:** WordPress Block Editor (Gutenberg) with Harington custom blocks

### Technologies & Libraries

| Category | Technologies |
|----------|-------------|
| **Core** | WordPress, PHP, MySQL, jQuery |
| **Animation** | GSAP 3, ScrollMagic, ScrollTrigger, Smooth Scrollbar, Three.js (WebGL) |
| **UI/Sliders** | Swiper.js, GS Logo Slider, FlexNav, Isotope, Packery |
| **Lightbox** | Magnific Popup |
| **Gallery** | Justified Gallery |
| **Icons** | Font Awesome 6 (Free) |
| **Fonts** | Google Fonts (Poppins, Six Caps), Custom (basis_grotesque_promedium) |
| **Forms** | Contact Form 7, CF7 Redirect |
| **SEO** | Rank Math SEO, Schema.org JSON-LD |
| **Analytics** | Google Analytics (G-X4JDVERK68), Google Ads (AW-876329674), Google Tag Manager, Site Kit |
| **Social** | jsSocials |
| **Performance** | Lazy loading (`loading="lazy"`), `srcset` for responsive images, DNS prefetch |
| **Hosting** | Standard WordPress hosting (Apache/Nginx with `.htaccess`) |

### CSS Methodology

- BEM-like naming: `.hero-title`, `.hero-subtitle-wrapper`, `.item-caption`
- Utility classes: `content-max-width`, `content-full-width`, `light-section`, `row_padding_bottom`
- Inline styles via WordPress block editor for section-specific overrides
- CSS custom properties limited to WordPress defaults (`--wp--preset--*`)

### JavaScript Architecture

- jQuery-dependent for DOM manipulation
- GSAP for all programmatic animations
- ScrollMagic for scroll-based triggers
- AJAX page transitions via custom theme scripts
- Smooth Scrollbar for inertia-based scrolling (replaces native scroll)

### SEO Techniques

- Rank Math plugin for meta, OG tags, schema
- JSON-LD structured data (Organization, WebSite, WebPage)
- Canonical URLs
- Sitemap (WordPress default)
- Prefetch links (`dns-prefetch` for Google Fonts, Google Tag Manager)
- Speculative loading (`<script type="speculationrules">` with `prefetch`)
- Semantic HTML (H1-H6 hierarchy)

### Performance

- Images use `srcset` with multiple resolutions
- `loading="lazy"` on below-fold images
- CSS and JS files are versioned for cache busting
- No heavy custom fonts beyond 2 Google Fonts
- Heavy JS bundle (GSAP, ScrollMagic, Three.js, Swiper, etc.) is a **potential bottleneck**

---

## 9. Design Tokens

### Color Palette

```css
--color-primary:       #ff0f0f
--color-bg-light:      #eeeeee
--color-bg-white:      #ffffff
--color-text-dark:     #171717 (header) / #222 (body)
--color-text-light:    #ffffff
--color-accent-dark:   #0a0a0a (project hover overlays)
--color-overlay:       rgba(0,0,0,0.5) / rgba(255,255,255,0.3)
```

### Spacing Scale

```css
--space-xxs:  5px
--space-xs:   10px
--space-sm:   20px
--space-md:   30px
--space-lg:   40px
--space-xl:   60px
--space-2xl:  80px
--space-3xl:  100px
--space-4xl:  120px
--space-5xl:  160px
--space-6xl:  220px
```

### Border Radius

```css
--radius-none:     0px
--radius-sm:       2px   (buttons, rare)
--radius-rounded:  9999px (cursor ball only)
```

### Shadow System

```css
--shadow-none:     none
/* Depth is created via motion (parallax), not shadows. */
```

### Typography Scale

```css
--font-primary:    'Poppins', sans-serif
--font-secondary:  'Six Caps', sans-serif
--font-hero:       'basis_grotesque_promedium', sans-serif

--text-xs:     12px
--text-sm:     14px
--text-base:   16px
--text-lg:     20px
--text-xl:     26px

--heading-1:   9vw (hero)
--heading-2:   6vw (section titles)
--heading-3:   4vw
--heading-4:   24px
--heading-5:   20px
--heading-6:   14px (uppercase)

/* All headings: uppercase (global) */
```

### Button Variants

```css
.btn-arrow       → .button-wrap with icon + text, parallax on hover
.btn-border      → .clapat-button with .button-border.rounded, border style
.btn-text        → Inline text with data-hover attribute
```

### Container Widths

```css
--container-narrow:   30% (hero subtitle, text columns)
--container-content:  1320px max-width (content-max-width)
--container-full:     100% (content-full-width)
```

### Breakpoints

```css
--bp-desktop:   1538px+
--bp-sm-desk:   1466px
--bp-tablet:    1024px
--bp-mobile:    767px
--bp-sm-mobile: 479px
```

---

## 10. Strengths

1. **Loading experience is a brand moment.** The preloader cycles through five personality traits — it turns a technical necessity into brand reinforcement.

2. **Typography as hero.** The massive 9vw headlines, indented last-words, and global uppercase create an unmistakable visual signature.

3. **Restrained color palette.** The `#eeeeee` background is distinctive and editorial. It immediately separates Acadio from the sea of white-background agency sites.

4. **Parallax depth without gimmickry.** The parallax effects are subtle enough to enhance without distracting. They add a premium feel.

5. **Social proof density.** 50+ client logos on the homepage is aggressive but effective. The trust signal is undeniable.

6. **Project-first storytelling.** The portfolio gets maximum real estate. Services are listed, but work is shown. This aligns with how B2B buyers evaluate agencies.

7. **Seamless page transitions.** AJAX page loading with cover-layer transition keeps the user in a fluid experience. No white flashes, no loading spinners (except initial).

8. **Custom cursor ecosystem.** The cursor follower, combined with parallax button elements and hover state changes, creates a cohesive interactive language.

9. **Minimal footer.** Most agency sites overload the footer. Acadio uses it only for essentials: back to top, copyright, and social. The "page nav" acts as the real footer.

10. **Consistent section numbering.** The "01", "02" decorative numbers across About and Services pages tie the experience together.

---

## 11. Weaknesses

1. **Global uppercase hurts long-form readability.** The blog articles likely inherit uppercase settings, which would make extended reading fatiguing. The brand voice works best in short bursts.

2. **No mega-menu for services.** With 9 service categories, a single-level nav means potential clients have to navigate to Services page to evaluate fit. A mega-menu or dropdown could improve discovery.

3. **Heavy JavaScript payload.** GSAP + ScrollMagic + Three.js + Smooth Scrollbar + Swiper + Isotope + Magnific Popup — the cumulative JS is significant. Performance on lower-end devices may suffer, especially with smooth-scroll reimplementing native behavior.

4. **Custom cursor accessibility gap.** The custom cursor (`#magic-cursor`) may interfere with standard cursor behaviors. No visible focus indicators for keyboard navigation.

5. **No search functionality.** For a site with 50+ projects and 20+ blog posts, there's no search. Visitors cannot easily find specific case studies.

6. **Blog uses default WordPress styling.** The Stories page feels less designed than the rest of the site. The blog cards are standard, and typography inconsistencies appear.

7. **Single-color accent.** The `#ff0f0f` red is used sparingly — but in some contexts, a secondary accent could add visual warmth (especially in photography-heavy sections).

8. **Contact form friction.** The form appears only on the Contact page. When a user is deep in a case study, they must navigate away. A "Let's talk" floating button or inline form module could reduce drop-off.

9. **No testimonials section.** Despite "500+ clients", there are no client quotes or testimonials visible. The logo wall and case studies do the heavy lifting, but testimonials would add another layer of social proof.

10. **No sticky CTA.** There's no persistent "Get in Touch" or "Let's Talk" button. Users must scroll to the bottom or navigate to contact. For a conversion-focused site, this is a missed opportunity.

11. **Smooth scroll can feel sluggish.** On some devices, Smooth Scrollbar's inertia can make the site feel slow compared to native scroll.

12. **Footer copyright text is small and easy to miss.** The "Acadio © 2024" is centered but visually subtle.

---

## 12. Summary — Design Philosophy

**"Monumental Minimalism"**

Acadio's design philosophy is about making bold statements through restraint. The site doesn't use many colors — it relies on one red accent and a signature near-white gray. It doesn't use illustrations — it uses professional photography and massive typography. It doesn't have complex navigation — it has a full-screen menu and lets the work speak.

The experience is designed to feel like flipping through a high-end architecture or fashion magazine: generous white space, large images, short declarative text, and a rhythm of calm (white sections) and drama (full-bleed project grids, marquee text). Every interaction — from the preloader cycling through brand words, to the custom cursor following your mouse, to the parallax-layered project images — reinforces the brand's five core traits: **bold, brave, iconic, simple, and louder.**

The underlying UX strategy is confidence-based conversion. Rather than grabbing the user with popups, aggressive CTAs, or chatbots, Acadio says: "Look at our work. Look at who trusts us. When you're ready, we're here." This approach works exceptionally well for its B2B audience — executives and decision-makers who want to evaluate competence before committing to a conversation.

**In one sentence:** Acadio treats its website not as a brochure, but as a **portfolio exhibition** where the brand, the work, and the client list are the gallery, and the user is a VIP guest moving through curated halls.
