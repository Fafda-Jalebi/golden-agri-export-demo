# Agri Export Co. — Business Website Demo

A polished, responsive agricultural export business website demo built with HTML5, CSS3, and vanilla JavaScript. This project showcases frontend development, UI/UX implementation, responsive design, semantic HTML, CSS architecture, vanilla JavaScript interactions, visual branding, product presentation, and professional business-site structure.

**Agri Export Co. is a fictionalized/anonymized public portfolio demonstration.** All company information, branding, contact details, imagery, and location information in this public demo are fictional and created for portfolio purposes.

---

## 🚀 Live Demo

[🚀 Live Demo](PLACEHOLDER)

> **Placeholder:** The live deployment URL is not available yet. Update this link once the site is deployed (e.g., to GitHub Pages).

---

## 1. Overview

This project is a **single-page business website** for a fictional agricultural export company. It is designed as a frontend-development showcase rather than a functioning commercial service — its purpose is to demonstrate how a professional, export-focused business website is structured, styled, and made interactive.

The target use case is a **business-to-business exporter website** aimed at importers, wholesalers, and export buyers. The demo exercises common frontend-development goals: clear information hierarchy, a strong visual brand presence, structured product presentation, and content that walks a visitor from first impression to a contact/inquiry action.

The project emphasizes why responsive business websites need **clear information hierarchy** (a distinct hero, product, quality, facility, export, and contact flow) and **strong visual presentation** (consistent color treatment, card-based organization, and product-focused imagery) to feel credible and trustworthy to professional buyers.

---

## 2. Key Features

What the demo actually implements:

- **Responsive business website** — desktop, tablet, and mobile layouts
- **Mobile navigation menu** — hamburger toggle with open/close state and ARIA state management
- **Hero/value proposition section** — headline, brand points, and call-to-action
- **Product showcase** — two fictional coriander seed products presented as cards
- **Product cards** — each with image, name, tagline, and feature points
- **Product gallery** — brand and product imagery presentation
- **Quality/process section** — source → pack → export flow
- **Facility showcase** — generic office/facility demo illustrations
- **Export-focused content** — importer/wholesale/export messaging
- **Regional Gujarat presence section** — location copy with an embedded Google Maps regional view
- **Google Maps regional view** — embed of Gujarat (regional-level, no business marker)
- **Contact/inquiry section** — phone/email/office inquiry UI using fictional demo information
- **Responsive footer** — brand summary and contact links
- **Scroll reveal animations** — IntersectionObserver-based reveal on scroll
- **SEO metadata** — page title and meta description
- **Open Graph metadata** — social sharing title and description
- **JSON-LD structured data** — schema.org LocalBusiness markup
- **Accessible image alt text** — descriptive alt text on all images
- **Semantic HTML structure** — `header`, `nav`, `main`, `section`, `footer`

This is a **static frontend project**. It does not include a backend, database, authentication, API, AI, payment processing, CMS, real e-commerce, or real order processing.

---

## 3. Website Sections

### Hero
The opening section states the value proposition ("Premium coriander seeds for reliable export supply"), highlights brand strengths, and includes a call-to-action to view products. A visual product showcase presents the packaging imagery.

### Product Range
Presents the two fictional coriander seed product lines — **Platinum Green** and **Gold Green** — as styled cards with imagery, taglines, and supporting feature points. Content is fictional demo product presentation.

### Quality Mindset
A source → pack → export presentation that communicates a quality-first narrative for export buyers. The three steps show how the demo frames sourcing, packing, and export preparation.

### Brand Gallery
A visual brand and product gallery section that presents the fictional logo and packaging imagery in a structured gallery layout.

### Location & Facility
Showcases generic office and facility demo illustrations alongside copy establishing a "ground presence" for the export trade. This section sets up the Gujarat regional presence.

### Why Choose Us
Presents quality assurance and market experience messaging as the demo's credibility-building content, framed as reasons for buyers to choose the fictional company.

### Export Focus
An export banner focused on importer/wholesale/export messaging — "From Gujarat to your market, with a brand buyers can remember."

### Contact
A contact/inquiry section with phone, email, and office fields. All contact details are **fictional demo information** (placeholder phone, fictional email, fictional office location) and do not reference any real business.

---

## 4. UI/UX Design

The visual design uses a consistent, professional agricultural theme:

