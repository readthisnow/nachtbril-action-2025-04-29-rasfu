# Landing Page Maintenance Guide

This guide will help you maintain and customize the Nachtbril Action landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text**: Find this line and replace the text:
```html
<div class="text-2xl font-bold text-blue-600">Nachtbril Action</div>
```

2. **Navigation Menu Items**: Locate these lines to modify menu text:
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Voordelen</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Kenmerken</a>
<a href="#faq" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">FAQ</a>
```

### Hero Section
The main banner section contains:

1. **Main Heading**: Update this section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    Nachtbril Action
    <span class="block text-blue-600 mt-2">Nu 10% Korting!</span>
</h1>
```

2. **Subheading**: Modify this line:
```html
<p class="text-xl text-gray-600 mb-8">Nog maar enkele exemplaren beschikbaar tegen deze speciale prijs!</p>
```

### Tailwind CSS Class Guide
Common classes explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `font-bold`: Bold text
- `mb-6`: Margin bottom spacing
- `text-gray-900`: Dark gray text color
- `hover:text-blue-600`: Blue text on hover

To modify styling:
1. Find the element you want to change
2. Locate its class attribute
3. Add or replace classes following this pattern:
   - Size: `text-sm`, `text-base`, `text-lg`, `text-xl`
   - Colors: `text-[color]-[shade]` (e.g., `text-blue-600`)
   - Spacing: `m-[number]` for margin, `p-[number]` for padding

## Managing Links

### Current Link Structure
The page contains these link types:

1. **Navigation Links**:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Kenmerken</a>
<a href="#faq">FAQ</a>
<a href="https://nachtbril.com/shop">Shop Nu</a>
```

2. **Call-to-Action Links**:
```html
<a href="https://nachtbril.com/shop" class="px-8 py-4 bg-blue-600 text-white rounded-full">
    Profiteer Nu van 10% Korting
</a>
```

### Updating Links
To update any link:

1. Locate the `<a>` tag
2. Modify the `href` attribute:
   - For internal sections: Use `#section-name`
   - For external pages: Use full URL `https://example.com`
   - For local pages: Use relative path `./page.html`

Example:
```html
<!-- Before -->
<a href="https://nachtbril.com/shop">Shop Nu</a>

<!-- After -->
<a href="https://your-new-shop-url.com">Shop Nu</a>
```

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate this section in the footer:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

Update the links:
```html
<ul class="space-y-2">
    <li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

Common issues and solutions:

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file names match exactly
   - Ensure proper path structure (`./` for local files)

2. **Styling Issues**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or conflicting classes
   - Verify responsive classes use correct breakpoints (`sm:`, `md:`, `lg:`)

3. **Layout Problems**
   - Inspect container classes (`container`, `mx-auto`, `px-6`)
   - Check grid system classes (`grid`, `grid-cols-*`)
   - Verify spacing classes are correct

Need help? Contact technical support or consult the [Tailwind CSS documentation](https://tailwindcss.com/docs).