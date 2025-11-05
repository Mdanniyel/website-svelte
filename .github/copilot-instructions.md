# Website Physics Tutoring - Copilot Instructions

## Project Overview
This is a professional physics tutoring website built with SvelteKit, Tailwind CSS, and designed with inspiration from Studio.tailwindui.com. The site caters to Hebrew-speaking physics students and implements RTL (right-to-left) text direction throughout.

## Design System & Philosophy

### Visual Identity
- **Design Inspiration**: Studio.tailwindui.com professional minimalist aesthetic
- **Color Palette**: Primarily neutral colors (neutral-50 to neutral-950) with minimal purple accents
- **Typography**: Inter font family throughout the site
- **Visual Pattern**: Alternating dark/light sections for visual rhythm
- **User Preference**: Clean, professional look without overly promotional language

### Color Usage Guidelines
- **Primary Background**: White (for most sections)
- **Dark Sections**: neutral-950 background with white text
- **Text Colors**: neutral-600 for body text, neutral-900 for headings (on light backgrounds)
- **Accent Color**: Purple (purple-100 backgrounds, purple-600 text/borders) - use sparingly
- **Avoid**: Bright colors, excessive use of color accents

### Layout & Spacing
- **Border Radius**: Consistently use `rounded-4xl` for modern, soft appearance
- **Container**: Use `mx-auto max-w-7xl` for main content containers
- **Padding**: Standard `px-6 lg:px-8` for horizontal spacing
- **Grid Layouts**: Prefer 4-column grids on larger screens with responsive breakpoints

## RTL (Hebrew) Support Requirements

### Text Direction
- All content is in Hebrew and requires RTL support
- Use `dir="rtl"` on appropriate elements
- Use logical properties: `ps-` instead of `pl-`, `pe-` instead of `pr-`
- Use `start-` and `end-` instead of `left-` and `right-` for positioning

### RTL-Specific CSS Classes
- `ps-8` instead of `pl-8` (padding-inline-start)
- `pe-8` instead of `pr-8` (padding-inline-end)
- `start-0` instead of `left-0` (positioning)
- `end-0` instead of `right-0` (positioning)

## Component Architecture

### Section Components (src/lib/sections/)
All major sections follow this pattern:
- Dark sections: `bg-neutral-950 text-white`
- Light sections: `bg-white text-neutral-900`
- Consistent padding: `py-24 sm:py-32`
- Container: `mx-auto max-w-7xl px-6 lg:px-8`

### Key Components
- **About.svelte**: Dark section with statistics, methodology explanation
- **Services.svelte**: White section with service grid and features
- **Hero.svelte**: Landing section with call-to-action and animated recommendations
- **Features.svelte**: Benefits and teaching approach

### Critical Animation System - Hero Recommendations
The hero section features an **auto-scrolling recommendations animation** - this is one of the most important visual elements that users see immediately upon entering the site.

#### Component Architecture:
1. **Hero.svelte**: Main landing section containing RecommendationsPanel
2. **RecommendationsPanel.svelte**: Container for multiple recommendation columns with fade effects
3. **RecommendationColumn.svelte**: Individual column with infinite scroll animation
4. **WaMessage.svelte**: Individual recommendation message component
5. **recommendations.json**: Data source with 27 authentic student testimonials

#### Animation Implementation:
```css
/* Key animation in RecommendationColumn.svelte */
ul.slide-top {
    animation: slide-top 70s linear infinite both;
}

@keyframes slide-top {
    100% {
        transform: translateY(-50%);
    }
}
```

#### Visual Effects:
- **Infinite Scroll**: Recommendations scroll continuously upward
- **Gradient Fade**: Top and bottom fade effects using `bg-linear-to-b from-white`
- **Multiple Columns**: 1-3 columns based on screen size (responsive)
- **Content Duplication**: Each recommendation array is duplicated for seamless loop

