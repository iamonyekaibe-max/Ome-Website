# OMÉ Essentials — Shopify Website
## Product Requirements Document

**Version 1.0 · 2026 · Confidential**

> "OMÉ for the everyday."

---

## 1. Document Overview

| Field | Details |
|-------|---------|
| **Product** | OMÉ Essentials — Shopify Ecommerce Website |
| **Brand** | OMÉ Essentials · o-MAY |
| **Platform** | Shopify (custom theme) |
| **Version** | 1.0 |
| **Date** | 2026 |
| **Status** | Draft — Pending Stakeholder Review |
| **Prepared By** | OMÉ Brand Team |

### References
- kaicollective.com
- amracollective.com
- OMÉ Brand Essence Doc v1.0

---

## 1.1 Purpose

This Product Requirements Document defines the full scope, features, user experience, and technical requirements for the OMÉ Essentials Shopify website. It serves as the single source of truth for designers, developers, and stakeholders throughout the build process.

---

## 1.2 Background & Inspiration

Two reference sites were analysed during scoping:

**Kai Collective** (kaicollective.com)
- London-based contemporary women's fashion brand
- Strong campaign-driven drops, loyalty programme (Kai Society)
- Bold hero imagery with clear collection taxonomy
- **Key takeaways**: loyalty/rewards integration, campaign storytelling, confident brand voice

**AMRA Collective** (amracollective.com)
- Visual-first Shopify store with clean navigation
- Strong hero banners and minimal friction to purchase
- **Key takeaways**: hero image impact, simple nav structure, mobile-first layout

**OMÉ positioning**: at the intersection — visual warmth and brand storytelling of Kai Collective, with clean simplicity and ease of AMRA Collective.

---

## 2. Goals & Success Metrics

### 2.1 Business Goals

- Launch a Shopify storefront that reflects OMÉ's brand identity: minimal luxury, effortless elegance, everyday wear
- Drive direct-to-consumer sales for the OMÉ Essentials RTW collection
- Build an owned audience through email capture and loyalty programme groundwork
- Position OMÉ as a premium but accessible women's fashion brand for ages 25–40
- Achieve a conversion rate of 2.5%+ within 90 days of launch

### 2.2 User Goals

- Discover and purchase OMÉ pieces with minimal friction
- Understand the brand story and what OMÉ stands for
- Find pieces that work for her real life — work, lounge, social
- Feel seen by the brand's voice, imagery, and product curation

### 2.3 Success Metrics

| Metric | Target |
|--------|--------|
| Conversion Rate | 2.5%+ within 90 days of launch |
| Average Order Value | $120+ |
| Email Capture Rate | 5%+ of site visitors |
| Bounce Rate | Under 55% on homepage |
| Mobile Traffic | 60%+ (mobile-first build required) |
| Page Load Speed | Under 3s on mobile (Google Core Web Vitals) |
| Return Customer Rate | 20%+ within 6 months |

---

## 3. Target Audience

### 3.1 Primary User Profile

| Attribute | Details |
|-----------|---------|
| **Age** | 25–40 |
| **Gender** | Women |
| **Location** | US-based (primary), with international capability |
| **Mindset** | Stylish, confident, and intentional. Knows what looks good. |
| **Shopping Habits** | Researches before buying. Values quality over quantity. |
| **Device** | Primarily mobile (Instagram, TikTok discovery) then desktop checkout |
| **Pain Points** | Fast fashion fatigue. Hard to find pieces that transition from day to night. Tired of over-branded clothing. |

### 3.2 How She Finds OMÉ

- Instagram / TikTok discovery via campaign content and influencer styling
- Google search: 'elevated basics', 'quiet luxury', 'luxury everyday clothing'
- Word of mouth — the brand is designed to prompt "where is that from?"

---

## 4. Site Architecture & Navigation

### 4.1 Top-Level Navigation

Inspired by Kai Collective's clean nav with clear category taxonomy and AMRA's minimal top bar. Navigation must be mobile-responsive with a hamburger menu on mobile.

- **New In** — Latest arrivals — hero placement, updated each drop
- **Shop** — Full collection with filter/sort — by category, size, price
- **Our Story** — Brand story, mission, and the OMÉ woman
- **Journal** — Editorial content — styling guides, outfit ideas, brand moments

### 4.2 Secondary Navigation / Footer

- Sizing Guide
- Shipping & Returns
- FAQ
- Contact / Support
- Privacy Policy & Terms
- Instagram link
- Email sign-up embedded in footer

### 4.3 Product Categories (Collections)

- Dresses
- Co-ords & Sets
- Tops
- Essentials
- New In
- Knitwear

---

