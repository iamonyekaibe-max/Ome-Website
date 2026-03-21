# OMÉ Essentials Shopify Store — Development Guide

**Version 1.0 · Built with Liquid & TailwindCSS**

---

## Table of Contents
1. [Brand Overview](#brand-overview)
2. [Design System](#design-system)
3. [Shopify Structure](#shopify-structure)
4. [Liquid Development](#liquid-development)
5. [Key Templates](#key-templates)
6. [Implementation Checklist](#implementation-checklist)

---

## Brand Overview

### Store Identity
- **Brand**: OMÉ Essentials
- **Domain**: omeclothing.com
- **Tagline**: "OMÉ for the everyday."
- **Positioning**: Premium essentials — effortless elegance without pretension
- **Market**: Women 25–40, US-based, intention-driven

### Brand Philosophy
- **Core Idea**: Effortless elegance. Everyday wear that feels intentional.
- **What it is**: Quality-first, timeless pieces designed for seamless transitions
- **What it's NOT**: Trend-led, loud, complicated, fast fashion

### Target Customer (The OMÉ Woman)
- Age 25–40, urban/suburban
- Confident, intentional, self-aware
- Values quality over quantity
- Wants clothes that work in multiple contexts (work → brunch → dinner)
- Not performing — style expresses how she feels
- Done with fast fashion

### Key Differentiators
1. Quality-first approach (not trend-first)
2. Effortless elegance (approachable luxury)
3. Intentional design (every detail matters)
4. Timeless pieces (not seasonal collections)
5. Made to be worn (comfort is priority)

---

## Design System

### Color Palette

| Color Name | Hex | RGB | Usage |
|------------|-----|-----|-------|
| Dark Brown | #140e06 | 20, 14, 6 | Primary text, headers, dark backgrounds |
| Ember Dark | #8b2800 | 139, 40, 0 | Strong accents, emphasis |
| Ember | #e05a18 | 224, 90, 24 | Primary accent, buttons, highlights |
| Gold | #f0a030 | 240, 160, 48 | Secondary accent, hover states |
| Rust | #7a2800 | 122, 40, 0 | Warm secondary, borders |
| Cream | #ede0cc | 237, 224, 204 | Card backgrounds, soft sections |
| Light Cream | #f7f0e6 | 247, 240, 230 | Page background |
| Muted | #b8906a | 184, 144, 106 | Secondary text, labels |
| Soft | #9a7050 | 154, 112, 80 | Tertiary text, hints |
| Rule | #e0d0bc | 224, 208, 188 | Borders, dividers |

### Typography

**Font Stack**
```
Headers/Serif: 'Bodoni Moda', 'Cormorant Garamond', serif
Body/Sans: 'Montserrat', -apple-system, BlinkMacSystemFont, sans-serif
```

**Font Weights**
- Light (300): Body text, taglines
- Regular (400): Headers, emphasis
- Bold (700): Interactive elements, CTAs

**Sizes**
- H1: 48-80px (serif, light/regular)
- H2: 28-40px (serif, regular)
- H3: 18-24px (serif, regular)
- Body: 16px (sans, light, line-height: 1.6-1.9)
- Label: 8-9px (sans, light, letter-spacing: 0.4em, uppercase)

### Spacing Scale

```
4px, 8px, 12px, 16px, 24px, 32px, 40px, 48px, 56px, 64px, 72px, 80px, 88px
```

---

## Shopify Structure

### Store Settings
- **Currency**: USD
- **Timezone**: America/New_York
- **Default Country**: United States
- **Theme Framework**: Custom Liquid theme or Prestige (modified)
- **CSS Approach**: TailwindCSS + Custom CSS

### Required Collections
1. **New Arrivals** — Latest pieces
2. **Essentials** — Core wardrobe pieces
3. **Tops** — Shirts, blouses, sweaters
4. **Bottoms** — Pants, skirts
5. **Dresses** — All dress styles
6. **Accessories** — Bags, belts, scarves
7. **Sale** — Discounted items
8. **Featured** — Hand-curated selections

### Product Attributes (Required Metafields)
- **Fabric Composition**: Text (e.g., "100% organic cotton")
- **Care Instructions**: Text (e.g., "Machine wash cold, lay flat to dry")
- **Fit**: Select (True to size / Runs small / Runs large)
- **Made-to-Order**: Boolean (yes/no)
- **Model Height**: Text (e.g., "5'9\"")
- **Material Source**: Text (e.g., "Italian linen", "Domestic cotton")
- **Sustainability Note**: Text (eco-friendly, sustainable practices)

---

## Liquid Development

### Development Framework

**Start with**: Shopify's Dawn theme (free, fast, Liquid-based)
**Modify**: Customize to match OMÉ brand aesthetic
**Extend**: Add custom sections and metafield displays

### Liquid File Structure

```
theme/
├── assets/
│   ├── app.css (compiled from TailwindCSS)
│   ├── theme.css (OMÉ-specific styles)
│   └── fonts/ (Bodoni Moda, Cormorant Garamond, Montserrat)
├── sections/
│   ├── header.liquid
│   ├── footer.liquid
│   ├── hero.liquid
│   ├── featured-collection.liquid
│   ├── testimonials.liquid
│   ├── newsletter.liquid
│   └── custom-*.liquid
├── snippets/
│   ├── product-card.liquid
│   ├── price.liquid
│   ├── form-*.liquid
│   └── *.liquid utilities
├── templates/
│   ├── index.liquid (homepage)
│   ├── product.liquid
│   ├── collection.liquid
│   ├── page.liquid
│   ├── cart.liquid
│   └── customer/*.liquid
└── config/
    └── settings_schema.json (theme customization options)
```

### Key Liquid Variables to Use

**Shop & Store**
```liquid
{{ shop.name }}              → "OMÉ Essentials"
{{ shop.url }}               → "https://omeclothing.com"
{{ cart.total_price }}       → Total in cents
{{ featured_collection }}    → Current featured collection
```

**Product Data**
```liquid
{{ product.title }}          → Product name
{{ product.featured_image }} → Featured product image
{{ product.metafields.custom.fabric_composition }}  → Fabric info
{{ product.metafields.custom.care_instructions }}   → Care details
{{ product.available }}      → True/false in stock
{{ product.price }}          → Price in cents formatted
{{ product.compare_at_price }}  → Strikethrough price
```

**Conditionals for OMÉ Store**
```liquid
{% if product.metafields.custom.made_to_order %}
  <span class="badge-made-to-order">Made to Order</span>
{% endif %}

{% if product.compare_at_price %}
  <span class="sale-badge">Sale</span>
{% endif %}

{% if product.available %}
  <button>Add to Cart</button>
{% else %}
  <span class="out-of-stock">Out of Stock</span>
{% endif %}
```

---

## Key Templates

### 1. Homepage (index.liquid)

**Structure**:
```
1. Hero Section
   - Full-width image/video
   - Headline: "OMÉ for the everyday"
   - Subheading: "Effortless elegance"
   - CTA: "Explore Essentials"

2. Featured Collection (Essentials)
   - "Shop Core Pieces"
   - 4-6 hero products in grid
   - Each card shows: image, name, price, quick-add

3. Brand Story Section
   - Headline: "Who Is OMÉ?"
   - 2-3 sentence brand essence
   - Link to About page

4. Trust Indicators
   - "Quality Essentials" — emphasis on materials
   - "Made to Wear" — comfort first
   - "Thoughtfully Made" — intentional design

5. Testimonials
   - Customer quotes about versatility
   - Show how pieces work in multiple contexts

6. Newsletter
   - "Get 10% Off Your First Order"
   - Email input + subscribe button
   - Privacy note
```

**Liquid Pattern**:
```liquid
<section class="hero">
  <div class="hero-content">
    <h1>{{ page.title }}</h1>
    <p>{{ page.content }}</p>
    <a href="/collections/essentials" class="btn btn-primary">
      Explore Essentials
    </a>
  </div>
</section>

{% for product in collections.essentials.products limit: 6 %}
  {% include 'product-card' %}
{% endfor %}
```

### 2. Product Page (product.liquid)

**Structure**:
```
1. Product Images
   - Multi-angle gallery (min 5 images)
   - Thumbnail carousel
   - Zoom capability
   - Color/variant swatches

2. Product Details (Right Side)
   - Title
   - Rating + review count (Judge.me)
   - Price (with sale strikethrough)
   - In-stock badge
   
3. Product Info Section
   - Fabric Composition (metafield)
   - Care Instructions (metafield)
   - Fit Info (metafield)
   - Material Source (metafield)
   - Sustainability note (if applicable)

4. Variant Selection
   - Size dropdown (XS-XXL)
   - Color swatches (with image change)
   - Quantity selector

5. Call-to-Action
   - "Add to Cart" button (prominent)
   - Save for later / Share buttons
   - Estimated delivery date

6. Below Fold
   - Returns & shipping info
   - "How to Style This Piece" section
     - 3-4 outfit combinations
     - Link to similar items
   - Size Guide
   - Trust badges

7. Related Products
   - "Complete the Look"
   - 4-6 related items from same collection
```

**Liquid Pattern for Metafields**:
```liquid
<div class="product-details">
  <h1>{{ product.title }}</h1>
  
  {% if product.metafields.custom.fabric_composition %}
    <div class="detail-block">
      <label>Fabric</label>
      <p>{{ product.metafields.custom.fabric_composition }}</p>
    </div>
  {% endif %}
  
  {% if product.metafields.custom.care_instructions %}
    <div class="detail-block">
      <label>Care</label>
      <p>{{ product.metafields.custom.care_instructions }}</p>
    </div>
  {% endif %}
  
  {% if product.metafields.custom.fit %}
    <div class="detail-block">
      <label>Fit</label>
      <p>{{ product.metafields.custom.fit }}</p>
    </div>
  {% endif %}
</div>
```

### 3. Collection Page (collection.liquid)

**Structure**:
```
1. Collection Hero
   - Collection image
   - Collection title
   - Description

2. Filters (Sidebar)
   - Price range slider
   - Size filter
   - Color filter
   - Availability (in stock)
   - Material (cotton, linen, etc.)

3. Sorting
   - Newest first
   - Price: Low to High
   - Price: High to Low
   - Best Selling
   - Alphabetical

4. Product Grid
   - 3-4 columns (responsive)
   - Lazy loading images
   - Each card:
     - Product image (hover effect: second image)
     - Product title
     - Price + sale strikethrough
     - In-stock indicator
     - Hover: Quick-add button
```

**Liquid Pattern**:
```liquid
<div class="collection-header">
  <h1>{{ collection.title }}</h1>
  <p>{{ collection.description }}</p>
</div>

<div class="collection-layout">
  <aside class="filters">
    <!-- Faceted filtering -->
    {% for filter in collection.filters %}
      <div class="filter-group">
        <h3>{{ filter.label }}</h3>
        {% for value in filter.values %}
          <label>
            <input type="checkbox" value="{{ value.value }}">
            {{ value.label }} ({{ value.count }})
          </label>
        {% endfor %}
      </div>
    {% endfor %}
  </aside>

  <main class="products">
    {% for product in collection.products %}
      {% include 'product-card' %}
    {% endfor %}
  </main>
</div>
```

### 4. Product Card Snippet (snippets/product-card.liquid)

```liquid
<div class="product-card">
  <div class="product-image">
    <img src="{{ product.featured_image }}" alt="{{ product.featured_image.alt }}">
    
    {% if product.images.size > 1 %}
      <img class="hover-image" src="{{ product.images[1] }}" alt="">
    {% endif %}
    
    {% if product.compare_at_price %}
      <div class="sale-badge">Sale</div>
    {% endif %}
  </div>

  <div class="product-info">
    <h3>{{ product.title }}</h3>
    
    <div class="price">
      {% if product.compare_at_price %}
        <span class="compare-at-price">
          {{ product.compare_at_price | money }}
        </span>
      {% endif %}
      <span class="current-price">{{ product.price | money }}</span>
    </div>

    {% if product.metafields.custom.fit %}
      <span class="fit-label">{{ product.metafields.custom.fit }}</span>
    {% endif %}

    <div class="availability">
      {% if product.available %}
        <span class="in-stock">In Stock</span>
      {% else %}
        <span class="out-of-stock">Out of Stock</span>
      {% endif %}
    </div>
  </div>

  <div class="product-actions">
    <button class="btn-add-to-cart" 
            data-product-id="{{ product.id }}">
      Add to Cart
    </button>
  </div>
</div>
```

---

## Implementation Checklist

### Phase 1: Theme Setup
- [ ] Install/duplicate Shopify Dawn theme
- [ ] Configure theme colors in `settings_schema.json`
  - [ ] Primary color (Ember #e05a18)
  - [ ] Secondary color (Gold #f0a030)
  - [ ] Background colors (cream palette)
  - [ ] Text colors (dark brown #140e06)
- [ ] Add custom fonts to `assets/`
  - [ ] Bodoni Moda
  - [ ] Cormorant Garamond
  - [ ] Montserrat
- [ ] Set up TailwindCSS (optional, or use custom CSS)

### Phase 2: Core Templates
- [ ] Edit `templates/index.liquid`
  - [ ] Hero section
  - [ ] Featured collection grid
  - [ ] Brand story section
  - [ ] Trust indicators
  - [ ] Newsletter signup
- [ ] Customize `templates/product.liquid`
  - [ ] Product images gallery
  - [ ] Metafield displays (fabric, care, fit)
  - [ ] Variant selection (size/color)
  - [ ] Related products section
- [ ] Customize `templates/collection.liquid`
  - [ ] Faceted filters
  - [ ] Sort options
  - [ ] Product grid layout

### Phase 3: Snippets & Components
- [ ] Create `snippets/product-card.liquid`
  - [ ] Include metafield badges
  - [ ] Price display with sale state
  - [ ] Availability indicator
- [ ] Create `snippets/price.liquid`
  - [ ] Handle currency formatting
  - [ ] Show compare-at price
- [ ] Create `snippets/form-*.liquid` for inputs

### Phase 4: Navigation & Header
- [ ] Customize `sections/header.liquid`
  - [ ] Logo area (centered or left-aligned)
  - [ ] Main navigation
  - [ ] Search bar
  - [ ] Cart icon
  - [ ] Mobile menu
- [ ] Set up header menu structure
  - [ ] Essentials
  - [ ] Shop (with dropdowns: Tops, Bottoms, Dresses, Accessories)
  - [ ] About
  - [ ] Contact

### Phase 5: Footer
- [ ] Customize `sections/footer.liquid`
  - [ ] Newsletter signup
  - [ ] Footer menu (About, Shipping, Returns, Contact)
  - [ ] Social links
  - [ ] Payment icons
  - [ ] Shipping/SSL badges

### Phase 6: Product Setup
- [ ] Create metafields in Shopify admin
  - [ ] fabric_composition (text)
  - [ ] care_instructions (text)
  - [ ] fit (select: true-to-size, runs-small, runs-large)
  - [ ] made_to_order (boolean)
  - [ ] model_height (text)
  - [ ] material_source (text)
- [ ] Upload 6-8 products as test data
  - [ ] Fill in all metafields
  - [ ] Upload multiple images per product
  - [ ] Set prices and variants

### Phase 7: Styling & CSS
- [ ] Create `assets/theme.css`
  - [ ] Color variables
  - [ ] Typography styles
  - [ ] Component styles (buttons, cards, badges)
  - [ ] Responsive breakpoints (mobile, tablet, desktop)
  - [ ] Hover states and interactions
  - [ ] Sale badges and indicators

### Phase 8: Testing
- [ ] Test on mobile (iOS, Android)
- [ ] Test on desktop (Chrome, Safari, Firefox)
- [ ] Test product pages (all metafields display)
- [ ] Test collection filtering
- [ ] Test add-to-cart flow
- [ ] Verify page speed (Lighthouse 80+)

### Phase 9: Apps & Integrations
- [ ] Install Judge.me (reviews)
- [ ] Install Klaviyo (email)
- [ ] Install Pixelbin (image optimization)
- [ ] Connect Google Analytics 4

### Phase 10: Launch
- [ ] Verify domain (omeclothing.com)
- [ ] Set up SSL (automatic in Shopify)
- [ ] Configure shipping zones & rates
- [ ] Set up payment gateway (Shopify Payments)
- [ ] Create policy pages (Returns, Shipping, Privacy)
- [ ] Test complete checkout flow
- [ ] Launch!

---

## CSS & Styling Patterns

### Colors in Liquid
```liquid
<!-- Use CSS variables for consistency -->
<style>
  :root {
    --color-dark: #140e06;
    --color-ember: #e05a18;
    --color-gold: #f0a030;
    --color-cream: #ede0cc;
    --color-light-cream: #f7f0e6;
    --color-text: #2a1a0c;
    --color-muted: #b8906a;
  }
</style>

<button style="background-color: var(--color-ember);">
  Add to Cart
</button>
```

### Button Styles
```css
/* Primary Button (Ember) */
.btn-primary {
  background-color: #e05a18;
  color: white;
  padding: 12px 28px;
  font-family: 'Montserrat', sans-serif;
  font-weight: 400;
  font-size: 14px;
  letter-spacing: 0.05em;
  border: none;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.btn-primary:hover {
  background-color: #f0a030;
}

/* Secondary Button (Outline) */
.btn-secondary {
  background-color: transparent;
  color: #140e06;
  border: 1px solid #e0d0bc;
  padding: 12px 28px;
  transition: all 0.3s ease;
}

.btn-secondary:hover {
  border-color: #e05a18;
  color: #e05a18;
}
```

### Typography Classes
```css
/* Headings */
h1 {
  font-family: 'Bodoni Moda', serif;
  font-size: 48px;
  font-weight: 400;
  color: #140e06;
  line-height: 1.2;
}

h2 {
  font-family: 'Cormorant Garamond', serif;
  font-size: 32px;
  font-weight: 400;
  color: #140e06;
}

/* Body Text */
body {
  font-family: 'Montserrat', sans-serif;
  font-size: 16px;
  font-weight: 300;
  color: #2a1a0c;
  line-height: 1.6;
}

/* Labels & Metadata */
.label {
  font-size: 8px;
  font-weight: 100;
  letter-spacing: 0.55em;
  text-transform: uppercase;
  color: #b8906a;
}
```

### Grid Layouts
```css
/* Product Grid (Responsive) */
.product-grid {
  display: grid;
  gap: 24px;
  grid-template-columns: repeat(4, 1fr);
}

@media (max-width: 1024px) {
  .product-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 640px) {
  .product-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 16px;
  }
}
```

---

## Important Notes

### Performance Optimization
- Use Shopify's image CDN for all images
- Implement lazy loading on product images
- Minimize CSS/JS file sizes
- Target Lighthouse score: 80+

### Mobile-First Approach
- Design for mobile first, then enhance for desktop
- Touch-friendly buttons (44px minimum height)
- Fast-loading hero images (use WebP with fallbacks)

### Accessibility
- Use semantic HTML (`<button>`, `<nav>`, `<main>`)
- Include alt text on all images
- Ensure color contrast meets WCAG AA (4.5:1)
- Make interactive elements keyboard-accessible

### Brand Voice in Copy
- Keep copy warm, direct, confident, intimate
- Avoid marketing jargon ("curated," "elevated," etc. — show, don't tell)
- Focus on how pieces *feel* and *live*, not trends
- Short sentences; let the product speak

### Customer Experience
- Show product details prominently (fabric, care, fit)
- Make returns/shipping info visible
- Include size guide on product pages
- Show how pieces work together (outfit suggestions)
- Build trust with testimonials and reviews

---

## References & Resources

### Shopify Documentation
- Liquid Syntax: https://shopify.dev/api/liquid
- Theme Development: https://shopify.dev/themes
- Product Metafields: https://shopify.dev/api/admin-rest/2024-01/resources/metafield

### Fonts
- Bodoni Moda: https://fonts.google.com/specimen/Bodoni+Moda
- Cormorant Garamond: https://fonts.google.com/specimen/Cormorant+Garamond
- Montserrat: https://fonts.google.com/specimen/Montserrat

### Tools
- Tailwind CSS: https://tailwindcss.com/
- Shopify Dawn Theme: https://github.com/Shopify/dawn
- Chrome DevTools: Lighthouse for performance auditing

---

**Version 1.0 · Last Updated: March 21, 2026**
**Status**: Ready for Liquid development
