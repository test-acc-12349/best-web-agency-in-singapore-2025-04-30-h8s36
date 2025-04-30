# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your web agency landing page. Follow these steps to make common updates while preserving the design and functionality.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. Locate the header section (near the top of the file):
```html
<div class="text-xl font-bold tracking-tight">
    <a href="/" class="text-white hover:text-blue-400 transition duration-300">
        Web Agency SG <!-- Change company name here -->
    </a>
</div>
```

2. Replace "Web Agency SG" with your company name
3. The existing style classes ensure:
   - `text-xl`: Large text size
   - `font-bold`: Bold weight
   - `hover:text-blue-400`: Blue color on hover

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-400 to-purple-400 bg-clip-text text-transparent">
    Best Web Agency In Singapore <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Grow your business with clicks <!-- Update subheading here -->
</p>
```

Important style classes:
- `text-4xl md:text-5xl lg:text-6xl`: Responsive text sizing
- `bg-gradient-to-r`: Creates gradient effect
- `max-w-3xl`: Controls maximum width

### Features Section
To modify feature cards:

1. Find the features grid:
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-12">
    <div class="bg-gray-900 rounded-xl p-8 shadow-lg hover:shadow-2xl transition duration-300">
        <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
        <p class="text-gray-400">Intuitive interfaces...</p>
    </div>
    <!-- Additional feature cards -->
</div>
```

2. Each card can be customized:
   - Update heading text in `<h3>` tags
   - Modify description in `<p>` tags
   - Keep the existing classes for consistent styling

## Managing Links

### Navigation Menu Links
The navigation menu contains internal page links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal links (same page sections):
   - Use `#section-name` format
   - Ensure the section ID matches (e.g., `id="features"`)
3. For external links:
   - Replace with full URL (e.g., `href="https://example.com"`)

### Call-to-Action Links
Update the main CTA buttons:

```html
<a href="https://fixrr.online" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-semibold px-8 py-4 rounded-lg">
    Get Started Today
</a>
```

Replace `https://fixrr.online` with your desired destination URL.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add new links:

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h4 class="font-semibold mb-4">Quick Links</h4>
        <ul class="space-y-2 text-gray-400">
            <!-- Add these new items -->
            <li><a href="/privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Step 2: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Add your policy content in the main section

## Troubleshooting

Common issues and solutions:

### Broken Links
If links aren't working:
1. Check for typos in `href` attributes
2. Verify file names match exactly
3. Ensure section IDs exist for internal links

### Styling Issues
If styles appear broken:
1. Verify Tailwind CSS is properly loaded:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```
2. Check for missing or mistyped class names
3. Ensure responsive classes use correct breakpoints (`md:`, `lg:`)

### Mobile Menu
If the mobile menu isn't working:
1. Verify Alpine.js is loaded:
```html
<script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
```
2. Check `x-data` and `x-show` directives are present
3. Ensure menu toggle button is properly configured

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).