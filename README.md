# K.E.M. Innovations Website

A professional website for K.E.M. Innovations, LLC - an IT Consulting company offering technology consulting, technical support, and app development services.

## Files Included

```
kem-website/
├── index.html          # Homepage
├── services.html       # Services page
├── about.html          # About/Team page
├── contact.html        # Contact page with form
├── styles.css          # Main stylesheet
├── images/
│   ├── logo-badge.jpeg      # Circular badge logo
│   └── logo-horizontal.png  # Horizontal logo
└── README.md           # This file
```

## Deploying to GitHub Pages

Follow these steps to get your website live:

### Step 1: Create a GitHub Account (if you don't have one)
1. Go to [github.com](https://github.com)
2. Click "Sign up" and follow the prompts

### Step 2: Create a New Repository
1. Click the "+" icon in the top right corner
2. Select "New repository"
3. Name it: `keminnovations.github.io` (or any name you prefer)
4. Make sure it's set to **Public**
5. Click "Create repository"

### Step 3: Upload Your Website Files
1. On your new repository page, click "uploading an existing file"
2. Drag and drop ALL the files from this folder:
   - `index.html`
   - `services.html`
   - `about.html`
   - `contact.html`
   - `styles.css`
   - `images/` folder (with both logos inside)
3. Click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to your repository's **Settings** tab
2. Scroll down to **Pages** in the left sidebar
3. Under "Source", select **Deploy from a branch**
4. Under "Branch", select **main** and **/ (root)**
5. Click **Save**

### Step 5: Connect Your GoDaddy Domain
1. In GitHub Pages settings, under "Custom domain", enter: `keminnovations.com`
2. Click Save

Now go to GoDaddy:
1. Log into your GoDaddy account
2. Go to **My Products** → Find your domain → Click **DNS**
3. Delete any existing A records or CNAME for @ or www
4. Add these **A Records** (Type: A, Name: @):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
5. Add a **CNAME Record**:
   - Type: CNAME
   - Name: www
   - Value: `yourusername.github.io` (replace with your GitHub username)
6. Save changes

**Note:** DNS changes can take up to 48 hours to propagate, but usually work within a few hours.

### Step 6: Enable HTTPS
1. Once your domain is connected, go back to GitHub Pages settings
2. Check "Enforce HTTPS" (may take a few minutes to become available)

## Making the Contact Form Work

The contact form is set up to use [Formspree](https://formspree.io), a free form handling service.

1. Go to [formspree.io](https://formspree.io) and create a free account
2. Create a new form
3. Copy your form ID (looks like: `f/xyzabc123`)
4. In `contact.html`, find this line:
   ```html
   <form id="contactForm" action="https://formspree.io/f/your-form-id" method="POST">
   ```
5. Replace `your-form-id` with your actual Formspree form ID

## Customizing the Site

### To update text content:
Open the HTML files in any text editor and modify the text between the tags.

### To update colors:
Open `styles.css` and modify the CSS variables at the top:
```css
:root {
  --navy-dark: #0a1628;
  --navy: #0d1b2a;
  --blue-primary: #0099dd;
  /* etc... */
}
```

### To add team member photos:
1. Add your photos to the `images/` folder
2. In `about.html`, find the team cards and replace the placeholder with:
   ```html
   <div class="team-photo">
     <img src="images/your-photo.jpg" alt="Name" style="width: 100%; height: 100%; object-fit: cover;">
   </div>
   ```

### To update team member names:
In `about.html`, find the team cards and update:
```html
<h3>Your Name</h3>
<p class="team-role">Co-Founder</p>
```

## Need Help?

If you run into any issues with the deployment, GitHub has excellent documentation:
- [GitHub Pages Quickstart](https://docs.github.com/en/pages/quickstart)
- [Managing a custom domain](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

Built with ❤️ for K.E.M. Innovations, LLC