- **Dark earthy background** — deep neutral background tones (`--forest`)
- **Green/olive agricultural accents** — leaf-tone surfaces (`--leaf`)
- **Gold highlights** — metallic gold accent color (`--gold`) for key highlights and accents
- **High-contrast typography** — strong contrast between text and the dark background for readability
- **Card-based content organization** — products, quality steps, and features presented in cards
- **Clear CTA hierarchy** — a primary hero call-to-action plus in-page navigation buttons
- **Product imagery** — consistent use of packaging and brand visuals throughout
- **Responsive navigation** — fixed header with a hamburger menu that expands on mobile
- **Consistent spacing** — section-based layout with uniform rhythm
- **Visual section separation** — alternating section treatments to guide the eye down the page
- **Mobile-first considerations** — layout collapse and stacking at tablet/mobile breakpoints
- **Scroll-based reveal effects** — content fades/animates in as it enters the viewport

The design is implemented directly in CSS with **CSS custom properties** for the color palette and spacing tokens — there is no third-party CSS framework.

---

## 5. Technical Implementation

### HTML5
- Semantic structure with `header`, `nav`, `main`, `section`, and `footer` elements
- Distinct, labeled sections for each content area (hero, products, quality, gallery, facility, why-choose-us, exports, location, contact)
- SEO metadata: page `<title>` and `<meta name="description">`
- Open Graph metadata: `og:title` and `og:description`
- JSON-LD structured data: `schema.org` `LocalBusiness` markup
- Accessible attributes: `aria-label` on navigation toggle and decorative containers, `aria-expanded` state on the menu button, `alt` text on every image, and a `title` on the embedded map iframe
- Responsive viewport meta tag

### CSS3
- **CSS custom properties** — design tokens (colors such as `--forest`, `--leaf`, `--gold`) defined in `:root` and reused via `var()` throughout
- **Flexbox** — used for navigation and layout alignment
- **CSS Grid** — used for product, feature, and gallery layouts (26 grid layout rules)
- **Responsive media queries** — breakpoints at `900px`, `768px`, and `640px`, plus a `prefers-reduced-motion: reduce` block
- **Animations/transitions** — smooth transitions for interactions and reveal effects
- **Responsive image handling** — `object-fit` (contain/cover) so imagery scales correctly across layout sizes

### Vanilla JavaScript
`script.js` (39 lines, no dependencies) implements the following, all guarded with optional chaining (`?.`) so missing elements never throw errors:

- **Header state** — toggles a `scrolled` class on the header when the page is scrolled past 16px, via a passive scroll listener
- **Mobile navigation** — the hamburger button toggles an `open` class on the nav and keeps the `aria-expanded` attribute in sync
- **Navigation state cleanup** — clicking any nav link closes the mobile menu and resets `aria-expanded`
- **Scroll reveal animations** — an `IntersectionObserver` (threshold `0.14`, `-60px` root margin) adds a `visible` class to `.reveal` elements as they enter the viewport, then unobserves them

No external libraries, frameworks, build tools, or network requests are used.

---

## 6. Responsive Design

The layout is fully responsive and adapts across three ranges:

- **Desktop** — multi-column grids (products, features, gallery) with side-by-side split sections; full horizontal navigation
- **Tablet** — grids collapse at `900px` and `768px`; the header compacts and navigation switches to the hamburger menu
- **Mobile** — single-column stacking at `640px`; sections, cards, and contact layout stack vertically; the mobile nav menu overlays the top of the page

The responsive navigation (hamburger toggle + ARIA state) and the grid-to-single-column transitions are implemented in CSS media queries with JavaScript-driven nav state. Images use `object-fit` to scale cleanly within their frames at every breakpoint.

---

## 7. SEO & Accessibility

What is actually implemented:

- **Page title** — "Agri Export Co. | Premium Coriander Seed Exporter"
- **Meta description** — a concise, fictional demo description
- **Open Graph metadata** — `og:title` and `og:description` for social sharing
- **JSON-LD** — `LocalBusiness` structured data (fictional, generic Gujarat-region data only)
- **Semantic HTML** — `header`, `nav`, `main`, `section`, `footer` landmarks
- **Image alt text** — every `<img>` has descriptive alt text
- **Navigation accessibility** — `aria-label` on the toggle button and `aria-expanded` reflecting menu state
- **ARIA labels** — used on the nav toggle and informative containers
- **iframe title** — the Google Maps embed has a descriptive `title`

No claim of automated accessibility scores is made; these are the accessibility and SEO practices present in the source.

---

## 8. Project Structure

```text
golden-agri-export-demo/
├── assets/
│   ├── demo-brand.png
│   ├── demo-facility-market.png
│   ├── demo-facility-signage.png
│   ├── demo-facility-yard.png
│   ├── demo-logo.png
│   ├── demo-pack-gold.png
│   └── demo-pack-green.png
├── index.html
├── styles.css
├── script.js
├── README.md
└── .gitignore
```

---

## 9. License

No license is applied. Developed as a personal portfolio demonstration project.
