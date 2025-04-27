# Cash Stuff Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Cash Stuff landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Cash Stuff</a>
```
Replace "Cash Stuff" with your desired text while keeping the surrounding code intact.

2. **Navigation Menu Items:**
```html
<div class="hidden lg:flex items-center space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Voordelen</a>
    <a href="#faq" class="hover:text-purple-400 transition-colors duration-300">FAQ</a>
</div>
```
Change "Features", "Voordelen", and "FAQ" to your preferred menu items.

### Hero Section
The main banner section contains:

1. **Main Heading:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Koop Cash Stuff Met Korting</h1>
```
Update the text between the `<h1>` tags. The classes control:
- `text-5xl/6xl/7xl`: Text size at different screen sizes
- `bg-gradient-to-r`: Creates the gradient effect
- `font-bold`: Makes text bold

2. **Subheading:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12">Mis deze exclusieve deals niet!</p>
```
Modify the text while maintaining the classes for consistent styling.

### Tailwind CSS Classes Explained
Common classes used throughout:
- `container mx-auto`: Centers content and sets max-width
- `px-6`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `grid grid-cols-1 md:grid-cols-2`: Creates responsive grid layouts
- `rounded-2xl`: Adds rounded corners
- `hover:shadow-xl`: Adds shadow on hover

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
<a href="https://amzn.to/3RATnVe">Shop Nu</a>
```

To update:
1. Internal links (starting with #): Update the href to match the ID of the target section
2. External links: Replace the full URL in the href attribute

Example:
```html
<!-- Before -->
<a href="https://amzn.to/3RATnVe">Shop Nu</a>
<!-- After -->
<a href="https://your-new-url.com">Shop Nu</a>
```

### Footer Links
Current placeholder links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files in your project folder:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
```html
<!-- Replace these placeholder links -->
<li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>

<!-- With these working links -->
<li><a href="privacy.html" class="hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these elements from index.html to your new pages:
1. The entire `<head>` section for consistent styling
2. The header and footer sections
3. The same body classes: `class="bg-gray-900 text-gray-100 font-inter antialiased"`

## Troubleshooting

Common Issues and Solutions:

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - IDs are case-sensitive
   - Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
   - Check that you've maintained the responsive classes (md: and lg: prefixes)
   - Test on different screen sizes using browser developer tools
   - Don't remove container classes as they maintain proper spacing

3. **Gradient Text Not Showing**
   - Ensure all these classes are present for gradient text:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)