# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Follow these detailed instructions to make updates while preserving the design and functionality.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<a href="/" class="text-2xl font-bold">hgbhss</a>

<!-- How to update -->
<a href="/" class="text-2xl font-bold">Your Company Name</a>
```

#### Hero Section
Look for these elements to update main headlines and descriptions:
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">hgbhss</h1>
<p class="text-xl md:text-2xl mb-8">htyhjjhr</p>
```

#### Features Section
Each feature card contains:
```html
<h3 class="text-xl font-semibold mb-4">vfdf</h3>
<p class="text-gray-600">Premium quality and innovative design</p>
```

### Tailwind CSS Modifications

#### Understanding Responsive Classes
- `md:` prefix means the style applies on medium screens and larger
- Example: `text-4xl md:text-6xl` means:
  - Mobile: text is extra-large (4xl)
  - Desktop: text is super-large (6xl)

#### Common Class Patterns
1. Button Styling:
```html
class="bg-black text-white px-8 py-3 rounded-full hover:bg-gray-800 transition-colors"
```
- `bg-black`: Black background
- `text-white`: White text
- `px-8`: Horizontal padding
- `py-3`: Vertical padding
- `rounded-full`: Rounded corners
- `hover:bg-gray-800`: Darker background on hover

## Fixing Broken Links

### Navigation Menu Links
Current placeholder links in the header:
```html
<div class="hidden md:flex items-center space-x-8">
    <a href="#" class="text-gray-600 hover:text-black transition-colors">Shop</a>
    <a href="#" class="text-gray-600 hover:text-black transition-colors">About</a>
    <a href="#" class="text-gray-600 hover:text-black transition-colors">Contact</a>
</div>
```

To update:
1. Replace `#` with your actual page URLs
2. Example:
```html
<a href="/shop.html" class="text-gray-600 hover:text-black transition-colors">Shop</a>
```

### Footer Links
Current footer links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Shop</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Blog</a></li>
</ul>
```

To update:
1. Replace `#` with corresponding page URLs
2. Ensure consistency with navigation menu links

### Social Media Links
Update social media links in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors">
        <i class="fab fa-instagram text-2xl"></i>
    </a>
    <!-- Repeat for Twitter and Facebook -->
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Add Links to Footer
Insert new links before the copyright section:
```html
<div class="border-t border-gray-800 mt-12 pt-8 text-center text-gray-400">
    <!-- Add these lines -->
    <div class="mb-4">
        <a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors mr-4">Privacy Policy</a>
        <a href="/terms.html" class="text-gray-400 hover:text-white transition-colors">Terms of Service</a>
    </div>
    <p>&copy; 2024 hgbhss. All rights reserved.</p>
</div>
```

### Step 2: Create Policy Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Maintain consistent styling

## Troubleshooting

### Common Issues

1. **Broken Responsive Design**
   - Check for `md:` prefixes in classes
   - Ensure container classes remain intact
   - Verify the viewport meta tag exists:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

2. **Missing Icons**
   - Confirm Font Awesome link is present:
   ```html
   <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
   ```

3. **Tailwind CSS Not Loading**
   - Verify the Tailwind CDN is properly linked:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

### Need Help?
- Check HTML syntax for missing closing tags
- Verify all links start with `/` for root-relative paths
- Test responsive design using browser developer tools
- Ensure images have proper paths and alt text

Remember to always test changes across different devices and browsers before deploying to production.