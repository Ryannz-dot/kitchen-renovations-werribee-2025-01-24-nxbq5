# Kitchen Renovations Landing Page - Maintenance Guide

This guide will help you maintain and customize the Kitchen Renovations landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your brand name and navigation menu. To update:

1. Change the brand name:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-800">KitchenReno</a>
```
Simply replace "KitchenReno" with your desired brand name.

### Hero Section
The hero section is your main banner area. To modify:

1. Update the main heading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-8">
    Expert Kitchen Renovations Werribee
</h1>
```
Replace the text while keeping the classes intact.

2. Modify the subheading:
```html
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Redefining Style and Functionality for Your Dream Kitchen
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-900`, `bg-indigo-600`, etc.
- Spacing: `px-6` (padding left/right), `py-4` (padding top/bottom), `mb-8` (margin bottom)
- Responsive prefixes: `md:` (medium screens), `lg:` (large screens)

## Managing Links

### Navigation Menu Links
The navigation menu contains internal links to page sections:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update these links:
1. The `#` symbol indicates an internal page section
2. Make sure the href matches the `id` of the target section
3. Example: `href="#features"` links to `<section id="features">`

### External Links
To update the main call-to-action button:

```html
<a href="http://kitchenrenovationswerribee.com" class="hidden md:block bg-indigo-600">
```
Replace the URL with your actual website address.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Locate the footer section and add privacy/terms links:

```html
<footer class="bg-gray-900 text-white py-16">
    <div class="container mx-auto px-6">
        <!-- Add this code in the footer grid -->
        <div class="text-gray-400">
            <a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
            <span class="mx-2">|</span>
            <a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
        </div>
    </div>
</footer>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Use the same header and footer as the main page
3. Add your policy content in the main section

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check if section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - If mobile layout breaks, check for proper responsive classes
   - Always test on multiple screen sizes
   - Use browser developer tools to test responsiveness

3. **Styling Problems**
   - Don't remove `font-['Poppins']` from body class
   - Maintain the Tailwind CSS import in the header
   - Keep the viewport meta tag for proper mobile rendering

### Need Help?
- Double-check spelling in class names
- Verify all opening tags have corresponding closing tags
- Use browser developer tools (F12) to inspect elements
- Keep backup copies before making major changes

Remember: Always test your changes across different devices and browsers before publishing updates to your live site.