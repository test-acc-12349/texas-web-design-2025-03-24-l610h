# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: Find this line and change "TWD":
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```

2. **Navigation Menu Items**: Located in the `<nav>` section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- Other menu items -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Best Websites In Texas</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `mb-6`: Bottom margin spacing
- `text-gray-900`: Dark gray text color
- `font-bold`: Bold text weight

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or replace Tailwind classes
4. Keep responsive classes (`md:`, `lg:`) to maintain mobile-friendly design

## Managing Links

### Current Link Locations

1. **Navigation Menu Links**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Links**:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```

### Updating Links

1. Internal Links (same page sections):
- Keep the `#` prefix
- Match the `id` of the target section
- Example: `href="#features"` links to `<section id="features">`

2. External Links:
- Replace `https://twd.com` with your actual website URL
- Example:
```html
<a href="https://your-actual-domain.com">Get Started</a>
```

## Adding Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling by copying these classes:
```
text-gray-400 hover:text-white transition-colors duration-300
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section `id` attributes match link `href` values
- Example: `<a href="#features">` should match `<section id="features">`

2. **Responsive Design Issues**
- Keep all responsive classes (`md:`, `lg:`)
- Don't remove `container` classes
- Maintain the viewport meta tag:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Style Changes Not Working**
- Verify Tailwind CDN is loading:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for typos in class names
- Ensure classes aren't being overridden

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.