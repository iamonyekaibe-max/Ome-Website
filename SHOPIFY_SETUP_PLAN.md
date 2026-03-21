# Shopify Store Setup Plan - Ome Clothing

## Phase 1: Foundation & Domain (Week 1)

### 1.1 Shopify Store Creation
- [ ] Create Shopify account (shopify.com)
- [ ] Choose Shopify plan: **Starter** ($29/month) → **Basic** ($39/month) recommended for fashion
- [ ] Set up initial store at: ome-clothing.myshopify.com

### 1.2 Domain Configuration
- [ ] Connect **omeclothing.com** to Shopify
  - Go to **Settings > Domains**
  - Click "Connect existing domain"
  - Update registrar DNS to Shopify nameservers (or use CNAME records)
  - Wait 24-48 hours for propagation
- [ ] Enable SSL/HTTPS (automatic with Shopify)
- [ ] Set primary domain to omeclothing.com
- [ ] Configure www redirection

### 1.3 Store Basics
- [ ] Add store name: "OMÉ Essentials"
- [ ] Set store currency: **USD** (primary)
- [ ] Select timezone: **America/New_York** (or your business timezone)
- [ ] Add store description: "OMÉ Essentials — Effortless elegance for everyday wear. Timeless pieces designed for women who have style without trying."

---

## Phase 2: Theme & Design (Week 2)

### 2.1 Theme Selection (Choose One)

**Option A: Modern Fashion Theme (Recommended for Launch)**
- **Prestige** ($180 one-time) - Luxury fashion focused
- **Narrative** - Storytelling & collections
- **Empire** - Fashion-forward, clean
- **Supply** - Minimalist, high-end

**Option B: Free Theme (Budget Start)**
- **Dawn** - Modern, fast, responsive
- **Brooklyn** - Classic e-commerce

### 2.2 Theme Customization
- [ ] Install chosen theme
- [ ] Customize theme settings:
  - [ ] Add logo (high-res PNG/SVG)
  - [ ] Set brand colors from positioning
  - [ ] Update typography to match brand voice
  - [ ] Configure product image galleries
  - [ ] Set up navigation menu structure
  - [ ] Add custom announcement banner (shipping info, promotions)

### 2.3 Homepage Setup
- [ ] **Hero section**: High-impact fashion imagery
  - Use best product photos from your Product Photos folder
  - Add compelling headline (from brand positioning)
  - CTA button: "Shop New Collection"
  
- [ ] **Featured collections section**
  - 3-4 top categories from your collections
  - Grid layout with images
  
- [ ] **Brand story section**
  - 2-3 sentences about Ome's mission/values
  - "About Ome" link to full about page
  
- [ ] **Trust indicators**
  - Fast Lagos delivery badge
  - Quality guarantee
  - Customer testimonial section
  
- [ ] **Email signup**
  - "Get 10% off your first order"
  - Privacy policy disclaimer

---

## Phase 3: Products & Inventory (Week 3)

### 3.1 Product Setup
- [ ] **Create product categories** (Collections):
  - Dresses
  - Tops
  - Bottoms
  - Accessories
  - New Arrivals
  - Sale
  - *[Add based on your product mix]*

- [ ] **Add products** with:
  - [ ] High-quality photos (min 3-5 per product, use Product Photos)
  - [ ] Detailed descriptions (150-200 words)
  - [ ] Size variants (XS, S, M, L, XL for apparel)
  - [ ] Color options
  - [ ] Pricing in NGN (with USD equivalent shown)
  - [ ] SKU/barcode for inventory
  - [ ] Tags: season, color, material, style

### 3.2 Fashion-Specific Metafields
Add custom fields for fashion products:
- [ ] **Fabric composition**: "100% cotton", "Cotton blend"
- [ ] **Care instructions**: "Machine wash cold"
- [ ] **Fit notes**: "True to size", "Runs small"
- [ ] **Size guide**: Link to size guide
- [ ] **Availability**: "In stock", "Made-to-order"
- [ ] **Material source**: "Nigerian cotton", "Imported"

### 3.3 Inventory Management
- [ ] Set stock quantities per size/color variant
- [ ] Enable low stock alerts
- [ ] Configure backorder settings (if applicable)
- [ ] Set up inventory tracking by location

---

## Phase 4: Payments & Fulfillment (Week 4)

### 4.1 Payment Methods
- [ ] **Shopify Payments** (Primary)
  - Supports card payments: Visa, Mastercard, Amex
  - 2.9% + $0.30 per transaction (US standard)
  
