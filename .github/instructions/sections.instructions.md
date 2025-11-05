---
applyTo: "src/lib/sections/**/*.svelte"
---

# Section Components Instructions

## Section Design Patterns

All section components must follow the Studio.tailwindui.com design pattern with alternating dark/light backgrounds:

### Dark Sections (bg-neutral-950)
- Background: `bg-neutral-950`
- Text: `text-white` for headers, `text-neutral-300` for body text
- Used for: About, Contact, and every other section
- Pattern:
```svelte
<section class="bg-neutral-950 py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <!-- Content -->
  </div>
</section>
```

### Light Sections (bg-white)
- Background: `bg-white`
- Text: `text-neutral-900` for headers, `text-neutral-600` for body text
- Used for: Services, Features, Hero
- Pattern:
```svelte
<section class="bg-white py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <!-- Content -->
  </div>
</section>
```

## RTL Support for Sections

### Critical RTL Classes
- Use `ps-` and `pe-` instead of `pl-` and `pr-`
- Use `start-` and `end-` instead of `left-` and `right-`
- Add `dir="rtl"` to Hebrew text containers
- Use `text-start` instead of `text-left`

### Grid Layouts
All grids should be responsive and RTL-compatible:
```svelte
<div class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
  <!-- Grid items with rounded-4xl styling -->
</div>
```

## Typography Standards

### Headers
- Section titles: `text-3xl font-bold tracking-tight sm:text-4xl`
- Subsection titles: `text-xl font-semibold leading-7`
- Color: `text-white` on dark, `text-neutral-900` on light

### Body Text
- Main text: `text-base leading-7`
- Secondary text: `text-sm leading-6`
- Color: `text-neutral-300` on dark, `text-neutral-600` on light

## Statistics Display

When showing numbers/achievements:
```svelte
<dl class="grid grid-cols-1 gap-8 sm:grid-cols-2 lg:grid-cols-4">
  <div class="flex flex-col-reverse gap-1">
    <dt class="text-base leading-7 text-neutral-300">{description}</dt>
    <dd class="text-4xl font-bold leading-9 tracking-tight text-white">{number}+</dd>
  </div>
</dl>
```

## Content Guidelines

### Hebrew Text Standards
- Keep language professional but approachable
- Focus on educational value and methodology
- Avoid overly promotional language
- Use proper Hebrew grammar and punctuation

### Physics Tutoring Context
- Emphasize personalized learning approach
- Highlight teaching methodology
- Include success stories and statistics
- Focus on student outcomes

## Component Consistency

### Purple Accents (Minimal Use)
- Use sparingly for CTAs and highlights
- Classes: `bg-purple-100`, `text-purple-600`, `border-purple-200`
- Avoid overuse - maintain professional neutral aesthetic

### Rounded Corners
- Consistently use `rounded-4xl` for all cards and containers
- This creates the modern, soft Studio aesthetic

### Spacing Standards
- Section padding: `py-24 sm:py-32`
- Container: `mx-auto max-w-7xl px-6 lg:px-8`
- Grid gaps: `gap-8`
- Card padding: `p-8`