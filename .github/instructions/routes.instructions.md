---
applyTo: "src/routes/**/*.svelte,src/routes/**/*.ts"
---

# Routes and Layout Instructions

## Page Structure Standards

### Main Page Layout (src/routes/+page.svelte)
The main page should follow this section order and pattern:

1. **Hero Section** (Light background)
2. **About Section** (Dark background - neutral-950)
3. **Services Section** (Light background)
4. **Features Section** (Dark background)
5. **Pricing Section** (Light background)
6. **Contact Section** (Dark background)

### Section Import Pattern
```svelte
<script lang="ts">
  import { Hero, About, Services, Features } from '$lib';
  // Other imports
</script>

<Hero />
<About />
<Services />
<Features />
<!-- Additional sections -->
```

## Layout Components (+layout.svelte)

### Root Layout Standards
- Include proper RTL meta tags
- Load Inter font family
- Set up Tailwind CSS
- Include proper viewport settings

### HTML Structure
```svelte
<html lang="he" dir="rtl">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <!-- Other meta tags -->
</head>
<body class="font-sans">
  <main>
    <slot />
  </main>
</body>
</html>
```

## Inline Sections in Routes

### Pricing Section Pattern
When adding pricing directly in routes (not as separate component):

```svelte
<!-- Pricing Section -->
<section class="bg-white py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <div class="mx-auto max-w-4xl text-center">
      <h2 class="text-3xl font-bold tracking-tight text-neutral-900 sm:text-4xl" dir="rtl">
        {title}
      </h2>
      <p class="mt-6 text-lg leading-8 text-neutral-600" dir="rtl">
        {description}
      </p>
    </div>
    
    <div class="mx-auto mt-16 max-w-md">
      <div class="rounded-4xl bg-white p-8 shadow-sm ring-1 ring-neutral-200">
        <!-- Pricing content -->
      </div>
    </div>
  </div>
</section>
```

### Section Alternating Pattern
Maintain consistent dark/light alternating:
- Hero: Light (bg-white)
- About: Dark (bg-neutral-950)
- Services: Light (bg-white)
- Features: Dark (bg-neutral-950)
- Pricing: Light (bg-white)
- Contact: Dark (bg-neutral-950)

## Data Loading (+layout.ts, +page.ts)

### Type Safety
```typescript
import type { PageData } from './$types';

export const load = async (): Promise<PageData> => {
  return {
    // Data structure
  };
};
```

### SEO Data Structure
```typescript
export const load = async () => {
  return {
    title: 'פיזיקה עם דניאל - חונכות פיזיקה מקצועית',
    description: 'לימוד פיזיקה מקצועי ומותאם אישית עם דניאל',
    keywords: 'פיזיקה, חונכות, בגרות, פיזיקה תיכון',
  };
};
```

## RTL Route Considerations

### Hebrew Content
- All text content should be wrapped with `dir="rtl"`
- Use proper Hebrew typography
- Maintain consistent text alignment

### URL Structure
- Keep URLs in English for better SEO
- Use descriptive paths: `/about`, `/services`, `/contact`
- Implement proper routing for Hebrew content

## Mobile Responsiveness

### Responsive Breakpoints
Follow Tailwind's responsive design:
- `sm:` - 640px and up
- `md:` - 768px and up  
- `lg:` - 1024px and up
- `xl:` - 1280px and up

### Mobile-First Approach
```svelte
<!-- Mobile first, then larger screens -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4">
  <!-- Content -->
</div>
```

## Error Handling

### Error Page Structure
```svelte
<!-- src/routes/+error.svelte -->
<section class="bg-white py-24 sm:py-32">
  <div class="mx-auto max-w-7xl px-6 lg:px-8">
    <div class="text-center">
      <h1 class="text-4xl font-bold text-neutral-900" dir="rtl">
        שגיאה בטעינת הדף
      </h1>
      <p class="mt-4 text-lg text-neutral-600" dir="rtl">
        אנא נסה שוב או פנה אלינו לעזרה
      </p>
    </div>
  </div>
</section>
```

## Performance Optimization

### Code Splitting
- Use dynamic imports for large components
- Implement proper lazy loading
- Optimize bundle size

### Image Optimization
- Use WebP format when possible
- Implement proper alt texts in Hebrew
- Use responsive image sizes

## Physics Tutoring Context

### Content Strategy
- Focus on educational value
- Highlight teaching methodology
- Include student success stories
- Emphasize personalized approach

### Call-to-Action Placement
- WhatsApp contact buttons
- Phone number display
- Contact form integration
- Social proof elements

## Testing Routes

### Route Testing Checklist
- [ ] RTL text displays correctly
- [ ] Section alternating pattern works
- [ ] Mobile responsiveness verified
- [ ] Contact buttons functional
- [ ] SEO meta tags present
- [ ] Performance optimized
- [ ] Accessibility standards met