- [ ] **PayPal** (Secondary)
  - App: "PayPal Payments"
  - Supports PayPal customers worldwide
  
- [ ] **Enable Buy Now Pay Later**
  - Klarna (growing US market)
  - Affirm (popular for fashion retail)
  
- [ ] **Apple Pay & Google Pay** (Mobile-first)
  - Native Shopify support
  - Higher conversion on mobile

### 4.2 Shipping Configuration
- [ ] **Set up shipping zones**:
  - Zone 1: Continental US (2-3 business days)
  - Zone 2: Alaska & Hawaii (5-7 business days)
  - Zone 3: International - Canada (5-7 business days) [optional]
  - Zone 4: International - Other countries (7-14 business days) [optional]

- [ ] **Shipping rates**:
  - Standard: $6.95 for orders under $75
  - Free shipping for orders $150+
  - Expedited: $14.95 (1 business day)

- [ ] **Carrier Integration**:
  - Use USPS for lightweight packages (optimal for apparel)
  - UPS for larger orders
  - ShipStation for multi-carrier optimization (Phase 7+)

- [ ] **Fulfillment setup**:
  - [ ] Manual: If you're packing/shipping yourself
  - [ ] ShipStation: Integrate for multi-carrier shipping
  - [ ] Track shipments with carrier APIs

### 4.3 Returns & Exchanges (Critical for Fashion)
- [ ] Implement return policy:
  - 30 days for returns
  - Exchange for different sizes/colors
  - Original condition required
  
- [ ] Install Returnly app for automated returns:
  - Customers request return/exchange
  - Auto-generate prepaid return label
  - Track return status
  - Increase customer confidence

### 4.4 Tax Configuration
- [ ] **Set up sales tax**:
  - Enable Shopify Tax if nexus in multiple states
  - Configure state sales tax rates (varies by state: 0-10%)
  - Set tax exemption settings (some states exempt clothing)
  
- [ ] **Consider**:
  - Which US states do you have nexus in? (location of inventory/warehouse)
  - Are you collecting sales tax or letting Shopify Tax handle it?
  
- [ ] **International orders** (if applicable):
  - VAT/GST may apply for Canada and EU orders

---

## Phase 5: Marketing & Analytics (Week 5)

### 5.1 Analytics Setup
- [ ] **Shopify Analytics Dashboard**
  - Monitor daily revenue, conversion rate
  - Track top products and collections
  - Analyze customer acquisition
  
- [ ] **Google Analytics 4 Integration**
  - Add GA4 property
  - Install via Google Channel app
  - Track: Product views, add-to-cart, purchases
  
- [ ] **Littledata** (Fashion-specific)
  - App: "Littledata for Google Analytics"
  - Track: Size/color conversion rates
  - Segment customers by apparel preferences

### 5.2 Email Marketing
- [ ] **Install Klaviyo** app
  - [ ] Set up customer segments
  - [ ] Create flows:
    - Welcome series (10% discount)
    - Abandoned cart recovery
    - Post-purchase follow-up
    - Re-engagement campaign for inactive customers
    - Seasonal collections announcement
  - [ ] Sync with Shopify customer data

### 5.3 Conversion Optimization
- [ ] **Product page optimization**
  - Multiple high-quality photos
  - Natural model photography where possible
  - Clear size/color selection
  - Social proof: Reviews/ratings (install Judge.me)
  - Trust badges: Secure checkout, money-back guarantee
  
- [ ] **Checkout optimization**
  - Minimize form fields
  - Enable guest checkout
  - Display trust signals
  - Show shipping cost early
  
- [ ] **Speed optimization**
  - Compress product images (use Pixelbin app)
  - Lazy load images
  - Minify CSS/JavaScript
  - Target PageSpeed score: 80+

### 5.4 Customer Reviews
- [ ] Install **Judge.me** or **Yotpo**
  - Post-purchase review request
  - Display reviews on product pages
  - Showcase social proof on homepage
  - Track product ratings

---

## Phase 6: Apps & Integrations (Week 6)

### 6.1 Essential Apps (Free/Freemium)
| App | Purpose | Cost |
|-----|---------|------|
| **Paystack Payment** | Local Nigerian payments | Free |
| **Judge.me Reviews** | Product reviews & ratings | Free plan available |
| **Klaviyo** | Email marketing | Free tier available |
| **Pixelbin** | Image optimization | Free plan available |
| **Google Analytics 4** | Web analytics | Free |

