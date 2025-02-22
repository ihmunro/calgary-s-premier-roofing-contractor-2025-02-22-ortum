# Premier Roofing Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Premier Roofing landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-800 hover:text-gray-600">
    Premier Roofing  <!-- Update this text -->
</a>
```

2. **Navigation Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update menu items here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Calgary's Premier Roofing Contractor  <!-- Update main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Our goal is to continually provide...  <!-- Update subheading -->
</p>
```

#### Understanding Tailwind Classes
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `font-bold`: Makes text bold
- `text-gray-600`: Sets text color to medium gray

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg">
    <!-- Icon -->
    <h3 class="text-xl font-bold mb-4">
        Ethical Practices  <!-- Update feature title -->
    </h3>
    <p class="text-gray-600">
        We maintain the highest standards...  <!-- Update feature description -->
    </p>
</div>
```

## Managing Links

### Navigation Links
1. Internal links (same-page sections):
```html
<a href="#features">Features</a>  <!-- Links to features section -->
<a href="#benefits">Benefits</a>  <!-- Links to benefits section -->
```

2. External links:
```html
<a href="https://calgaryspremierroofer.com" class="inline-block bg-blue-600">
    Get Your Free Quote  <!-- Update URL and text -->
</a>
```

### Footer Links
Update company information and links in the footer:
```html
<div>
    <p class="text-gray-400 mb-2">
        Email: iainhmunro@gmail.com  <!-- Update contact info -->
    </p>
    <p class="text-gray-400">
        Calgary, Alberta  <!-- Update address -->
    </p>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
1. Create two new files in your project folder:
   - `privacy.html`
   - `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links with actual page links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li>
            <a href="privacy.html" class="text-gray-400 hover:text-white">
                Privacy Policy
            </a>
        </li>
        <li>
            <a href="terms.html" class="text-gray-400 hover:text-white">
                Terms of Service
            </a>
        </li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Links**
   - Check that all `href` attributes start with either:
     - `#` for same-page sections
     - `./` for local pages
     - `https://` for external websites

2. **Responsive Design Issues**
   - Ensure Tailwind responsive classes are in order:
     - `text-base md:text-lg lg:text-xl`
     - Never: `lg:text-xl md:text-lg text-base`

3. **Animation Not Working**
   - Verify AOS script is loaded:
```html
<script src="https://unpkg.com/aos@next/dist/aos.js"></script>
<script>
    AOS.init({
        duration: 1000,
        once: true,
    });
</script>
```

### Best Practices
- Always test changes in multiple browsers
- Check mobile responsiveness using browser dev tools
- Maintain consistent spacing and indentation
- Keep backup copies before making major changes

Need additional help? Contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).