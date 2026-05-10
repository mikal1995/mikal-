# Mikal Narration — ITD 210 Capstone Website

> **Live Site:** [Replace with your Netlify or GitHub Pages URL]  
> **GitHub Repo:** [Replace with your GitHub repository URL]

---

## Project Description

Mikal Narration is a fully interactive, five-page multimedia capstone website built for ITD 210 — Advanced Multimedia Development at Northern Virginia Community College. The site demonstrates digital storytelling through immersive web design, interactive 3D graphics, video, and accessible front-end development.

The design language uses a deep-space dark aesthetic with an electric blue accent system, editorial display typography (Syne), and purposeful motion to create an experience that feels alive — not just a collection of static pages.

---

## Live URL

🔗 [yourname-capstone.netlify.app](https://yourname-capstone.netlify.app)

---

## Pages

| Page | File | Description |
|------|------|-------------|
| Home | `index.html` | Hero with animated rings, 3D icosahedron viewer, page card grid |
| About | `about.html` | Bio, animated skill bars, project timeline, FAQ accordion |
| Gallery | `gallery.html` | Filterable image grid with lightbox modal |
| Media | `media.html` | YouTube embed, tabbed sections, 3D torus knot viewer |
| Contact | `contact.html` | Accessible form with validation, mood selector, success state |

---

## Technologies Used

- **HTML5** — Semantic landmarks, ARIA roles and attributes
- **CSS3** — Custom properties, CSS Grid, Flexbox, animations, `clamp()`, logical properties
- **JavaScript** — Vanilla JS, IntersectionObserver, Constraint Validation API, event delegation
- **Three.js r128** — Interactive 3D scenes (IcosahedronGeometry, TorusKnotGeometry)
- **Google Fonts** — Syne (display), DM Sans (body)
- **Netlify / GitHub Pages** — Static site deployment

---

## Features

### Site-wide
- ☀️ **Dark/Light mode toggle** — persists via localStorage across all pages
- 📊 **Scroll progress bar** — thin accent line grows as you scroll
- ⬆️ **Back-to-top button** — appears after 300px scroll, smooth scroll on click
- 📱 **Responsive design** — tested at 375px, 768px, and 1280px
- ⌨️ **Keyboard-navigable** — full Tab/Enter navigation, skip-to-content links
- 🎭 **Scroll-triggered animations** — IntersectionObserver reveal system

### Per Page
- **Home:** Three.js icosahedron with drag-rotation, keyboard control, and particle orbit
- **About:** Animated skill bars, vertical timeline, FAQ accordion
- **Gallery:** Category filter tabs, CSS hover overlays, lightbox with keyboard navigation (ESC/arrows)
- **Media:** YouTube embed, keyboard-navigable tab panels, Three.js torus knot
- **Contact:** Live validation, character counter, mood selector, accessible success state

### Accessibility
- WCAG 2.1 AA color contrast on all text
- Visible focus rings on all interactive elements
- `aria-expanded`, `aria-controls`, `aria-hidden`, `aria-live`, `aria-required` throughout
- `prefers-reduced-motion` media query suppresses all animations
- Alt text / `aria-label` on all images and canvases

---

## File Structure

```
mikal-narration/
├── index.html          # Homepage
├── about.html          # About page
├── gallery.html        # Gallery page
├── media.html          # Media page
├── contact.html        # Contact page
├── css/
│   ├── style.css       # Shared design system (tokens, reset, utilities, header, footer)
│   └── index.css       # Homepage-specific styles
├── js/
│   └── main.js         # Shared JS (nav, scroll progress, dark mode, reveal, back-to-top)
└── README.md
```

---

## Final Reflection

### Strongest Part
The design system — the CSS custom property architecture in `style.css` — is the strongest part of the final site. Every color, spacing value, and transition speed is centralized in `:root` variables, which made the light/dark mode toggle trivial to implement and kept all five pages visually consistent without duplication.

### What I Learned About Responsive Design
The biggest lesson was mobile-first thinking. Starting base styles for the smallest screen and then adding `@media (min-width: ...)` overrides is far more efficient than starting desktop-first and hacking it down. Using `clamp()` for fluid typography removed almost all breakpoint-specific font size overrides.

### Most Impactful Feedback
The feedback about accessibility being non-negotiable changed my approach most. Early versions had decorative elements that weren't aria-hidden, missing labels on inputs, and no skip link. Learning to think "what does a screen reader experience?" at every step made the code better even for sighted users — clearer structure, more meaningful HTML, better focus management.

### What I'd Add With More Time
1. A scroll-driven narrative page where story text syncs with Three.js scene transitions
2. Real form backend (Netlify Forms or Formspree) for actual message delivery
3. A site-search feature and page transitions with the View Transitions API
4. More Three.js scenes — a point cloud that reacts to scroll position

---

## Asset Credits

| Asset | Source | License |
|-------|--------|---------|
| Syne font | Google Fonts (Sven Fuchs et al.) | Open Font License |
| DM Sans font | Google Fonts (Colophon Foundry) | Open Font License |
| Three.js r128 | [threejs.org](https://threejs.org) | MIT License |
| All SVG artwork | Created originally for this project | Original work |
| YouTube embed | Public YouTube player embed API | YouTube Terms of Service |
| AI assistance | Claude (Anthropic) — Three.js scene setup, tab ARIA patterns, CSS scaffolding. All code read, understood, and documented by Mikal Siele. | N/A |

---

## Code Attribution

Claude (Anthropic) was used as an AI coding assistant for:
- Three.js scene initialization and geometry setup
- IntersectionObserver reveal pattern
- Tab panel ARIA pattern
- CSS layout scaffolding

All AI-generated code was reviewed, understood, tested, and commented by Mikal Siele in the student's own words. No code was submitted without comprehension.

---

*ITD 210 — Advanced Multimedia Development | Northern Virginia Community College | Spring 2025*  
*Instructor: Dr. Juls Gilliam*
