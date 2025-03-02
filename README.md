# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Logo
</div>
```
Replace "Logo" with your company name. The gradient effect will automatically apply.

2. **Navigation Links**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
Change the text between `<a>` tags to update menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold tracking-tight text-gray-900 mb-8">
    Lorem ipsum dolor
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Lorem ipsum dolor
</p>
```
- Replace "Lorem ipsum dolor" with your headline
- Update the paragraph text below
- The `md:` and `lg:` prefixes control text size on different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-6">
        <i class="fas fa-star text-purple-600"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Lorem ipsum</h3>
    <p class="text-gray-600">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
</div>
```
To update:
1. Change the icon by replacing `fa-star` with any [Font Awesome](https://fontawesome.com/icons) icon class
2. Update the heading and paragraph text
3. Maintain the existing classes for consistent styling

## Fixing Broken Links

### Current Link Structure
The page contains these types of links:
1. Navigation menu links (Features, Benefits, Contact)
2. Call-to-action buttons ("Get Started")
3. Footer links

### Updating Navigation Links
```html
<!-- Before -->
<a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>

<!-- After -->
<a href="/features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
Replace `#` with your actual URL paths:
- Internal pages: Use relative paths (e.g., `/features`)
- External links: Use full URLs (e.g., `https://example.com`)

### Call-to-Action Buttons
```html
<!-- Find these buttons -->
<a href="#" class="inline-flex items-center px-8 py-4 text-lg font-semibold text-white bg-gradient-to-r from-purple-600 to-blue-500 rounded-full shadow-lg hover:shadow-xl transform hover:scale-105 transition-all duration-300">
```
Replace `#` with your target URL (e.g., `/signup` or `/contact`)

## Linking Privacy and Terms Pages

### Adding Footer Links
Locate the footer section and add new links:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <div>
        <h3 class="text-xl font-bold mb-6">Legal</h3>
        <ul class="space-y-4">
            <!-- Add these new items -->
            <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Alternative Navigation Placement
To add links in the main navigation:
```html
<div class="hidden md:flex space-x-8">
    <!-- Existing links -->
    <a href="/privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy</a>
    <a href="/terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms</a>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Layouts**
- Check that you haven't removed any essential Tailwind classes
- Verify all `div` tags are properly closed
- Maintain the responsive prefixes (`md:`, `lg:`)

2. **Missing Icons**
- Ensure the Font Awesome CDN link remains in the `<head>`
- Verify icon class names match exactly

3. **Link Issues**
- Test all links after updating
- Use relative paths (`/page.html`) for internal links
- Include `https://` for external links

### Need Help?
- Double-check class names against [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML using [W3C Validator](https://validator.w3.org/)
- Keep original code backed up before making changes

Remember to test your changes across different screen sizes using browser developer tools (F12) to ensure responsive design remains intact.