# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing your landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
The main headline and subtext are located in the "Hero Section". Look for:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold tracking-tight text-gray-900 mb-8">
    Lorem ipsum dolor
</h1>
```
To update:
1. Locate the text between the `<h1>` tags
2. Replace "Lorem ipsum dolor" with your desired headline
3. Keep the surrounding HTML tags intact

#### Features Section
Each feature card contains:
```html
<h3 class="text-xl font-semibold text-gray-900 mb-4">Feature 1</h3>
<p class="text-gray-600">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
```
To update feature content:
1. Find the feature cards in the Features Section
2. Replace "Feature 1" with your feature name
3. Update the description text in the `<p>` tag

### Tailwind CSS Classes

#### Understanding Responsive Classes
In this template, responsive classes use these prefixes:
- `md:` - applies to medium screens (768px and up)
- `lg:` - applies to large screens (1024px and up)

Example:
```html
<div class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Default size: text-4xl (36px)
- Medium screens: text-5xl (48px)
- Large screens: text-6xl (60px)

#### Common Class Modifications

**Changing Colors**
To update the gradient background in the CTA section:
```html
<section class="py-24 bg-gradient-to-r from-purple-600 to-pink-600">
```
You can modify:
- `from-purple-600` to any color (e.g., `from-blue-600`)
- `to-pink-600` to any color (e.g., `to-green-600`)

**Adjusting Spacing**
Padding and margin classes follow this pattern:
- `p-` for padding
- `m-` for margin
- Numbers represent size (1-16)

Example:
```html
<div class="p-8 mb-6">  <!-- 8 units padding, 6 units bottom margin -->
```

## Fixing Broken Links

### Navigation Menu Links
Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```

To update:
1. Locate the `href="#"` attribute
2. Replace with proper link path:
   - Internal section: `href="#features"`
   - External page: `href="https://yoursite.com/page"`

### Footer Links
Current placeholder links are in the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Features</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Benefits</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Contact</a></li>
</ul>
```

Update these following the same process as navigation links.

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
In the footer's legal section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <!-- ... -->
    </ul>
</div>
```

### Adding Terms of Service Link
In the same section:
```html
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

To implement:
1. Create privacy.html and terms.html files in your root directory
2. Update the href attributes to point to these files
3. Ensure the files exist before pushing live

## Troubleshooting

### Common Issues

**Broken Responsive Design**
If your responsive design breaks:
1. Check for missing `md:` or `lg:` prefixes
2. Verify container classes remain intact:
```html
<div class="container mx-auto px-6">
```

**Missing Styles**
If Tailwind styles aren't applying:
1. Verify the Tailwind CSS link is present in the head:
```html
<link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
```
2. Check for typos in class names

Remember to:
- Test all changes across different screen sizes
- Validate links before pushing live
- Keep backups of working versions
- Test in multiple browsers

Need help? Consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.