## 5. Page-by-Page Requirements

### 5.1 Homepage

#### Hero Section
- Full-bleed hero image or short video loop (autoplay, muted, loop)
- Lifestyle photography — not product shots
- Overlay tagline: "OMÉ for the everyday."
- Single CTA button: "Shop Now" or "Explore the Collection"
- Inspired by: AMRA's full-bleed header impact + Kai Collective's campaign imagery

#### Category Tiles
- 4–6 category tiles below hero
- Minimal labels, strong imagery
- Categories: Dresses · Tops · Essentials · New In · Co-ords · Knitwear

#### Featured Collection
- 'New In' or current campaign collection
- Horizontal scroll on mobile, grid on desktop
- 4–8 products shown
- Each card: image, product name, price, quick-add to cart

#### Brand Statement
- Full-width text section: "OMÉ made for the everyday."
- Optional: secondary image beside text
- Dark brown or cream background

#### Instagram / UGC Row
- Shoppable Instagram feed or UGC row
- Shows 6–8 lifestyle images
- Inspired by Kai Collective's social proof and community content

#### Email Capture
- Embedded section: "Join the OMÉ Edit" — first name + email
- Light cream background
- Incentive: early access to new drops + 20% off first order

### 5.2 Collection / Shop Page

- **Grid layout**: 2 columns mobile, 3–4 columns desktop
- **Filter sidebar** (desktop) / filter drawer (mobile): Size, Category, Price, Colour
- **Sort options**: Newest · Price Low–High · Price High–Low · Best Sellers
- **Product card**: primary image + hover/tap second image (model on garment)
  - Name, price, size dots
- **Badges**: 'Sold Out' on unavailable products; 'New' on arrivals within 14 days
- **Pagination**: Infinite scroll or 'Load More' — no hard page breaks

### 5.3 Product Detail Page (PDP)

#### Media
- 5–8 images: model shots (multiple angles), flat lay, detail/texture close-up
- Image zoom on desktop
- Swipe gallery on mobile
- Optional: short product video loop (5–10 seconds)

#### Product Information
- Product name, price (and sale price if applicable)
- Colour selector (swatch or image tiles)
- Size selector with size guide link
- 'Add to Bag' CTA — prominent, ember/gold colour
- 'Save to Wishlist' secondary action

#### Description & Details
- Short editorial description (brand voice — warm, direct, intimate)
- Accordion: Materials & Care · Fit & Sizing · Shipping & Returns
- Inspired by Kai Collective's clean PDP layout with collapsible details

#### Social Proof
- Star rating + review count
- Expandable full reviews section
- UGC / "How she wears it" section — customer photos tagged with this product

#### You May Also Like
- 4 recommended products
- Algorithm: same category + same colour family

### 5.4 Our Story Page

- Brand story in OMÉ's voice — the woman, the ethos, the 'why'
- Full-bleed imagery interspersed with text
- Not a wall of copy
- Key messages: Effortless elegance. Made for real life. Quality without compromise.
- Embedded: brand values (Quality · Simplicity · Comfort · Versatility) as visual tiles

### 5.5 Cart & Checkout

- Slide-out cart drawer (not a full page redirect)
- Inspired by Kai Collective's cart UX
- Cart shows: product image, name, size, colour, quantity, subtotal
- Upsell slot in cart: 'Complete the look' or 'You might also need'
- Free shipping threshold bar: "Add $X more for free shipping"
- Checkout: Shopify native checkout
- Accelerated payment options: Shop Pay, Apple Pay, Google Pay
- Post-purchase: order confirmation email with brand voice copy and social follow CTA

---

## 6. Design System

### 6.1 Brand Colours

| Color | Hex | Usage |
|-------|-----|-------|
| Dark Brown | #140e06 | Primary dark background, footer |
| Rust | #7a2800 | Campaign / statement backgrounds |
| Ember | #e05a18 | Primary gradient anchor, CTAs, accents |
| Gold | #f0a030 | Gradient highlight, hover states |
| Cream | #ede0cc | Secondary background, product pages |
| Light Cream | #f7f0e6 | Primary background, default ground |
| Muted Tan | #b8906a | Body text, subheads, secondary labels |

### 6.2 Typography

| Type | Font | Usage |
|------|------|-------|
| **Display / Logo** | Bodoni Moda — Serif | OMÉ wordmark and hero headings only |
| **Body / UI** | Montserrat Weight 100–300 | All body copy, labels, navigation, buttons |
| **Editorial** | Cormorant Garamond Italic | Pull quotes, brand statements, Our Story page |
| **Fallbacks** | Bodoni MT, Didot, Garamond (serif) · Futura, Century Gothic (sans) | System fallbacks |

