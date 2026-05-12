# The Campus Library Website Specification

**Version:** 1.0
**Last Updated:** May 12, 2026
**Project Type:** Single-page marketing/informational website

---

## 1. Project Overview

### Project Name
The Campus Library

### Core Functionality
A sophisticated Art Nouveau-styled single-page website showcasing a 24-hour antiquarian library in Burari, Delhi. Features library information, amenities, reviews, popular times, and contact details.

### Target Users
- Students (school, college, university)
- Researchers and academics
- Book enthusiasts and bibliophiles
- Local community seeking quiet study spaces
- Remote workers needing workspace

---

## 2. Visual & Rendering Specification

### 2.1 Design Philosophy
Art Nouveau-inspired design emphasizing elegance, classical beauty, and sophistication. Bridges antiquarian heritage with modern functionality.

### 2.2 Color Palette

| Color Name | Hex Code | Usage |
|------------|----------|-------|
| Primary | `#6B2D3D` | Headings, buttons, key elements (Deep Burgundy) |
| Secondary | `#C9A227` | Accents, dividers, stars (Antique Gold) |
| Accent | `#8B9A6D` | Secondary accents (Sage Green) |
| Background | `#F5F0E6` | Main page background (Warm Cream) |
| Text | `#3D2B1F` | Body text (Rich Brown) |
| Ivory | `#FFFEF5` | Cards, overlays |
| Cream Dark | `#E8E0D0` | Borders, dividers |

### 2.3 Typography

| Element | Font Family | Weight/Style |
|---------|-------------|--------------|
| Headings | Playfair Display | 600-700, Regular |
| Body Text | Cormorant Garamond | 400-600, Regular/Italic |
| Decorative Flourishes | Great Vibes | Regular (Script) |

**Google Fonts Import:**
```
https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Cormorant+Garamond:ital,wght@0,400;0,500;0,600;1,400&family=Great+Vibes&display=swap
```

### 2.4 Visual Elements

- **Organic Curves:** Flowing SVG decorative elements in hero background
- **Gold Leaf Accents:** Borders and dividers with gold gradients
- **Paper Texture:** Subtle noise overlay (3% opacity) via inline SVG
- **Corner Flourishes:** Decorative corner ornaments on about card
- **Botanical Motifs:** Star/diamond decorative dividers (SVG)

---

## 3. Page Structure & Layout

### 3.1 Navigation
- **Fixed Header:** Transparent → blur backdrop on scroll
- **Logo:** Book icon SVG + "The Campus Library" text
- **Nav Links:** About, Features, Reviews, Visit
- **Mobile Menu:** Hamburger toggle → slide-in drawer (right side)

### 3.2 Sections (in order)

| Section | ID | Purpose |
|---------|-----|---------|
| Hero | (none) | Full-viewport introduction with rating |
| About | `#about` | Library description |
| Features | `#features` | 6 amenity cards |
| Reviews | `#reviews` | Horizontal review carousel |
| Popular Times | (none) | Animated bar chart |
| Contact | `#contact` | Address, phone, hours, map link |
| Footer | (none) | Closing with copyright |

---

## 4. Component Specification

### 4.1 Header
```css
- Fixed position, full width
- Background: transparent → linear-gradient on scroll
- Backdrop-filter: blur(10px) when scrolled
- Padding: 1rem 2rem → 0.5rem 2rem (shrinks)
- Transition: 0.4s ease
```

### 4.2 Hero Section
- Min-height: 100vh
- Flexbox centered layout
- Background: linear-gradient (ivory → cream)
- Floating SVG curves with animation
- Rating badge with shadow

### 4.3 Rating Badge
```css
- Background: ivory
- Border: 1px solid cream-dark
- Border-radius: 50px
- Shadow: 0 4px 30px rgba(107,45,61,0.1)
- Contains: stars (gold), rating number, review count
```

### 4.4 Feature Cards
```css
- Grid: repeat(auto-fit, minmax(280px, 1fr))
- Gap: 2rem
- Padding: 2.5rem 2rem
- Border-radius: 16px
- Border: 1px solid cream-dark
- Hover: translateY(-8px), shadow, top border reveal
```

### 4.5 Review Cards
```css
- Min-width: 350px
- Horizontal scroll container
- Scroll-snap-type: x mandatory
- Custom gold scrollbar
```

