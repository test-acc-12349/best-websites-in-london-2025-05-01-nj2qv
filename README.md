# WebLondon Landing Page - Maintenance Guide

This guide will help you maintain and customize the WebLondon landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-900">WebLondon</a>
```
Simply replace "WebLondon" with your desired text.

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Best Websites In London
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```

To modify:
- Replace "Best Websites In London" with your headline
- Replace "Custom Websites For Your Business" with your subheading
- Keep the existing classes to maintain responsive design

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, etc. (larger number = bigger text)
- Spacing: `mb-6`, `py-24`, etc. (m=margin, p=padding, numbers are multipliers of 4px)
- Colors: `text-gray-900`, `bg-blue-600` (higher numbers = darker shades)
- Responsive prefixes: `md:`, `lg:` (styles apply at those breakpoints)

Example of modifying a feature card:
```html
<!-- Original -->
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition duration-300">

<!-- To make it blue with white text -->
<div class="bg-blue-600 text-white rounded-xl p-8 shadow-lg hover:shadow-xl transition duration-300">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="font-medium text-gray-600 hover:text-gray-900 transition-colors">Features</a>
    <a href="#benefits" class="font-medium text-gray-600 hover:text-gray-900 transition-colors">Benefits</a>
    <a href="#faq" class="font-medium text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
    <a href="#contact" class="font-medium text-gray-600 hover:text-gray-900 transition-colors">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#features` with your desired link:
   - Use `#section-name` for same-page sections
   - Use `/page-name.html` for other pages
   - Use `https://example.com` for external links

### Call-to-Action Buttons
The template has multiple "Get Started" buttons linking to "https://sigmaseo.io". To update:

```html
<!-- Find all instances like this -->
<a href="https://sigmaseo.io" class="inline-flex items-center...">
```

Replace `https://sigmaseo.io` with your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` placeholders:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Ensure file names match exactly (including case)
   - Verify file locations are correct

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the head section
   - Test on different screen sizes

3. **Style Changes Not Working**
   - Verify Tailwind CDN link is present and working
   - Check for typos in class names
   - Ensure classes aren't being overridden

### Need Help?
- Double-check your changes against the original code
- Use browser developer tools (F12) to inspect elements
- Validate your HTML at [W3C Validator](https://validator.w3.org/)

Remember to always backup your files before making changes!