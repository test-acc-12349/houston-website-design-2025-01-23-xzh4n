# Houston Website Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Houston Website Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To modify:

1. **Logo Text**
```html
<!-- Find this line in the header -->
<div class="text-2xl font-bold text-gray-800">HWD</div>
```
- Replace "HWD" with your desired logo text
- Adjust size by changing `text-2xl` to `text-3xl` for larger or `text-xl` for smaller

### Hero Section
Located at the top of the page with main headline:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Houston Website Design
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Houston</p>
```
- Update text between tags to change headlines
- Size classes explained:
  - `text-4xl`: Default size
  - `md:text-5xl`: Size on medium screens
  - `lg:text-6xl`: Size on large screens

### Features Section
To modify feature cards:

```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-paint-brush text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Custom Design</h3>
    <p class="text-gray-600">Unique, tailored designs...</p>
</div>
```
- Change icon by replacing `fa-paint-brush` with any [Font Awesome](https://fontawesome.com/icons) icon
- Update heading text in `<h3>` tags
- Modify description in `<p>` tags

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition duration-300">Contact</a>
</div>
```

To update links:
1. For internal sections, use `#section-id`
2. For external pages, use full URL: `https://example.com`
3. For local pages, use relative path: `about.html`

### Call-to-Action Links
Update the main CTA buttons:

```html
<!-- Find these lines -->
<a href="https://hwd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
```
- Replace `https://hwd.com` with your actual website URL
- Maintain the class attributes to preserve styling

### Social Media Links
Located in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition duration-300">
        <i class="fab fa-twitter text-xl"></i>
    </a>
    <!-- More social links -->
</div>
```
- Replace `#` with your social media profile URLs
- Change icons by modifying `fa-twitter` to other social media icons

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:

```html
<ul class="space-y-2">
    <!-- Add after existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues:

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify file locations in your directory

2. **Styling Problems**
   - Don't remove `class=""` attributes
   - Keep responsive classes (starting with `md:` or `lg:`)
   - Maintain spacing in class names

3. **Icons Not Showing**
   - Verify Font Awesome CDN link in header
   - Check icon class names on [Font Awesome](https://fontawesome.com/icons)
   - Ensure proper icon prefix (`fas`, `fab`, etc.)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Keep backups before making changes

Remember to test all changes on multiple devices and browsers to ensure proper functionality and appearance.