# TechGadgets Landing Page - Maintenance Guide

This guide will help you maintain and customize the TechGadgets landing page. Whether you're new to HTML and CSS or just getting started, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">TechGadgets</a>
```
Simply replace "TechGadgets" with your desired name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="mailto:global.suprise@gmail.com">Contact</a>
</div>
```
Replace the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Affiliate Marketing
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Your gateway for techs and gadgets
</p>
```
- To change heading size: modify `text-4xl`, `text-5xl`, or `text-6xl`
- To adjust spacing: modify `mb-6` (margin-bottom) values

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (xs, sm, base, lg, xl, 2xl, etc.)
- `mb-{size}`: Margin bottom (1, 2, 4, 6, 8, etc.)
- `py-{size}`: Padding top and bottom
- `px-{size}`: Padding left and right
- `bg-{color}-{shade}`: Background color (blue-600, gray-900, etc.)

## Fixing Broken Links

### Main Navigation Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="mailto:global.suprise@gmail.com">Contact</a>
<a href="https://bestbargainsmart.com">Get Started</a>
```

To update:
1. Internal links (starting with #) point to sections on the same page
2. Email links should start with "mailto:"
3. External links need full URLs starting with "https://"

### Call-to-Action Buttons
Located in multiple sections:
```html
<a href="https://bestbargainsmart.com" class="inline-block bg-blue-600...">
    Explore Now
</a>
```
Replace the href value with your desired destination URL.

## Linking Privacy and Terms Pages

### Footer Links Section
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your project folder
2. Update the links like this:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Layout:**
   - Check that you haven't removed any essential Tailwind classes
   - Verify all opening tags have matching closing tags
   - Ensure proper nesting of div elements

2. **Links Not Working:**
   - Confirm file paths are correct
   - Check for typos in URLs
   - Verify files exist in the specified locations

3. **Responsive Design Issues:**
   - Keep the `md:` and `lg:` prefixed classes for proper mobile responsiveness
   - Don't remove the `container` classes from parent elements
   - Maintain the viewport meta tag in the header

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct locations
3. Ensure all changes maintain the existing structure
4. Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class details

Remember to always backup your files before making changes, and test on multiple devices and browsers after updates.