### 6.2 Recommended Paid Apps (Phase 7+)
| App | Purpose | Cost |
|-----|---------|------|
| **ShipStation** | Multi-carrier shipping | $9.99/month |
| **Returnly** | Returns management | Transaction-based |
| **Littledata** | Fashion analytics | $19/month |
| **Gorgias** | Customer support automation | $10/month |

### 6.3 Social Integration
- [ ] Add Instagram feed (Screenlist or Instafeed app)
- [ ] Create "Shop on Instagram" tags
- [ ] Link to Facebook Business Page
- [ ] Add social proof widgets (testimonials)

---

## Phase 7: Pre-Launch Checklist (Week 7)

### Technical Setup
- [ ] [ ] Domain configured and SSL active
- [ ] [ ] Mobile responsiveness tested on phones
- [ ] [ ] All product images optimized and uploaded
- [ ] [ ] Payment methods tested in test mode
- [ ] [ ] Shipping zones configured
- [ ] [ ] Policy pages added (Privacy, Terms, Return)
- [ ] [ ] Contact forms working
- [ ] [ ] Page speed optimized (Lighthouse 80+)

### Content & Branding
- [ ] [ ] Store name, logo, brand colors consistent
- [ ] [ ] About page completed with brand story
- [ ] [ ] Product descriptions written (150+ words each)
- [ ] [ ] Size guides created and linked
- [ ] [ ] Brand voice consistent across copy
- [ ] [ ] Customer testimonials added

### Customer Experience
- [ ] [ ] Customer service email set up
- [ ] [ ] WhatsApp business account created
- [ ] [ ] FAQ page addressing common questions
- [ ] [ ] Help section with shipping/returns info
- [ ] [ ] Refund & returns policy clear

### Marketing Prep
- [ ] [ ] Email list import (if you have existing customers)
- [ ] [ ] Welcome email series created
- [ ] [ ] Social media linked
- [ ] [ ] Google Search Console verified
- [ ] [ ] Instagram shop tags configured
- [ ] [ ] Launch announcement planned

---

## Phase 8: Post-Launch (Ongoing)

### First Month
- [ ] Monitor daily performance metrics
- [ ] Respond to customer inquiries within 12 hours
- [ ] Collect feedback from first customers
- [ ] Optimize top-performing products
- [ ] Adjust shipping times based on real data
- [ ] Run first email campaign

### Monthly Tasks
- [ ] Update collections (new season/arrivals)
- [ ] Monitor top products and slow movers
- [ ] Analyse abandoned carts
- [ ] Optimize product pages with A/B tests
- [ ] Run seasonal promotions
- [ ] Update social media with latest designs

### Quarterly Goals
- [ ] Review overall conversion rate and improve
- [ ] Implement Hydrogen migration plan (if scaling)
- [ ] Expand payment methods if needed
- [ ] Analyze customer feedback and iterate
- [ ] Plan next season collection launch

---

## Technology Stack Summary

**Frontend**
- Shopify Liquid theme (launch phase)
- TailwindCSS for custom styling (if needed)
- Plan migration to Hydrogen+React as you scale

**Backend**
- Shopify GraphQL APIs
- Shopify Webhooks for inventory sync
- Paystack/Flutterwave integrations

**Data & Analytics**
- Shopify Analytics (built-in)
- Google Analytics 4
- Littledata for fashion metrics
- Klaviyo for email intelligence

**Images & Performance**
- Shopify CDN (native)
- Pixelbin for optimization
- WebP format support
- Lazy loading enabled

**Integrations**
- Payment: Shopify Payments + Paystack + Flutterwave
- Shipping: ShipStation (if multi-location)
- Returns: Returnly
- Email: Klaviyo
- Reviews: Judge.me

---

## Budget Estimate

| Category | Cost (Monthly) | Notes |
|----------|-----------------|-------|
| Shopify Plan | $39 | Basic plan recommended for startup |
| Domain | ~$12/year | .com domain registration (paid annually) |
| Theme | $180-280 | One-time purchase (not monthly) |
| Apps | $10-30 | Klaviyo free tier, Pixelbin free tier available |
| Shipping supplies* | Variable | Boxes, packaging, labels (depends on volume) |
| **Total** | **~$50-70/month** | Plus payment processing fees (2.9% per order) |

*Shipping supplies costs not included in monthly estimate — scales with order volume

---

**Next Step**: Fill in your specific brand details in [BRAND_POSITIONING.md](BRAND_POSITIONING.md), then I'll help customize this plan further.