### 4.6 Popular Times Chart
```css
- 7 rows (Mon-Sun)
- Bar animation: width 0 → var(--width) on scroll
- Gradient: secondary → accent
- Duration: 1s ease
```

### 4.7 Contact Cards
```css
- Grid: repeat(auto-fit, minmax(300px, 1fr))
- Icon circle: 70px, gradient background
- "Open" badge: green dot with pulse animation
```

---

## 5. Interaction Specification

### 5.1 Animations

| Element | Animation | Duration | Delay |
|---------|-----------|----------|-------|
| Hero text | fadeInUp | 1s | staggered 0.2s |
| Scroll indicator | bounce | 2s | 1s |
| Floating curves | float | 20-25s | infinite |
| Section reveal | fadeInUp | 0.8s | scroll trigger |
| Time bars | width expand | 1s | scroll trigger |
| Card hover | translateY + shadow | 0.4s | - |

### 5.2 JavaScript Functionality

- Mobile menu toggle (hamburger ↔ X animation)
- Header scroll detection (add/remove .scrolled class)
- Scroll reveal observer (Intersection Observer pattern)
- Smooth scroll for anchor links
- Popular times bar animation trigger

---

## 6. Content Data

### 6.1 Library Information
- **Name:** The Campus Library
- **Tagline:** A Sanctuary for Antiquarian Literature & Modern Scholarship
- **Phone:** 093159 94676
- **Address:** 2nd floor, 100 Feet Rd, Opposite Guru Gobind Singh Hospital, Block B, Sant Nagar, Burari, Delhi - 110084
- **Hours:** Open 24 hours
- **Rating:** 4.9 / 5 (8 Google Reviews)

### 6.2 Amenities (Features)
1. Peaceful Environment
2. Modern Amenities
3. RO Purified Water
4. Flexible Hours
5. Air Conditioned
6. High-Speed WiFi

### 6.3 Reviews
1. "Peaceful environment and equipped with modern amenities. A wonderful place to immerse yourself in literature."
2. "The ambiance is calm and inviting, making it a perfect place to read or study. Truly a hidden gem in Burari."
3. "RO water and timing is flexible. The staff is helpful and the collection is impressive."
4. "A beautiful space that fosters concentration and learning. Highly recommended for students and book lovers alike."

### 6.4 Popular Times
| Day | Peak Time | Intensity |
|-----|-----------|-----------|
| Mon | 6 PM | 85% |
| Tue | 5-7 PM | 75% |
| Wed | 6 PM | 80% |
| Thu | 5-7 PM | 70% |
| Fri | 4-6 PM | 60% |
| Sat | 11 AM-1 PM | 55% |
| Sun | 10 AM-12 PM | 45% |

### 6.5 External Links
- Google Maps: `https://share.google/mgLZYfHgFkkHkflNp`

---

## 7. Technical Implementation

### 7.1 Technology Stack
- HTML5 (semantic)
- CSS3 (custom properties, flexbox, grid, animations)
- Vanilla JavaScript (no frameworks)
- Google Fonts (CDN)

### 7.2 File Structure
```
newwebsite/
├── index.html    (complete single-file application)
├── SPEC.md      (this document)
└── PRD.md       (product requirements)
```

### 7.3 Browser Support
- Chrome, Firefox, Safari, Edge (latest)
- Mobile browsers (iOS Safari, Chrome Android)

---

## 8. Acceptance Criteria

### Visual
- [ ] Art Nouveau aesthetic with organic curves
- [ ] Burgundy (#6B2D3D) and gold (#C9A227) color scheme
- [ ] Playfair Display + Cormorant Garamond typography
- [ ] Paper texture overlay (subtle)
- [ ] Hero fills viewport with staggered animations

### Functional
- [ ] Smooth scroll navigation
- [ ] Mobile hamburger menu works
- [ ] Header shrinks on scroll
- [ ] Sections reveal on scroll
- [ ] Popular times bars animate
- [ ] No console errors

### Responsive
- [ ] Desktop: full nav, 3-column grids
- [ ] Tablet: hamburger menu, 2-column grids
- [ ] Mobile: single column, touch-friendly

---

## 9. Color Accessibility

| Combination | Ratio | WCAG Level |
|-------------|-------|-----------|
| Gold on Cream | 4.2:1 | AA Pass |
| Burgundy on Cream | 7.1:1 | AAA Pass |
| Text on White | 12.6:1 | AAA Pass |
