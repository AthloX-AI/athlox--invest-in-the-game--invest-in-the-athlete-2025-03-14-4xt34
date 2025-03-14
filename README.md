# AthloX Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the AthloX landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
- [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
- [Fixing Broken Links](#fixing-broken-links)
- [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections to Update

#### 1. Header/Navigation
```html
<header class="fixed w-full bg-gray-900/95 backdrop-blur-sm z-50 border-b border-gray-800">
```
- To update the logo text, locate:
```html
<a href="/" class="text-2xl font-bold text-white tracking-tight">AthloX</a>
```
- Simply replace "AthloX" with your desired text
- The `text-2xl` class controls size, `font-bold` controls weight

#### 2. Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-blue-600">
    AthloX: Invest in the Game, Invest in the Athlete
</h1>
```
- Replace the heading text while maintaining the HTML structure
- The responsive text sizes are:
  - Mobile: `text-4xl`
  - Tablet: `md:text-5xl`
  - Desktop: `lg:text-6xl`

#### 3. Features Cards
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-gray-900 hover:bg-gray-800 transition-all duration-300 transform hover:scale-105">
    <h3 class="text-xl font-semibold mb-4">Performance</h3>
    <p class="text-gray-400">Track and analyze athlete performance metrics in real-time</p>
</div>
```
To modify:
1. Locate the feature card you want to change
2. Update the `<h3>` title text
3. Update the `<p>` description text
4. Maintain the existing classes for consistent styling

### Understanding Key Tailwind Classes

- Layout Classes:
  - `container`: Centers content and sets max-width
  - `mx-auto`: Centers horizontally
  - `px-6`: Horizontal padding
  - `py-24`: Vertical padding

- Responsive Classes:
  - `md:`: Applies styles at medium screens (768px+)
  - `lg:`: Applies styles at large screens (1024px+)

- Interactive Classes:
  - `hover:`: Styles applied on mouse hover
  - `transition-all`: Smooth transitions
  - `duration-300`: Transition timing

## Fixing Broken Links

### Navigation Menu Links
Current navigation links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the link you want to change
2. Modify the `href` attribute:
   - For internal sections: Use `#section-id`
   - For external pages: Use full URL
   ```html
   <a href="https://example.com/page">Link Text</a>
   ```

### Call-to-Action Links
Current CTA link:
```html
<a href="https://athlox.kit.com" class="inline-flex items-center px-8 py-4 text-lg font-semibold bg-blue-500 text-white rounded-full hover:bg-blue-600 transition-all duration-300 transform hover:scale-105">
```

To update:
1. Replace `https://athlox.kit.com` with your desired URL
2. Maintain all existing classes for consistent styling

## Linking Privacy and Terms Pages

### Footer Links Section
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout**
   - Check that all opening tags have matching closing tags
   - Verify the `container` class is present on main sections
   - Ensure responsive classes (`md:`, `lg:`) are properly formatted

2. **Links Not Working**
   - For internal links (#features, #benefits), verify the ID exists in the HTML
   - For external links, ensure the URL includes `https://` or `http://`
   - Check for typos in href attributes

3. **Styling Issues**
   - Confirm Tailwind CSS is properly loaded in the head section
   - Check for conflicting classes
   - Verify class names are spelled correctly

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)
- Test your page across different browsers and devices

Remember to always test your changes in multiple browsers and screen sizes before deploying to production.