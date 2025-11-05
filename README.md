# Ahmad Tijjani Foundation Website

A responsive website showcasing the youth development programs and activities of the Ahmad Tijjani Foundation.

## 🌟 Features

- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Hero Slideshow**: Automatic image slideshow with manual controls
- **Program Showcase**: Display current and upcoming programs with application forms
- **Photo Gallery**: Interactive gallery with modal view
- **Contact Forms**: Integrated with Netlify Forms for easy submission handling
- **Smooth Navigation**: Smooth scrolling and mobile-friendly menu

## 📁 File Structure

```
├── index.html          # Main HTML file
├── styles.css          # CSS styling
├── script.js           # JavaScript functionality
└── README.md          # This file
```

## 💳 Setting Up Payment Gateways (Important!)

Before going live with donations, you need to obtain and configure API keys from Paystack and/or Flutterwave:

### Getting Paystack API Keys

1. Sign up at [Paystack](https://paystack.com/)
2. Go to **Settings → API Keys & Webhooks**
3. Copy your **Public Key** (starts with `pk_test_` for testing or `pk_live_` for production)
4. Open `donate.html` and find line with `PAYSTACK_PUBLIC_KEY`
5. Replace the placeholder with your actual key:
   ```javascript
   const PAYSTACK_PUBLIC_KEY = 'pk_test_your_actual_key_here';
   ```

### Getting Flutterwave API Keys

1. Sign up at [Flutterwave](https://dashboard.flutterwave.com/signup)
2. Navigate to **Settings → API Keys**
3. Copy your **Public Key** (starts with `FLWPUBK_TEST-` for testing)
4. Open `donate.html` and find line with `FLUTTERWAVE_PUBLIC_KEY`
5. Replace the placeholder with your actual key:
   ```javascript
   const FLUTTERWAVE_PUBLIC_KEY = 'FLWPUBK_TEST-your_actual_key_here-X';
   ```

### Testing Payment Integration

Use these test cards to verify your integration works:

**Paystack Test Card:**
- Card: 4084 0840 8408 4081
- CVV: 408
- Expiry: Any future date
- PIN: 0000 (if prompted)

**Flutterwave Test Card:**
- Card: 4187 4274 1556 4246
- CVV: 828
- Expiry: 09/32
- PIN: 3310

### Updating Bank Details

Edit the bank transfer section in `donate.html` (around lines 103-118):
- Update bank name
- Update account name
- Update account number
- Update Swift code (if applicable)
- Update donation email address

## 🎨 Customization Guide

### Changing Colors

Edit the CSS variables in `styles.css` (lines 11-35):

```css
:root {
    --primary-color: #2c5f2d;      /* Main green color */
    --secondary-color: #f39c12;     /* Orange accent color */
    /* ... other colors ... */
}
```

### Updating Images

#### Hero Slideshow Images

Edit `script.js` (lines 25-41):

```javascript
const heroImages = [
    {
        url: 'your-image-url.jpg',
        caption: 'Your caption here'
    },
    // Add more images as needed
];
```

#### Gallery Images

Edit `script.js` (lines 44-72):

```javascript
const galleryImages = [
    {
        url: 'your-image-url.jpg',
        caption: 'Your caption here'
    },
    // Add more images as needed
];
```

### Adding or Removing Programs

Edit the Programs Section in `index.html` (around lines 141-226):

```html
<div class="program-card">
    <div class="program-icon">
        <i class="fas fa-graduation-cap"></i>  <!-- Change icon -->
    </div>
    <h3 class="program-title">Program Name</h3>
    <p class="program-description">Description here...</p>
    <div class="program-status">Status (e.g., "Currently Open")</div>
    <button class="btn btn-secondary apply-btn" data-program="Program Name">Apply Now</button>
</div>
```

**Available Icons**: Browse icons at [Font Awesome](https://fontawesome.com/icons)

### Updating Contact Information

Edit the Contact Section in `index.html` (lines 263-306):

- **Address**: Line 268
- **Phone**: Line 279
- **Email**: Line 289
- **Office Hours**: Line 299

### Updating Social Media Links

Edit the Footer Section in `index.html` (lines 482-487):

```html
<a href="https://facebook.com/yourpage" target="_blank">...</a>
<a href="https://twitter.com/yourhandle" target="_blank">...</a>
<!-- ... update each link ... -->
```

### Changing Text Content

#### About Section

Edit `index.html` lines 119-139:
- Mission statement
- Vision statement  
- Impact statistics

#### Hero Section

Edit `index.html` lines 66-68:
- Main headline
- Subtitle text

## 📝 Netlify Forms Setup

The website is configured for Netlify Forms. When deploying to Netlify:

1. **Contact Form**: Submissions go to `contact` form
2. **Application Form**: Submissions go to `program-application` form

To view form submissions:
1. Log into your Netlify dashboard
2. Go to your site
3. Click "Forms" in the navigation
4. View submissions for each form

### Form Fields

**Contact Form:**
- Name
- Email
- Subject
- Message

**Application Form:**
- Full Name
- Email
- Phone Number
- Age
- Program Selection (auto-filled)
- Education Level
- Motivation
- Additional Information

### Success Page

After form submission, users are redirected to a custom success page (`success.html`) that:
- Confirms their submission was received
- Provides information about response times
- Offers navigation back to the main site
- Can be customized to match your branding

## 🚀 Deployment to Netlify

### Method 1: Drag and Drop

1. Go to [Netlify](https://www.netlify.com/)
2. Sign up or log in
3. Drag and drop your project folder to the Netlify dashboard
4. Your site will be live instantly!

### Method 2: Git Integration

1. Push your code to GitHub
2. In Netlify, click "New site from Git"
3. Connect your repository
4. Netlify will automatically deploy

### Important Notes:

- Forms will automatically work once deployed to Netlify
- No build command needed (pure HTML/CSS/JS)
- No publish directory needed (root directory is fine)

## 🛠️ Local Development

To test locally, you can use any static file server:

**Using Python:**
```bash
python -m http.server 5000
```

**Using Node.js:**
```bash
npx http-server -p 5000
```

Then open `http://localhost:5000` in your browser.

## 📱 Browser Compatibility

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

## 💡 Tips for Updating

1. **Always test changes locally before deploying**
2. **Keep backups of your images and content**
3. **Use high-quality images (but optimize them for web)**
4. **Recommended image sizes:**
   - Hero images: 1920x1080px
   - Gallery images: 800x600px
   - About images: 600x400px

## 📞 Support

For technical assistance, refer to:
- [Netlify Forms Documentation](https://docs.netlify.com/forms/setup/)
- [Font Awesome Icons](https://fontawesome.com/icons)
- [Google Fonts](https://fonts.google.com/)

## 📄 License

© 2025 Ahmad Tijjani Foundation. All Rights Reserved.

---

**Built with ❤️ for youth development**
