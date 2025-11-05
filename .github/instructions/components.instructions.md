---
applyTo: "src/lib/components/**/*.svelte"
---

# UI Components Instructions

## Component Design Principles

All UI components must follow the established design system based on Studio.tailwindui.com patterns.

## Button Components

### Primary Buttons
```svelte
<button class="rounded-full bg-purple-600 px-6 py-3 text-sm font-semibold text-white shadow-sm hover:bg-purple-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-purple-600">
  {buttonText}
</button>
```

### Secondary Buttons
```svelte
<button class="rounded-full bg-white px-6 py-3 text-sm font-semibold text-purple-600 shadow-sm ring-1 ring-inset ring-purple-200 hover:bg-purple-50">
  {buttonText}
</button>
```

### Ghost Buttons
```svelte
<button class="rounded-full px-6 py-3 text-sm font-semibold text-purple-600 hover:text-purple-500">
  {buttonText}
</button>
```

## Card Components

### Standard Card Pattern
```svelte
<div class="rounded-4xl bg-white p-8 shadow-sm ring-1 ring-neutral-200">
  <!-- Card content -->
</div>
```

### Dark Card Pattern (for dark sections)
```svelte
<div class="rounded-4xl bg-neutral-900 p-8 ring-1 ring-neutral-800">
  <!-- Card content with white text -->
</div>
```

## Icon Components

### Icon Standards
- Use consistent sizing: `h-6 w-6` for standard icons
- Color: `text-neutral-600` on light backgrounds, `text-neutral-300` on dark
- Stroke width: `stroke-2` for outline icons

### WhatsApp Icon Usage
```svelte
<svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24">
  <!-- SVG path -->
</svg>
```

## Form Components

### Input Fields
```svelte
<input 
  class="block w-full rounded-md border-0 py-1.5 text-neutral-900 shadow-sm ring-1 ring-inset ring-neutral-300 placeholder:text-neutral-400 focus:ring-2 focus:ring-inset focus:ring-purple-600 sm:text-sm sm:leading-6"
  type="text"
  placeholder="{placeholder}"
/>
```

### Textarea Fields
```svelte
<textarea 
  class="block w-full rounded-md border-0 py-1.5 text-neutral-900 shadow-sm ring-1 ring-inset ring-neutral-300 placeholder:text-neutral-400 focus:ring-2 focus:ring-inset focus:ring-purple-600 sm:text-sm sm:leading-6"
  rows="4"
  placeholder="{placeholder}"
></textarea>
```

## RTL Support for Components

### Text Direction
- Add `dir="rtl"` to components containing Hebrew text
- Use logical properties for spacing
- Test text alignment in RTL context

### Positioning Classes
- Use `start-` and `end-` instead of `left-` and `right-`
- Use `ps-` and `pe-` instead of `pl-` and `pr-`
- Use `ms-` and `me-` instead of `ml-` and `mr-`

## Contact Components

### WhatsApp Integration
- Use green accent color for WhatsApp: `text-green-600`
- Include proper RTL support for phone numbers
- Format: `"https://wa.me/972{phoneNumber}?text={message}"`

### Phone Integration
- Use `tel:` protocol for phone links
- Format phone numbers for Israeli context
- Include proper RTL directionality

## Component Props Standards

### TypeScript Interfaces
```typescript
interface ComponentProps {
  title: string;
  description?: string;
  variant?: 'default' | 'dark' | 'purple';
  size?: 'sm' | 'md' | 'lg';
}
```

### Default Values
Always provide sensible defaults for optional props:
```typescript
export let variant: 'default' | 'dark' | 'purple' = 'default';
export let size: 'sm' | 'md' | 'lg' = 'md';
```

## Accessibility Standards

### ARIA Labels
- Always include proper `aria-label` for interactive elements
- Use `aria-describedby` for additional context
- Include `role` attributes where appropriate

### Keyboard Navigation
- Ensure all interactive elements are keyboard accessible
- Proper tab order with `tabindex` if needed
- Visible focus states

### Screen Reader Support
- Use semantic HTML elements
- Include proper heading hierarchy
- Add `alt` text for images
- Use `sr-only` class for screen reader only content

## Component Testing

### Props Validation
- Test all prop combinations
- Verify default values work correctly
- Test edge cases and error states

### RTL Testing
- Test component appearance in RTL mode
- Verify text alignment and spacing
- Check icon and button positioning

### Responsive Testing
- Test on mobile, tablet, and desktop
- Verify grid layouts adapt properly
- Check text sizing and readability