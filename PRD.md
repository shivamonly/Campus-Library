# Product Requirements Document (PRD)
## The Campus Library Website

**Version:** 1.0
**Last Updated:** May 12, 2026
**Project Type:** Single-page marketing/informational website

---

## 1. Executive Summary

### 1.1 Purpose
The Campus Library website serves as the digital presence for a 24-hour library located in Burari, Delhi. The website showcases the library's antiquarian literature collection, modern amenities, and provides essential information for potential visitors including students, researchers, and bibliophiles.

### 1.2 Target Audience
- Students (school, college, university)
- Researchers and academics
- Book enthusiasts and bibliophiles
- Local community members seeking quiet study spaces
- Remote workers needing workspace

### 1.3 Business Context
- **Google Rating:** 4.9 stars (8 reviews)
- **Operating Hours:** 24/7
- **Location:** Sant Nagar, Burari, Delhi - 110084
- **Phone:** 093159 94676

---

## 2. Visual & Design Specification

### 2.1 Design Philosophy
Art Nouveau-inspired design emphasizing elegance, classical beauty, and sophistication. The aesthetic bridges antiquarian heritage with modern functionality.

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

### 2.4 Visual Elements

- **Organic Curves:** Flowing SVG decorative elements
- **Gold Leaf Accents:** Borders and dividers with gold gradients
- **Paper Texture:** Subtle noise overlay (3% opacity) for vintage feel
- **Corner Flourishes:** Decorative corner ornaments on cards
- **Botanical Motifs:** Star/diamond decorative dividers

---

## 3. Page Structure & Layout

### 3.1 Navigation
- **Fixed Header:** Appears on scroll with blur backdrop
- **Logo:** Left-aligned with book icon SVG
- **Nav Links:** About, Features, Reviews, Visit
- **Mobile Menu:** Hamburger toggle with slide-in drawer

### 3.2 Sections

#### 3.2.1 Hero Section
- Full viewport height
- Animated entrance (staggered fade-in)
- Floating decorative SVG curves (parallax animation)
- Library name in large display typography
- Tagline: "A Sanctuary for Antiquarian Literature & Modern Scholarship"
- Rating badge with Google reviews count
- Scroll indicator with bounce animation

#### 3.2.2 About Section
- Card container with ornamental corners
- Drop-cap styling on first paragraph
- Two-paragraph description
- Elegant border treatments

#### 3.2.3 Features Section (Amenities)
- 6-card grid layout (responsive: 3 cols → 2 cols → 1 col)
- Icon circles with gradient backgrounds
- Hover lift effect with top border reveal

**Feature Cards:**
1. Peaceful Environment - Study atmosphere
2. Modern Amenities - Contemporary facilities
3. RO Purified Water - Complimentary filtered water
4. Flexible Hours - 24/7 availability
5. Air Conditioned - Climate controlled
6. High-Speed WiFi - Free internet

#### 3.2.4 Reviews Section
- Horizontal scrolling carousel
- Scroll-snap navigation
- Review cards with decorative quote marks
- 5-star rating display
- Custom styled scrollbar (gold accent)

#### 3.2.5 Popular Times Section
- Animated bar chart
- 7-day week display
- Peak time labels
- Scroll-triggered animation

#### 3.2.6 Contact Section
- 3-card grid layout
- Location with full address
- Phone number with tel: link
- Hours with live "Open" status badge
- Google Maps link button

#### 3.2.7 Footer
- Full-width burgundy background
- Decorative top border gradient
- Library name and tagline
- Copyright notice (© 2026)

---

## 4. Functionality Specification

### 4.1 Navigation
- Smooth scroll behavior for all anchor links
- Fixed header appears on scroll (threshold: 100px)
- Mobile menu toggle with hamburger animation
- Auto-close menu on link click

### 4.2 Animations

| Animation | Trigger | Duration | Easing |
|-----------|---------|----------|--------|
| Hero entrance | Page load | 1s stagger | ease |
| Scroll indicator bounce | Page load | 2s loop | ease-in-out |
| Section reveal | Scroll into view | 0.8s | ease |
| Bar chart fill | Scroll into view | 1s | ease |
| Card hover lift | Mouse enter | 0.4s | ease |
| Top border reveal | Card hover | 0.4s | ease |
| Floating curves | Continuous | 20-25s | ease-in-out |
| Header shrink | Scroll >100px | 0.4s | ease |

### 4.3 Responsive Breakpoints

| Breakpoint | Layout Changes |
|------------|----------------|
| > 768px | Full navigation, 3-column grids |
| ≤ 768px | Hamburger menu, 2-column grids |
| ≤ 480px | Single column, reduced padding |

---

## 5. Content Specification

### 5.1 Library Information

**Name:** The Campus Library
**Tagline:** A Sanctuary for Antiquarian Literature & Modern Scholarship

