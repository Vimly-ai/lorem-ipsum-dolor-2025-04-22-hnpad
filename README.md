# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Logo
</div>
```
- Replace "Logo" with your company name
- Keep the surrounding div and its classes to maintain the gradient effect

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```
- Replace "Features", "Benefits", and "Contact" with your desired menu items
- Keep the `class` attributes to maintain styling and hover effects

### Hero Section
Located at the top of the page, containing your main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Lorem ipsum dolor
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    Lorem ipsum dolor sit amet, consectetur adipiscing elit.
</p>
```
- Replace "Lorem ipsum dolor" with your main headline
- Update the paragraph text below it
- Keep the `class` attributes to maintain responsive text sizing:
  - `text-4xl`: Default size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Feature Cards
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl border border-gray-100 hover:shadow-xl transition duration-300 transform hover:scale-105">
    <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Feature 1</h3>
    <p class="text-gray-600">Lorem ipsum dolor sit amet</p>
</div>
```
- Update "Feature 1" with your feature name
- Replace the lorem ipsum text
- Keep the hover effects (`hover:shadow-xl` and `hover:scale-105`)

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
</div>
```
To update links:
1. Replace `#` with your target URL
2. For internal pages: `href="./features.html"`
3. For external links: `href="https://example.com"`

### Call-to-Action Buttons
```html
<a href="#" class="bg-gradient-to-r from-purple-600 to-pink-600 text-white px-8 py-4 rounded-full">
    Get Started Now
</a>
```
- Update the `href="#"` with your signup or contact page URL
- Example: `href="./signup.html"` or `href="https://app.yourservice.com/signup"`

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer section:
```html
<div>
    <h4 class="font-bold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Update the href attributes:
```html
<li><a href="./privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="./terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Gradient Text**
If the gradient text disappears:
```html
<!-- Make sure these classes are present -->
bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent
```

2. **Responsive Issues**
If elements don't stack properly on mobile:
- Check for `md:` prefixes in classes
- Ensure the viewport meta tag is present:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Button Hover Effects Not Working**
Verify these classes are present:
```html
hover:shadow-xl transform hover:scale-105 transition duration-300
```

### Need Help?
- Double-check class names match exactly (Tailwind is case-sensitive)
- Verify all opening tags have corresponding closing tags
- Ensure proper nesting of elements
- Test on multiple screen sizes using browser developer tools

Remember to always make a backup of your files before making changes, and test your updates across different browsers and devices.