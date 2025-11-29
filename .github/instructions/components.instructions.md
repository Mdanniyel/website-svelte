---
applyTo: 'src/lib/components/**/*.svelte'
---

# UI Components Instructions

## Critical Animation Components

### Hero Recommendations System

The hero section's auto-scrolling recommendations are **the most important visual element** users see first.

#### RecommendationsPanel Component

```svelte
<!-- Container with multiple columns and fade effects -->
<aside class="relative my-2 flex gap-2 overflow-hidden">
	<RecommendationColumn recommendations={recommendations.slice(0)} additionalClasses="" />
	<RecommendationColumn
		recommendations={recommendations.slice(4)}
		additionalClasses="lg:block hidden"
	/>
	<RecommendationColumn
		recommendations={recommendations.slice(2)}
		additionalClasses="xl:block hidden"
	/>

	<!-- Critical fade effects -->
	<div class="pointer-events-none absolute inset-x-0 top-0 h-32 bg-linear-to-b from-white"></div>
	<div class="pointer-events-none absolute inset-x-0 bottom-0 h-32 bg-linear-to-t from-white"></div>
</aside>
```

#### RecommendationColumn Component

```svelte
<!-- Infinite scroll animation -->
<section class="{additionalClasses} min-w-60 grow overflow-hidden">
	<ul class="slide-top space-y-5">
		{#each recommendations as recommendation}
			<li><WaMessage text={recommendation} /></li>
		{/each}
		{#each recommendations as recommendation}
			<li><WaMessage text={recommendation} /></li>
		{/each}
	</ul>
</section>

<style>
	ul.slide-top {
		animation: slide-top 70s linear infinite both;
	}

	@keyframes slide-top {
		100% {
			transform: translateY(-50%);
		}
	}
</style>
```

#### Animation Guidelines

- **Duration**: 70 seconds - DO NOT CHANGE (calibrated for readability)
- **Direction**: translateY(-50%) for upward scroll
- **Content**: Real student testimonials in Hebrew
- **Performance**: Uses CSS transforms for GPU acceleration
- **Responsive**: 1-3 columns based on screen size

#### WaMessage Component

Individual recommendation styled as WhatsApp message:

- Green background mimicking WhatsApp
- Hebrew RTL text direction
- Proper spacing and typography

## Button Components

### Primary Buttons

```svelte
<button
	class="rounded-full bg-purple-600 px-6 py-3 text-sm font-semibold text-white shadow-sm hover:bg-purple-500 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-purple-600"
>
	{buttonText}
</button>
```

### Secondary Buttons

```svelte
<button
	class="rounded-full bg-white px-6 py-3 text-sm font-semibold text-purple-600 shadow-sm ring-1 ring-purple-200 ring-inset hover:bg-purple-50"
>
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
	class="block w-full rounded-md border-0 py-1.5 text-neutral-900 shadow-sm ring-1 ring-neutral-300 ring-inset placeholder:text-neutral-400 focus:ring-2 focus:ring-purple-600 focus:ring-inset sm:text-sm sm:leading-6"
	type="text"
	{placeholder}
/>
```

### Textarea Fields

```svelte
<textarea
	class="block w-full rounded-md border-0 py-1.5 text-neutral-900 shadow-sm ring-1 ring-neutral-300 ring-inset placeholder:text-neutral-400 focus:ring-2 focus:ring-purple-600 focus:ring-inset sm:text-sm sm:leading-6"
	rows="4"
	{placeholder}
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