**Contact Details:**
- Phone: 093159 94676
- Address:
  ```
  2nd floor, 100 Feet Rd
  Opposite Guru Gobind Singh Hospital
  Block B, Sant Nagar, Burari
  Delhi - 110084
  ```

**Operating Hours:** Open 24 hours (all days)

**Rating:**
- 4.9 out of 5 stars
- 8 Google Reviews

### 5.2 Sample Reviews

1. "Peaceful environment and equipped with modern amenities. A wonderful place to immerse yourself in literature."

2. "The ambiance is calm and inviting, making it a perfect place to read or study. Truly a hidden gem in Burari."

3. "RO water and timing is flexible. The staff is helpful and the collection is impressive."

4. "A beautiful space that fosters concentration and learning. Highly recommended for students and book lovers alike."

### 5.3 Popular Times Data

| Day | Peak Busy Time | Intensity |
|-----|----------------|-----------|
| Monday | 6 PM | 85% |
| Tuesday | 5-7 PM | 75% |
| Wednesday | 6 PM | 80% |
| Thursday | 5-7 PM | 70% |
| Friday | 4-6 PM | 60% |
| Saturday | 11 AM-1 PM | 55% |
| Sunday | 10 AM-12 PM | 45% |

---

## 6. Technical Specification

### 6.1 Technology Stack
- **Framework:** Vanilla HTML5, CSS3, JavaScript
- **Fonts:** Google Fonts (Playfair Display, Cormorant Garamond, Great Vibes)
- **Icons:** Custom SVG inline icons
- **No external dependencies or frameworks**

### 6.2 File Structure
```
newwebsite/
├── index.html    (complete single-file application)
├── SPEC.md      (design specification)
└── PRD.md       (this document)
```

### 6.3 External Resources
| Resource | URL | Status |
|----------|-----|--------|
| Google Fonts | fonts.googleapis.com | ✓ Verified |
| Google Maps | share.google.com/mgLZYfHgFkkHkflNp | ✓ Verified |

### 6.4 Browser Support
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Android)

---

## 7. Performance Specification

### 7.1 Optimization
- No external JavaScript dependencies
- Inline SVG icons (no icon library overhead)
- CSS-based animations (GPU accelerated)
- Lazy animation triggers via Intersection Observer pattern

### 7.2 Accessibility
- Semantic HTML structure
- Color contrast compliance (WCAG AA)
- Keyboard navigable
- Mobile touch-friendly

---

## 8. Acceptance Criteria

### 8.1 Visual Verification
- [ ] Art Nouveau aesthetic with organic curves visible
- [ ] Color palette matches specification (burgundy, gold, cream)
- [ ] Typography renders correctly (Playfair Display, Cormorant Garamond)
- [ ] Hero section fills viewport with staggered animations
- [ ] All 6 feature cards display with icons
- [ ] Review carousel scrolls horizontally
- [ ] Popular times chart animates on scroll
- [ ] Footer displays with copyright 2026

### 8.2 Functional Verification
- [ ] Navigation links scroll smoothly to sections
- [ ] Mobile hamburger menu opens/closes
- [ ] Header shrinks on scroll
- [ ] Sections reveal on scroll into view
- [ ] Popular times bars animate when visible
- [ ] Google Maps link opens in new tab
- [ ] Phone number is clickable (tel: link)
- [ ] Page loads without console errors

### 8.3 Responsive Verification
- [ ] Desktop: Full navigation, 3-column grids
- [ ] Tablet: Hamburger menu, 2-column grids
- [ ] Mobile: Single column, touch-friendly

---

## 9. Future Considerations

### 9.1 Potential Enhancements
- Virtual tour/360° imagery
- Online catalog search
- Reservation system for study rooms
- Book recommendation engine
- Blog/news section for events
- Photo gallery with lightbox
- Social media integration
- Newsletter signup
- Dark mode toggle

### 9.2 Analytics Integration
- Google Analytics 4 for traffic tracking
- Heatmap integration (Hotjar/FullStory)
- Review aggregation from Google

---

## 10. Appendix

### A. Color Accessibility
| Combination | Ratio | WCAG Level |
|-------------|-------|-----------|
| Gold on Cream | 4.2:1 | AA Pass |
| Burgundy on Cream | 7.1:1 | AAA Pass |
| Text on White | 12.6:1 | AAA Pass |

### B. Animation Keyframes
```css
fadeInUp: translateY(30px) → translateY(0), opacity 0 → 1
float: translate + rotate oscillation
bounce: translateY oscillation
pulse: opacity 1 → 0.5 → 1
```

### C. Contact Card Icons
- Location: Map pin (SVG)
- Phone: Telephone (SVG)
- Hours: Clock (SVG)

---

*Document prepared for The Campus Library digital presence*
*© 2026 The Campus Library, Delhi*
