# Solar Proposal Website Design Guidelines

## Design Approach
**System-Based Approach: Material Design Enterprise Variant**
This professional solar energy proposal platform requires a clean, data-focused design system that emphasizes clarity, trust, and precision. Material Design principles provide the foundation with enterprise customizations for credibility.

**Key Design Principles:**
- Professional credibility through clean layouts and structured information hierarchy
- Data clarity with well-organized tables, calculators, and specifications
- Trust-building through consistent branding and polished presentation
- Efficiency in form completion and proposal generation

---

## Core Design Elements

### A. Typography
**Font Families:**
- Primary: Inter (headings, UI elements, data tables)
- Secondary: Source Sans Pro (body text, descriptions)
- Monospace: JetBrains Mono (numerical data, calculations)

**Hierarchy:**
- Page Titles: text-4xl font-bold (Inter)
- Section Headers: text-2xl font-semibold (Inter)
- Subsections: text-xl font-medium (Inter)
- Body Text: text-base font-normal (Source Sans Pro)
- Data/Numbers: text-lg font-mono (JetBrains Mono)
- Captions: text-sm font-normal (Source Sans Pro)

### B. Layout System
**Spacing Primitives:** Use Tailwind units of **4, 6, 8, 12, 16** exclusively
- Component padding: p-6 or p-8
- Section spacing: mb-12 or mb-16
- Form field gaps: gap-6
- Card spacing: space-y-8
- Grid gaps: gap-6 or gap-8

**Container Strategy:**
- Global max-width: max-w-7xl mx-auto
- Form containers: max-w-4xl mx-auto
- Data tables: w-full within max-w-6xl
- Two-column layouts: grid grid-cols-1 lg:grid-cols-2 gap-8

**Header Layout (Every Page):**
- Fixed header with logo left (h-16 object-contain)
- Company details right-aligned (address, website, phone, email in text-sm)
- Sticky positioning for proposal navigation

---

## C. Component Library

### Core UI Elements

**Cards:**
- Professional card containers with subtle elevation
- Border: border border-gray-200
- Padding: p-8
- Rounded: rounded-lg
- Shadow: shadow-sm hover:shadow-md transition

**Data Tables:**
- Full-width responsive tables with alternating row backgrounds
- Header row: bg-gray-50 font-semibold text-left
- Cell padding: px-6 py-4
- Border: border-b border-gray-200
- Numerical columns: text-right font-mono

**Form Inputs:**
- Input fields: border border-gray-300 rounded-lg px-4 py-3 text-base
- Focus state: focus:ring-2 focus:ring-blue-500 focus:border-blue-500
- Labels: block text-sm font-medium mb-2
- Helper text: text-xs text-gray-500 mt-1
- Required indicators: Red asterisk after label

**Buttons:**
- Primary CTA: bg-blue-600 text-white px-8 py-3 rounded-lg font-semibold
- Secondary: border-2 border-blue-600 text-blue-600 px-8 py-3 rounded-lg font-semibold
- Navigation: bg-gray-100 text-gray-700 px-6 py-2 rounded-md
- Icon buttons: p-2 rounded-full hover:bg-gray-100

### Navigation

**Multi-Step Form Progress:**
- Horizontal stepper showing: Input → Assessment → Specifications → Pricing → ROI → Summary
- Active step: bg-blue-600 text-white
- Completed: bg-green-500 text-white with checkmark
- Upcoming: bg-gray-200 text-gray-500
- Connector lines between steps

**Proposal Page Navigation:**
- Sidebar navigation (desktop) or hamburger menu (mobile)
- Active page highlighted with left border accent
- Page numbers with titles

### Forms

**Multi-Step Input Form:**
- Grouped field sections with clear headings
- Grid layout: grid grid-cols-1 md:grid-cols-2 gap-6
- Validation feedback: Red border + error message below field
- Success state: Green checkmark icon
- Progress save indicators

**Calculator Interfaces:**
- Input section clearly separated from results
- Results displayed in prominent metric cards
- Live calculation updates
- "Calculate" button triggers results display

### Data Displays

**ROI Calculator Table:**
- 25-row table with columns: Year | Units Generated | MSEB Rate | Value Generated | Investment Remaining | Savings | Cumulative
- Sticky header row on scroll
- Highlight breakeven year with subtle background
- Responsive: horizontal scroll on mobile with frozen first column

**Bill of Materials List:**
- Two-column layout: Component details | Specifications/Warranty
- Component name: text-lg font-semibold
- Specifications: text-sm in definition list format
- Warranty badges: inline pill badges with warranty years

**Metric Cards (Dashboard Style):**
- Grid of 2x2 or 3x3 cards showing key metrics
- Large number: text-4xl font-bold font-mono
- Label below: text-sm text-gray-600
- Icon accent in top-right corner

### Overlays

**PDF Generation Modal:**
- Center overlay with backdrop blur
- "Generating Proposal..." with spinner
- Download button appears when ready
- Preview thumbnail option

---

## D. Animations
**Minimal, Purposeful Motion Only:**
- Page transitions: Smooth fade-in (300ms)
- Form validation: Shake animation on error (200ms)
- Calculator results: Slide-down reveal (400ms)
- Success states: Subtle checkmark animation
- NO scroll-triggered animations
- NO decorative motion

---

## Images

**Placement and Usage:**

1. **Company Profile Page (Page 1):**
   - Hero section with professional solar installation image (provided: Baner_3X1P5_12 Low_1761342080049.jpg)
   - Full-width banner, h-96 with gradient overlay
   - Company logo and tagline centered over image with blurred background button containers

2. **Installation Gallery (Pages 8-10):**
   - Masonry grid layout showcasing all 11 provided installation photos
   - Grid: grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6
   - Images: rounded-lg shadow-md hover:shadow-xl transition
   - Lightbox modal on click for full-size viewing

3. **Case Study References:**
   - Before/after style presentation
   - Two-column layout with project details + installation photo
   - Use images: IMG-20240425-WA0028, IMG-20240715-WA0011, IMG-20250115-WA0005

4. **Technical Specifications Page:**
   - Small product images for solar panels, inverters (use placeholder icons if needed)
   - Image thumbnails: w-24 h-24 rounded-md

**Image Treatment:**
- Border radius: rounded-lg for all photos
- Aspect ratio: object-cover to maintain consistency
- Loading: Lazy load images outside viewport

---

## Page-Specific Layouts

**Input Form Pages:** Single-column centered form (max-w-4xl) with clear section divisions

**Calculator/Results Pages:** Split layout - inputs left (40%), results right (60%) on desktop; stacked on mobile

**ROI Analysis Page:** Full-width table + visual chart section below

**Gallery Pages:** Full-width masonry grid with filtering options

**PDF Proposal Output:** Clean, print-optimized layout with company header/footer on each page, single-column A4 format