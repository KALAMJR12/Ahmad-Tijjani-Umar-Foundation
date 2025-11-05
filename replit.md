# Ahmad Tijjani Foundation Website

## Overview

This is a static website for the Ahmad Tijjani Foundation, a youth development organization. The site showcases programs, provides a photo gallery, and handles contact/application forms. It's built with vanilla HTML, CSS, and JavaScript, designed to be hosted on static hosting platforms like Netlify.

The website features:
- Responsive design for mobile, tablet, and desktop
- Automatic hero image slideshow with call-to-action buttons
- Program showcase with application forms
- Interactive photo gallery with modal view
- Contact forms with Netlify Forms integration
- Donate page with bank transfer and online payment options (Paystack & Flutterwave)
- Volunteer registration form with comprehensive application
- Mobile-friendly navigation

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Technology Stack:**
- Pure HTML5, CSS3, and vanilla JavaScript (no frameworks)
- Google Fonts (Poppins) for typography
- Font Awesome 6.4.0 for icons
- Responsive design using CSS Flexbox and Grid

**File Structure:**
- `index.html` - Main homepage with all content sections
- `donate.html` - Donation page with payment gateway integration
- `volunteer.html` - Volunteer registration page with application form
- `success.html` - Thank you page for form submissions
- `styles.css` - Centralized styling with CSS custom properties for theming
- `script.js` - All interactive functionality (slideshow, gallery, navigation)

**Design Pattern:**
- Single-page application structure with anchor-based navigation
- CSS variables in `:root` for easy theme customization
- Mobile-first responsive approach
- Modular JavaScript with clearly separated concerns (navigation, slideshow, gallery, forms)

**Key Features:**
1. **Hero Slideshow**: Auto-rotating image carousel with manual controls and CTA buttons for Donate/Volunteer
2. **Gallery System**: Image grid with modal popup, configured via `galleryImages` array
3. **Mobile Navigation**: Hamburger menu with toggle functionality across all pages
4. **Smooth Scrolling**: JavaScript-powered smooth navigation between sections
5. **Payment Integration**: Paystack and Flutterwave payment gateways for online donations
6. **Multi-page Structure**: Separate pages for home, donate, and volunteer functions

**Customization Approach:**
- Color scheme controlled through CSS variables (`:root` in styles.css)
- Content images managed through JavaScript arrays (easy to update)
- Inline documentation comments guide developers to update sections

### Static Hosting

**Platform:** Netlify (configured for form handling)
- Forms use `data-netlify="true"` attribute for automatic processing
- Success page redirect after form submission
- No server-side code required

**Form Handling:**
- Contact forms and program applications integrated with Netlify Forms
- Client-side validation (handled by browser)
- Redirect to `success.html` on successful submission

### Content Management

**Image Management:**
- Hero slideshow images: Array-based configuration in `script.js`
- Gallery images: Array-based configuration in `script.js`
- Currently using Unsplash placeholder images (need replacement with actual foundation photos)

**Content Updates:**
- All content embedded directly in HTML (no CMS)
- Section-specific comments in HTML guide content updates
- Payment gateway API keys need to be updated in donate.html before going live
- Bank account details in donate.html should be updated with actual foundation account
- No database or dynamic content generation

## External Dependencies

### Third-Party Services

1. **Google Fonts**
   - Font: Poppins (weights: 300, 400, 600, 700)
   - CDN: fonts.googleapis.com
   - Purpose: Typography across entire site

2. **Font Awesome**
   - Version: 6.4.0
   - CDN: cdnjs.cloudflare.com
   - Purpose: Icons for UI elements

3. **Unsplash**
   - Purpose: Placeholder images for hero slideshow and gallery
   - Note: Should be replaced with actual foundation photos

4. **Netlify Forms**
   - Purpose: Form submission handling without backend code
   - Integration: HTML attribute `data-netlify="true"`
   - Features: Spam protection, email notifications, submission storage
   - Forms: Contact form, Program applications, Volunteer applications

5. **Paystack**
   - Purpose: Online payment processing for donations
   - Integration: Inline JS library with public API key
   - Supports: Cards, bank transfers, USSD, mobile money
   - Note: API keys in donate.html need to be replaced with live keys

6. **Flutterwave**
   - Purpose: Alternative payment gateway for donations
   - Integration: Inline checkout library
   - Supports: Multiple payment methods and currencies
   - Note: API keys in donate.html need to be replaced with live keys

### No Database

This is a static site with no database requirements. All content is hardcoded in HTML or configured through JavaScript arrays.

### No Backend APIs

The site operates entirely client-side with no custom backend. Form processing is handled by Netlify's built-in form service.

### Browser APIs Used

- **Intersection Observer**: Potentially for scroll animations (not visible in truncated files)
- **DOM Manipulation**: Standard JavaScript for interactive features
- **CSS Transitions/Animations**: For smooth UI interactions