# SPEC.md - House of Manish Fashion Website

## 1. Concept & Vision

House of Manish is a trendy online fashion destination celebrating the rich heritage of Indian craftsmanship with a modern twist. Drawing inspiration from Rajasthani art traditions — vibrant colors, intricate patterns, and timeless elegance — the website feels like stepping into a royal boutique infused with cultural pride. The experience blends heritage with contemporary fashion, appealing to those who appreciate art, tradition, and modern style.

## 2. Design Language

### Aesthetic Direction
**Rajasthani Royal meets Contemporary Fashion** — Bold jewel tones, intricate mandala patterns, traditional motifs like elephants and peacocks, warm earthy backgrounds, and gold accents reminiscent of royal Mughal artistry. Think heritage art gallery meets modern Indian fashion.

### Color Palette
- **Primary**: `#8B1538` (Royal Maroon) — Headlines, primary text
- **Secondary**: `#D4A574` (Desert Sand) — Subheadings, borders
- **Accent**: `#F4A020` (Marigold Gold) — CTAs, highlights, hover states
- **Background**: `#FDF5E6` (Old Lace Cream) — Page background
- **Surface**: `#FFF8F0` (Warm White) — Cards, product tiles
- **Text Light**: `#6B5344` (Warm Brown) — Secondary text, descriptions
- **Deep Accent**: `#1E4D2B` (Emerald Green) — Decorative elements
- **Royal Blue**: `#1C3A5F` — Contrast accents

### Typography
- **Headlines**: "Playfair Display", serif — Elegant, royal, fashion-forward
- **Body/UI**: "Poppins", sans-serif — Clean, modern, readable
- **Decorative**: "Tiro Devanagari Hindi" for accent text
- **Fallbacks**: Georgia, system-ui

### Spatial System
- Base unit: 8px
- Section padding: 80px vertical (desktop), 48px (mobile)
- Card gaps: 24px
- Container max-width: 1200px
- Border radius: 4px (subtle, refined)

### Motion Philosophy
CSS-only transitions:
- Hover lifts: `transform: translateY(-4px)` with `box-shadow` enhancement
- Color transitions: 0.3s ease for links and buttons
- Underline animations on navigation links

### Visual Assets
- Icons: Custom inline SVGs for social media (Instagram, Facebook, Twitter/X, Pinterest)
- Product images: Generated gradient backgrounds with fashion-themed colors (no external images needed)
- Decorative elements: Subtle gold accent lines, geometric shapes

## 3. Layout & Structure

### Page Structure

**All Pages:**
- Fixed navigation header with logo and nav links
- Footer with social links, quick links, and newsletter signup

**Homepage (`index.html`):**
1. Hero Banner — Full-width, statement headline, CTA button, decorative pattern
2. Featured Categories — 3-column grid (Women, Men, Accessories)
3. New Arrivals — 4-product showcase grid
4. Brand Promise — Split layout with icon highlights
5. Instagram Feed — Static grid placeholder

**About Page (`about.html`):**
1. Hero section with brand story
2. Our Values — 3-column icon grid
3. Timeline — Brand journey milestones
4. Team section — Founder/leadership cards

**Products Page (`products.html`):**
1. Page header with filter hints (static)
2. Product grid — 3-column, 9 products (6 clothes, 3 accessories)
3. Each product: generated image, name, price, description, "Add to Cart" button

**Contact Page (`contact.html`):**
1. Split layout — Contact form left, info right
2. Form fields: Name, Email, Subject dropdown, Message textarea
3. Contact details: Address, phone, email
4. Map placeholder with styled border

### Responsive Strategy
- Desktop: Full layouts, hover states
- Tablet (≤992px): 2-column grids, adjusted spacing
- Mobile (≤576px): Single column, hamburger menu hidden (CSS-only), stacked layouts

## 4. Features & Interactions

### Navigation
- Logo on left, nav links center/right
- Hover: Gold underline animation slides in from left
- Active page indicated with gold underline
- Mobile: Links stack vertically (CSS-only, no JS toggle)

### Product Cards
- Default: White card, subtle shadow
- Hover: Lifts up, shadow intensifies, "Quick View" overlay appears (CSS only)
- Button: Outlined initially, fills gold on hover

### Contact Form
- Inputs: Bottom border style, label floats up on focus (CSS :focus-within)
- Submit button: Solid gold background on hover
- Validation: HTML5 native (required, email type)

### Footer
- Newsletter input with submit button
- Social icons: Circle icons, gold fill on hover

## 5. Component Inventory

### Navigation Bar
- **Default**: White background, black text, subtle bottom shadow
- **Scrolled**: Same (no JS scroll effect)
- Logo: "LUMIÈRE" in Cormorant Garamond, letter-spaced

### Hero Banner
- Full viewport height (100vh) or substantial (70vh)
- Large headline, subtext, CTA button
- Decorative diagonal stripe or geometric pattern

### Product Card
- **Default**: White, 4px radius, `box-shadow: 0 2px 8px rgba(0,0,0,0.08)`
- **Hover**: `transform: translateY(-4px)`, `box-shadow: 0 8px 24px rgba(0,0,0,0.12)`
- Image area: Generated gradient, 1:1.2 aspect ratio
- Content: Product name (Jost 600), price (gold), description (gray), button

### Button
- **Primary**: Gold background (#c9a87c), white text, 48px height, letter-spaced
- **Secondary**: Transparent, gold border, gold text
- **Hover**: Darken 10%, slight scale (1.02)
- **Disabled**: 50% opacity (for form validation)

### Form Inputs
- **Default**: Bottom border only, transparent background
- **Focus**: Gold bottom border, label color change
- **Error**: Red border (HTML5 validation)

### Footer
- Dark background (#1a1a1a), white/gray text
- Section dividers with gold accent line
- Social icons in circular containers

## 6. Technical Approach

### File Structure
```
/
├── index.html
├── about.html
├── products.html
├── contact.html
├── css/
│   └── styles.css
└── SPEC.md
```

### CSS Architecture
- CSS custom properties for colors, spacing, fonts
- Mobile-first responsive approach
- BEM-lite naming convention
- Flexbox and CSS Grid for layouts
- No CSS preprocessors needed

### Browser Support
- Modern browsers (Chrome, Firefox, Safari, Edge)
- CSS Grid with fallbacks
- No vendor prefixes needed for core features

### Performance
- Inline SVGs for icons (no external requests)
- System fonts with Google Fonts enhancement
- Minimal CSS (single file, ~800-1000 lines)
- No images to load (generated gradients)