#### Critical Notes:
- Animation duration: 70 seconds for smooth, readable scroll
- Content: Real Hebrew testimonials from physics students
- Performance: Uses CSS transforms for smooth GPU acceleration
- **Never modify the animation timing** - it's calibrated for optimal readability

### Statistics Format
When displaying numbers/statistics:
```svelte
<dd class="text-4xl font-bold leading-9 tracking-tight text-white">{number}+</dd>
<dt class="text-base leading-7 text-neutral-300">{description}</dt>
```

## Content Guidelines

### Tone & Language
- Professional but approachable Hebrew
- Focus on teaching methodology and student success
- Avoid overly promotional language
- Emphasize personalized learning approach

### Key Messaging Themes
- Personalized physics tutoring
- Proven teaching methodology
- Student success stories (statistics)
- Flexible learning options

## Technical Standards

### Framework & Tooling
- **Frontend**: SvelteKit with TypeScript
- **Styling**: Tailwind CSS with custom Studio-inspired patterns
- **Build Tool**: Vite
- **Development**: Hot module replacement enabled

### File Structure
```
src/
├── lib/
│   ├── components/          # Reusable UI components
│   ├── sections/           # Page sections (About, Services, etc.)
│   └── index.ts           # Component exports
├── routes/
│   ├── +layout.svelte     # Root layout
│   ├── +layout.ts         # Layout data
│   └── +page.svelte       # Home page
└── app.html               # HTML template
```

### Code Quality Standards
- Use TypeScript for type safety
- Follow Svelte component conventions
- Maintain consistent indentation and formatting
- Use semantic HTML elements
- Implement proper accessibility attributes

## Component Design Patterns

### Card Components
```svelte
<div class="rounded-4xl bg-white p-8 shadow-sm ring-1 ring-neutral-200">
  <!-- Content -->
</div>
```

### Grid Layouts
```svelte
<div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
  <!-- Grid items -->
</div>
```

### Button Styles
- Primary: Purple background with white text
- Secondary: White background with purple border
- Ghost: Transparent with purple text

## Deployment & Build

### Production Considerations
- Static site generation enabled
- Optimized for performance
- Mobile-responsive design
- SEO-friendly structure

### Assets
- Store static assets in `static/` directory
- Optimize images for web delivery
- Use appropriate image formats (WebP when possible)

### Design Reference Materials
The `inspire-templates/` directory contains the original Studio.tailwindui.com inspiration materials:
- **HTML Templates**: `about.html`, `main.html`, `our-work.html`, `blog.html` - Original Studio component code
- **Screenshots**: `about.png`, `home.png`, `our-work.png`, `studio.tailwindui.com_ (3).png` - Visual references
- **Hebrew Version**: `סטודיו - סטודיו מפתחים עטור פרסים הממוקם בדנמרק (10_29_2025 11：14：10 AM).html` - Hebrew Studio page

**Important**: Always reference these templates when implementing new components to maintain design consistency with the Studio aesthetic.

## Common Modifications

### Adding New Sections
1. **Reference Templates**: Check `inspire-templates/` directory for Studio.tailwindui.com patterns
2. Create new component in `src/lib/sections/`
3. Follow existing dark/light alternating pattern
4. Export from `src/lib/index.ts`
5. Import and use in `+page.svelte`

### Styling New Components
1. **Study Original Code**: Reference HTML templates in `inspire-templates/` for exact Studio patterns
2. Use existing neutral color palette
3. Follow Studio.tailwindui.com design patterns exactly
4. Implement RTL support from start
5. **Visual Verification**: Compare with screenshot references in `inspire-templates/`
6. Test on mobile and desktop viewports

## User Feedback Integration
Based on user preferences learned during development:
- Prefer minimal color usage (black/white/gray with small purple accents)
- Avoid overly wide cards (use max-w-md for compact layouts)
- Keep promotional language subtle and professional
- Maintain consistent spacing and typography throughout

## Maintenance Notes
- Test RTL layout changes carefully
- Verify color contrast for accessibility
- Keep design system consistent across all sections
- Regular review of mobile responsiveness