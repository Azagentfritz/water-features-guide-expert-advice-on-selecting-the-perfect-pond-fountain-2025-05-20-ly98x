# Water Features Guide Landing Page - Maintenance Documentation

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Modifying Text Content

#### Header Section
The site logo and navigation menu are located in the `<header>` section:
```html
<div class="flex-shrink-0">
    <a href="/" class="text-xl font-semibold text-blue-600">WaterFeaturesGuide</a>
</div>
```
To change the logo text, simply replace "WaterFeaturesGuide" with your desired text.

#### Hero Section
The main headline and subheading are in the first `<section>` after `<main>`:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Water Features Guide: Expert Advice on Selecting the Perfect Pond Fountain
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 max-w-3xl mx-auto">
    Transform Your Outdoor Space with the Right Water Feature
</p>
```
Update these text elements while maintaining the existing HTML structure.

### Understanding Tailwind CSS Classes

#### Responsive Design Classes
The page uses responsive prefixes:
- `md:` - applies styles at medium screens (768px and up)
- `lg:` - applies styles at large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: `text-4xl` (2.25rem)
- Tablet: `text-5xl` (3rem)
- Desktop: `text-6xl` (3.75rem)

#### Common Tailwind Classes Used
- Spacing: `px-4`, `py-24`, `mb-6` (padding and margin)
- Colors: `text-blue-600`, `bg-white`, `text-gray-900`
- Flex: `flex`, `items-center`, `justify-between`
- Grid: `grid`, `grid-cols-1`, `md:grid-cols-3`

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update these:
1. Locate the `href` attribute
2. Replace `#section-name` with:
   - Internal sections: Keep `#` prefix (e.g., `#features`)
   - External pages: Use full URL (e.g., `https://example.com/features`)

### Call-to-Action Links
Current CTA links:
```html
<a href="https://pondfountaindepot.com/collections/pond-fountains" 
   class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
    Explore Pond Fountains
</a>
```

To update:
1. Replace the URL in `href`
2. Maintain the existing classes for consistent styling
3. Update button text as needed

## Linking Privacy and Terms Pages

### Footer Links Section
Locate the Legal section in the footer:
```html
<div>
    <h3 class="text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Replace `#` with the correct path:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

2. Ensure privacy.html and terms.html exist in the same directory as index.html

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Verify all section IDs are unique
   - Example: `<section id="features">` matches `href="#features"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify proper use of responsive prefixes (`md:`, `lg:`)
   - Test all breakpoints

3. **Missing Styles**
   - Confirm Tailwind CDN is loading
   - Check for typos in class names
   - Verify class combinations are valid

### Need Help?
- Double-check the Tailwind CSS documentation
- Use browser inspector to identify styling issues
- Ensure all external resources (fonts, CDN) are accessible
- Test all links before deploying changes

Remember to always backup your files before making significant changes, and test thoroughly across different devices and browsers.