# Premed Medical Academy Landing Page - Maintenance Guide

This guide will help you maintain and customize the Premed Medical Academy landing page. It's written for beginners with no prior coding experience.

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
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    Premed Academy <!-- Change this text -->
</a>
```

2. **Navigation Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update navigation text here -->
    <a href="#benefits">Benefits</a>
    <a href="#video">Watch Demo</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
Located at the top of the page:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold mb-8 leading-tight">
    Register your high school or group to Premed Medical Academy <!-- Edit this text -->
</h1>
```

2. **Subheading:**
```html
<p class="text-xl md:text-2xl mb-12 text-gray-300 max-w-3xl mx-auto">
    Learn Premed Medical School Subjects from Home <!-- Edit this text -->
</p>
```

### Understanding Tailwind Classes

Key classes explained:
- `text-4xl`: Large text size (mobile)
- `md:text-6xl`: Larger text size on medium screens
- `mb-8`: Bottom margin spacing
- `max-w-3xl`: Maximum width constraint
- `mx-auto`: Center horizontally
- `bg-gray-900`: Dark background color

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Modify existing classes or add new ones
4. Test on different screen sizes

Example:
```html
<!-- Original -->
<div class="bg-gray-900 p-8 rounded-2xl">

<!-- Modified with different colors and padding -->
<div class="bg-blue-900 p-12 rounded-2xl">
```

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#video">Watch Demo</a>
<a href="#faq">FAQ</a>
```

To update:
1. The `#` symbol indicates an internal page section
2. Ensure the href matches the section's ID attribute
3. Example: `href="#features"` links to `<section id="features">`

### External Links
The main call-to-action button:
```html
<a href="https://tentritepremed.agency" class="bg-blue-600 hover:bg-blue-700">
    Register Now
</a>
```

To update external links:
1. Replace the URL in `href=""`
2. Test the link works
3. Consider adding `target="_blank"` for opening in new tab

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

### Creating Policy Pages
Basic structure for privacy.html/terms.html:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Premed Medical Academy</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="bg-gray-900 text-gray-100">
    <!-- Copy header from index.html -->
    
    <main class="container mx-auto px-4 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes exactly
   - Check for typos in IDs and hrefs
   - IDs are case-sensitive

2. **Styling Issues**
   - Verify Tailwind CSS is properly loaded
   - Check for conflicting classes
   - Test responsiveness using browser developer tools

3. **External Links**
   - Verify URLs are complete and correct
   - Include https:// in external URLs
   - Test links in different browsers

4. **Images Not Loading**
   - Check image URLs are correct
   - Ensure images exist at specified paths
   - Verify image file permissions

Need help? Contact: premedpoland@gmail.com

Remember to:
- Test all changes in multiple browsers
- Check mobile responsiveness
- Back up files before making changes
- Validate HTML at [W3C Validator](https://validator.w3.org/)