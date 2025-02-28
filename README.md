# Landing Page Maintenance Guide

This guide will help you maintain and customize the Innodium landing page. Whether you're new to web development or just getting started, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styles](#updating-text-and-styles)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styles

### Header Section
The header contains your brand name and navigation menu. To update:

1. **Brand Name**: Locate this line and change "Innodium" to your brand name:
```html
<a href="/" class="text-2xl font-bold text-indigo-600">Innodium</a>
```

2. **Navigation Items**: Find the navigation div and modify menu items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
The main banner section contains your primary headline and call-to-action:

1. **Main Headline**: Update this text:
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight">Build Your Website in Minutes, Not Days</h1>
```

2. **Subheadline**: Modify this line:
```html
<p class="text-xl md:text-2xl text-gray-200 mb-12 max-w-3xl mx-auto">Best AI Website Builder, No Code Required</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-{size}`: Adds margin bottom (4, 6, 8, etc.)
- `py-{size}`: Adds padding top and bottom
- `bg-{color}`: Sets background color
- `md:`: Applies styles only on medium screens and larger

Example of modifying text size and color:
```html
<!-- Original -->
<h2 class="text-3xl md:text-4xl font-bold text-gray-900">

<!-- Modified for larger, blue text -->
<h2 class="text-4xl md:text-5xl font-bold text-blue-900">
```

## Managing Links

### Navigation Links
1. Internal section links are prefixed with #:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```

2. External links should include the full URL:
```html
<!-- Replace with your actual URL -->
<a href="https://innodium.com" class="hidden md:inline-block px-6 py-2 bg-indigo-600">Get Started</a>
```

### Footer Links
The footer contains multiple link sections. Update these with your actual URLs:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-6">Product</h4>
    <ul class="space-y-4">
        <!-- Replace # with actual URLs -->
        <li><a href="#" class="hover:text-white transition-colors duration-300">Features</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Pricing</a></li>
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the Legal section in the footer and update the href attributes:

```html
<div>
    <h4 class="text-lg font-semibold text-white mb-6">Legal</h4>
    <ul class="space-y-4">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
When creating privacy.html and terms.html, copy these essential elements from index.html:
- The entire `<head>` section
- Header navigation
- Footer section

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check for typos in href attributes
   - Ensure file names match exactly (case-sensitive)
   - Verify all files are in the correct directory

2. **Responsive Design Issues**
   - Keep the `md:` prefix for medium-screen styles
   - Don't remove container classes
   - Maintain the viewport meta tag in the head section

3. **Style Problems**
   - Don't remove Tailwind CDN link from head section
   - Keep all class names exactly as written
   - When adding new styles, refer to Tailwind documentation

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct location
3. Ensure all HTML tags are properly closed
4. Compare your changes against the original code

Remember to always test your changes across different screen sizes using browser developer tools.