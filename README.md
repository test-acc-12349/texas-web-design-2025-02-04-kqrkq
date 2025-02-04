# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

### Hero Section
To update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
- Replace "Texas Web Design" and "Best Websites In Texas" with your text
- The classes `text-4xl`, `md:text-5xl`, and `lg:text-6xl` control text size at different screen sizes

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-server text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package at no additional cost.</p>
</div>
```
To modify:
1. Change the icon by replacing `fa-server` with any [Font Awesome](https://fontawesome.com/icons) icon name
2. Update the heading text ("Free Hosting")
3. Modify the description text

### Understanding Tailwind Classes
Common classes used in this template:
- `text-{size}`: Controls text size (xs, sm, base, lg, xl, 2xl, etc.)
- `mb-{number}`: Adds margin bottom (1-16)
- `p-{number}`: Adds padding (1-16)
- `bg-{color}-{shade}`: Sets background color
- `text-{color}-{shade}`: Sets text color

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute
2. Replace the value with:
   - `#section-id` for same-page links
   - `https://example.com` for external links
   - `./page.html` for internal pages

### Call-to-Action Links
Update the main CTA button:
```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">Get Started Today</a>
```
Replace `https://twd.com` with your desired URL.

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300"><i class="fab fa-twitter"></i></a>
    <a href="#" class="hover:text-white transition-colors duration-300"><i class="fab fa-facebook"></i></a>
    <a href="#" class="hover:text-white transition-colors duration-300"><i class="fab fa-linkedin"></i></a>
</div>
```
Replace `#` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Replace these placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```
With:
```html
<ul class="space-y-2">
    <li><a href="./privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="./terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues:

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly
   - Verify file locations relative to index.html

2. **Styling Problems**
   - Confirm Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Verify responsive classes (md:, lg:) are properly formatted

3. **Icons Not Showing**
   - Verify Font Awesome CSS is loaded
   - Check icon class names against Font Awesome documentation
   - Ensure internet connection for CDN access

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check the [Font Awesome icons](https://fontawesome.com/icons) reference
- Validate your HTML using [W3C Validator](https://validator.w3.org/)

Remember to always test your changes across different screen sizes using browser developer tools.