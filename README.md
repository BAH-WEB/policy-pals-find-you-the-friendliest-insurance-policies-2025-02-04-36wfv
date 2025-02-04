# PolicyPals Landing Page Maintenance Guide

This guide will help you maintain and customize the PolicyPals landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting Guide](#troubleshooting-guide)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text:**
```html
<!-- Find this line in the header section -->
<span class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">PolicyPals</span>
```
- Replace "PolicyPals" with your desired text
- Keep the classes unchanged to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```
- Edit text between `<a>` tags
- Maintain the `class` attributes for consistent styling

### Hero Section
The main banner section contains:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent">
    Policy Pals Find You The Friendliest Insurance Policies
</h1>
```
- Update the heading text while keeping the classes
- The classes control responsive text sizing (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)

2. **Subheading:**
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
    Discover Your Ideal Policy with PolicyPals.co.uk...
</p>
```
- Modify the text between the `<p>` tags
- Keep the classes for proper spacing and responsive design

### Understanding Key Tailwind Classes

- **Responsive Classes:**
  - `md:` prefix: Applies styles on medium screens and up
  - `lg:` prefix: Applies styles on large screens and up
  
- **Spacing Classes:**
  - `px-4`: Horizontal padding of 1rem
  - `py-4`: Vertical padding of 1rem
  - `mb-8`: Bottom margin of 2rem

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:

```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://www.PolicyPals.Co.Uk">Get Started</a>
```

To update:
1. Internal links (starting with #) connect to section IDs
2. External links need full URLs
3. Steps to modify:
   ```html
   <!-- Example: Updating the Get Started link -->
   <a href="https://www.yournewdomain.com">Get Started</a>
   ```

### Footer Links
Located at the bottom of the page:

```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#faq">FAQ</a></li>
</ul>
```

To update:
1. Ensure internal links match section IDs
2. Update email address:
   ```html
   <p class="text-gray-400">support@policypals.co.uk</p>
   ```

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
Located in the footer:

```html
<!-- Current placeholder links -->
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To update:
1. Replace `#` with actual page paths:
   ```html
   <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
   <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
   ```

2. Ensure privacy.html and terms.html exist in your root directory

## Troubleshooting Guide

### Common Issues:

1. **Broken Internal Links:**
   - Check that section IDs match href attributes
   - Example: `href="#features"` needs matching `id="features"` in section tag

2. **Responsive Design Issues:**
   - Verify Tailwind classes are properly nested
   - Check mobile view using browser dev tools
   - Common classes to check:
     ```html
     text-4xl md:text-5xl lg:text-6xl
     hidden md:flex
     ```

3. **Gradient Text Not Showing:**
   - Ensure all these classes are present:
     ```html
     bg-gradient-to-r from-blue-500 to-teal-400 bg-clip-text text-transparent
     ```

Remember to:
- Test all changes in multiple browsers
- Verify mobile responsiveness
- Keep backup copies before making significant changes
- Maintain consistent styling across all sections

Need help? Contact support@policypals.co.uk for assistance.