### 6.3 Design Principles

- **Mobile-first**: all layouts designed for 375px viewport first, scaled up
- **Generous white (cream) space**: OMÉ never feels crowded
- **Imagery leads**: minimal UI chrome. Let the photography do the work
- **Consistent spacing**: 8px base unit. 16 / 24 / 32 / 48 / 64 / 96px scale
- **No harsh black**: use Dark Brown (#140e06) instead throughout
- **CTAs**: ember gradient or dark brown. Never grey. Always legible

---

## 7. Shopify Theme & Technical Requirements

### 7.1 Theme Recommendation

| Aspect | Details |
|--------|---------|
| **Recommended base theme** | Dawn (Shopify free) or Prestige (paid, $350) as a starting point for customisation |
| **Customisation** | Significant — custom sections required for homepage, PDP, brand pages |
| **Developer Needed** | Yes — Shopify Liquid developer for custom sections and theme overrides |

Both Kai Collective and AMRA use heavily customised Shopify themes.

### 7.2 Required Shopify Apps

| Feature | App Recommended |
|---------|-----------------|
| **Reviews** | Judge.me or Okendo — product reviews and UGC |
| **Email Marketing** | Klaviyo — email flows, welcome series, abandoned cart, post-purchase |
| **Loyalty Programme** | Smile.io or LoyaltyLion — points, rewards, early access tiers (inspired by Kai Society) |
| **Wishlist** | Wishlist King or Growaveave |
| **Size Guide** | Kiwi Size Chart — embedded on PDP |
| **Instagram Feed** | Instafeed or Covet.pics — shoppable feed on homepage |
| **Upsell / Cross-sell** | ReConvert or Zipify Pages — post-purchase and cart upsells |
| **SEO** | Plug in SEO or Smart SEO — meta optimisation, sitemap, schema |
| **Analytics** | Google Analytics 4 + Meta Pixel + TikTok Pixel |

### 7.3 Performance Requirements

- Lighthouse score: 85+ mobile, 90+ desktop
- LCP (Largest Contentful Paint): under 2.5s
- **Images**: WebP format, lazy-loaded below the fold. Max 200KB per product image
- **Fonts**: self-hosted or Google Fonts — no render-blocking
- No unnecessary app scripts loading on all pages

---

## 8. Customer Experience — Loyalty & Email

### 8.1 Loyalty Programme: OMÉ Edit

Inspired by Kai Collective's 'Kai Society' loyalty model. OMÉ's loyalty programme is called the **OMÉ Edit** — exclusive access and rewards for repeat customers.

| Element | Details |
|---------|---------|
| **Programme Name** | The OMÉ Edit |
| **Tiers** | Everyday · Elevated · Essential (based on annual spend) |
| **Earn Points** | 1 point per $1 spent, bonus points for reviews, referrals, social shares |
| **Redeem Points** | $5 off per 100 points |
| **Perks** | Early access to new drops · Members-only pieces · Birthday reward |
| **Platform** | Smile.io (recommended) or LoyaltyLion |

### 8.2 Email Flows (Klaviyo)

**Welcome Series** (3 emails)
- Brand introduction
- Best sellers
- OMÉ Edit loyalty signup

**Abandoned Cart** (2 emails)
- Reminder at 1hr
- Final nudge at 24hr with social proof

**Post-Purchase** (3 emails)
- Order confirmation
- Shipping update
- "Complete the look" at 7 days

**Win-Back** (2 emails)
- At 60 days inactive — "We miss you" + 10% off

**New Drop Announcement**
- Campaign email to full list on every collection launch

**Birthday Email**
- Sent on customer birthday month with exclusive offer

---

## 9. Content Requirements

### 9.1 Photography Direction

Photography is the most important brand asset on the site. All imagery must align with OMÉ's aesthetic: clean, feminine, modern, minimal luxury.

**Settings**
- Natural light
- Minimal props
- Real environments — home, cafe, street

**Tone**
- Candid and relaxed, not posed
- She's living her life, not modelling

**Colour Palette on Set**
- Cream, rust, earthy neutrals
- Avoid pure white or stark grey

**Model Diversity**
- Women 25–40, various skin tones
- OMÉ is for every woman who moves with intention

**Mandatory Shots Per Product**
- Front on model
- Back on model
- Detail/texture
- Flat lay

### 9.2 Copywriting Voice

All copy must match the OMÉ brand voice: **warm, direct, confident, intimate**.

**Key Guidelines**
- Short sentences. No fluff. Every word earns its place.
- Speak to "her" not "women" — intimate and personal.
- Never use: "luxurious", "affordable luxury", "premium quality". Show don't tell.

**Product Descriptions**
- 30–60 words
- Lead with feel and moment, not fabric specs
- Example: *"The piece she reaches for on a slow Sunday. Soft enough for the sofa, put-together enough for wherever the day takes her."*

### 9.3 SEO Content Strategy

**Primary Keywords**
- elevated basics
- quiet luxury clothing
- everyday luxury fashion

**Secondary Keywords**
- capsule wardrobe
- minimal fashion
- effortless style
- luxury everyday wear

**Long-tail Keywords**
- elevated casual women's clothing
- quality basics for women
- minimal luxury RTW

**Blog Topics**
- How to build a capsule wardrobe
- Quiet luxury styling guide
- What is elevated basics fashion

**Meta Title Format**
```
Product Name | OMÉ Essentials
```

**Meta Description Format**
```
Short editorial hook + product benefit + brand name. Max 155 chars.
```

---

## 10. Feature Priority Matrix

P0 = Launch blocker. P1 = Launch goal. P2 = Post-launch roadmap.

| Feature | Priority | Effort | Notes |
|---------|----------|--------|-------|
| Homepage with hero + collections | P0 | Medium | Core brand entry point |
| Collection / Shop page with filters | P0 | Medium | Required for product discovery |
| Product Detail Page (PDP) | P0 | High | Core purchase flow |
| Cart drawer + checkout | P0 | Medium | Native Shopify checkout |
| Mobile responsive layout | P0 | Medium | 60%+ traffic is mobile |
| Email capture (Klaviyo) | P0 | Low | Critical for owned audience |
| Welcome email flow | P0 | Low | Klaviyo setup |
| Product reviews (Judge.me) | P1 | Low | Trust and conversion |
| Wishlist | P1 | Low | Retention tool |
| Instagram feed on homepage | P1 | Low | Social proof |
| Our Story page | P1 | Low | Brand trust |
| Journal / Blog | P1 | Medium | SEO long-term |
| Size guide (Kiwi) | P1 | Low | Reduces returns |
| Abandoned cart emails | P1 | Low | Klaviyo flow |
| Loyalty programme (OMÉ Edit) | P2 | Medium | Post-launch — Phase 2 |
| UGC / shoppable photos | P2 | Medium | Phase 2 |
| Gift cards | P2 | Low | Holiday season |
| International shipping + currency | P2 | High | Phase 2 expansion |
| Shop Pay / Buy Now Pay Later | P1 | Low | Increases AOV |

---

## 11. Launch Plan & Timeline

### Phase 0 — Pre-build
**Weeks 1–2**: Finalise brand assets, photography, copy, product list. Shopify account setup. Domain & email config.

### Phase 1 — Design
**Weeks 3–5**: Wireframes → Hi-fi mockups (mobile + desktop) for all core pages. Client sign-off before build.

### Phase 2 — Development
**Weeks 6–10**: Theme build and customisation. App integrations. Klaviyo flows setup.

### Phase 3 — QA & Content
**Weeks 11–12**: Full device + browser QA. Product upload and copy QA. Performance audit.

### Phase 4 — Soft Launch
**Week 12**: Password-off for OMÉ Edit preview list. Gather feedback.

### Phase 5 — Public Launch
**Week 13**: Full launch. Announce via email + social. Paid traffic begins.

---

## 12. Open Questions & Decisions Required

- **Photography**: Has a photographer been booked? Shoot date? Number of products and looks to shoot?
- **Inventory**: How many SKUs at launch? Recommended minimum: 15–25 products across 4–6 categories.
- **Pricing**: Is the price range finalised? This affects PDP layout and payment option decisions (BNPL threshold).
- **Loyalty Programme**: Launch Day 1 or Phase 2? Recommend Phase 2 — add once traffic and customer base established.
- **Domain**: Has omeessentials.com (or similar) been registered?
- **Shopify Plan**: Recommended Shopify Basic ($29/mo) at launch, upgrade to Shopify ($79/mo) when reports needed.
- **Developer**: In-house or agency? Timeline and budget need to be confirmed before Phase 1 begins.
- **Returns Policy**: Define before launch — required for PDP accordion and customer service setup.

---

## 13. Launch Product Catalogue

The following products have been photographed and are confirmed for the launch collection. Each entry includes the product name, category, Shopify description (ready to copy-paste), and photography notes.

### 13.1 The Marble Co-ord Set

| Attribute | Details |
|-----------|---------|
| **Product Name** | The Marble Co-ord |
| **Category** | Co-ords & Sets |
| **Silhouette** | Halter crop top + wide-leg trouser, two-piece set |
| **Print** | Black & white marble-stripe print |
| **SKU Format** | OME-COORD-MARBLE-[SIZE] |
| **Images on File** | 9 images — front standing, back standing, seated lifestyle, sofa lifestyle, shelving backdrop |
| **Suggested Price** | $95 – $125 (set) |

#### Shopify Product Description
The set she reaches for when she wants to look like she planned it — but didn't have to think twice. The Marble Co-ord pairs a structured halter top with wide-leg trousers in a bold black and white marble stripe. Put together enough for brunch. Comfortable enough for the whole day.

#### Size & Fit
- Halter neckline with self-tie detail
- Square neckline with peplum hem
- Wide-leg trousers with elasticated waist and side pockets
- Model wears a size S/M. Fits true to size.
- Sold as a set. Top and trousers included.

#### Photo Direction Notes
- **Hero image**: Image 3 or 4 — full front-on standing shot, green arch backdrop
- **Secondary**: Image 7 — seated on sofa, relaxed energy. Strong lifestyle shot.
- **Detail**: Image 6 — seated looking at phone. Shows the set in motion, pocket detail visible.
- **Back shot**: Image 1 — back view showing halter tie and wide-leg silhouette.

---

### 13.2 The Scallop Maxi

| Attribute | Details |
|-----------|---------|
| **Product Name** | The Scallop Maxi |
| **Category** | Dresses |
| **Silhouette** | Two-piece co-ord — structured black top + full-length flared skirt |
| **Print** | Solid black top with scallop hem detail. Off-white/cream ditsy floral print skirt. |
| **SKU Format** | OME-DRESS-SCALLOP-[SIZE] |
| **Images on File** | 3 images — back standing, full front standing (2 angles), green arch and ladder backdrop |
| **Suggested Price** | $110 – $140 |

#### Shopify Product Description
Clean lines meet playful detail. The Scallop Maxi pairs a fitted black structured top — with a soft scallop hemline — against a sweeping cream floral skirt. It moves beautifully. It photographs beautifully. She'll wear it everywhere.

#### Size & Fit
- Structured black top with one-shoulder bow detail and scallop waist hem
- Full-length flared skirt in cream with small ditsy floral print. Elasticated waist.
- Model wears a size S/M. Fits true to size.
- Sold as a set. Top and skirt included.

#### Photo Direction Notes
- **Hero image**: Image 11 — full front-on, relaxed stance, smiling. Clean full-length view.
- **Secondary**: Image 12 — slight angle, shows skirt movement and scallop hem clearly.
- **Back shot**: Image 10 — back view showing bow tie detail and skirt silhouette.

---

### 13.3 The Circle Dress

| Attribute | Details |
|-----------|---------|
| **Product Name** | The Circle Dress |
| **Category** | Dresses |
| **Silhouette** | Tiered ruffle maxi dress with halter neckline |
| **Print** | Black base with multicolour brushstroke circle print — pink, yellow, green, blue, red, white |
| **SKU Format** | OME-DRESS-CIRCLE-[SIZE] |
| **Images on File** | 4 images — side back, full front standing (2 angles), editorial leaning pose |
| **Suggested Price** | $120 – $155 |

#### Shopify Product Description
For when she walks in and the room notices. The Circle Dress is a full-length tiered ruffle halter in a bold multicolour circle print on black. It has presence. It has movement. It is, without question, the dress people will ask about.

#### Size & Fit
- Halter neckline with self-tie at neck
- Square neckline with fitted bodice
- Four tiered ruffle skirt graduating to full length
- Fully lined
- Model wears a size S. Fits true to size. Size up for a more relaxed bodice fit.

#### Photo Direction Notes
- **Hero image**: Image 14 — front full-length, arm on ladder, relaxed smile. Confident energy.
- **Secondary**: Image 15 — arms crossed, strong and self-assured. Great for editorial use.
- **Side shot**: Image 13 — side profile showing tiered ruffle movement and print detail.
- **Lifestyle**: Image 16 — looking off camera, hand in hair. Natural and candid.

---

## Photography Summary

| Metric | Details |
|--------|---------|
| **Total Images** | 16 images across 3 products |
| **Photographer Style** | Studio lifestyle — green arch backdrop, natural light feel, white sofa, bamboo ladder |
| **Model** | Single model across all 3 products. Consistent styling. |
| **Recommendation** | Add 1–2 detail/texture shots per product (fabric close-up) before site launch. Currently missing for all three products. |
| **File Format** | JPG — confirm resolution is 2000px+ on shortest edge for Shopify upload |

---

**OMÉ Essentials · Shopify PRD · Version 1.0 · 2026**

> "OMÉ for the everyday."
