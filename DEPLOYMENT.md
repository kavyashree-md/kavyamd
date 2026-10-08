# 🚀 Kavya Shree M D — Portfolio Deployment Guide

This guide provides complete instructions for testing, debugging, and deploying Kavya's **Cyberpunk & Synthwave Developer Portfolio** to production hosting platforms.

---

## 📋 Architecture & Assets Overview

The portfolio is built as a pure, high-performance static web application requiring **no build steps, bundlers, or servers**:
- **Core Entry Point**: [`index.html`](./index.html) (Semantic HTML5, Vanilla CSS3 with Cyberpunk/Synthwave design system, and Vanilla JavaScript).
- **Embedded Document**: [`Kavya.pdf`](./Kavya.pdf) (Official Resume viewer & direct download).
- **Certification Document**: [`Certificate_KAVYA_SHREE_MD.pdf`](./Certificate_KAVYA_SHREE_MD.pdf) (Infosys Unix Certification PDF).
- **Media Assets**:
  - [`picture.jpeg`](./picture.jpeg) — Hero HUD profile image, avatar, social preview, and favicon.
  - [`smart_irrigation.jpg`](./smart_irrigation.jpg) — IoT Smart Irrigation project thumbnail & modal banner.
  - [`ai_predictive_engine.jpg`](./ai_predictive_engine.jpg) — AI Predictive Engine project thumbnail & modal banner.
  - [`unix_automation.jpg`](./unix_automation.jpg) — Unix Automation project thumbnail & modal banner.
  - [`boot_camp.jpeg`](./boot_camp.jpeg) — Department bootcamp milestone photo.
- **Deployment & SEO Helpers**:
  - [`.nojekyll`](./.nojekyll) — Disables Jekyll processing on GitHub Pages so all static files are served directly.
  - [`robots.txt`](./robots.txt) — Directs web crawlers and search engines.
  - [`sitemap.xml`](./sitemap.xml) — Sitemap listing pages and documents for Google/Bing indexing.
  - [`.gitignore`](./.gitignore) — Prevents temporary OS and scratch files from entering git history.

---

## 🔍 Pre-Deployment Component Test & Quality Audit

Every component has been verified across layout breakpoints and functional flows:

| Component | Tested Functionality | Status |
| :--- | :--- | :---: |
| **Navigation Bar** | Desktop fixed sidebar with smooth-scroll anchors (`#hero`, `#about`, `#skills`, `#timeline`, `#projects`, `#chat`, `#contact`). Active link highlighting on scroll spy. | ✅ Verified |
| **Mobile Drawer** | Mobile topbar (<1024px) with hamburger trigger, slide-in drawer, frosted backdrop, and ESC key dismissal. | ✅ Verified |
| **Theme Switcher** | Cyberpunk (dark neon) & Synthwave (day neon) palette toggle with persistence via `localStorage`. | ✅ Verified |
| **Resume Controls** | "View Resume" button opens full-screen HUD modal viewer with embedded PDF iframe and fallback; "Download Resume" triggers direct PDF download. | ✅ Verified |
| **Skill Filters** | Interactive filter pills ("All", "Core Languages", "Web & Cloud", "Tools & Hardware") with dynamic card display. | ✅ Verified |
| **Timeline Filters** | Interactive filter pills ("All", "Education", "Major Project", "Career Milestone") with direct link to certificate PDF. | ✅ Verified |
| **Project HUD Modals** | 4 detailed modal views for IoT, Machine Learning, Unix, and Portfolio projects with ESC key and backdrop close. | ✅ Verified |
| **Interactive AI Chat** | Simulated AI Kavya chatbot with preset prompt chips, animated typing indicator, auto-scroll, and documented API integration points. | ✅ Verified |
| **Contact Form** | Client-side validation with real-time error messages, submit button state handling, in-page confirmation box, and reset flow. | ✅ Verified |
| **Footer & Social Badges** | Accessible social badges with ARIA labels linking to LinkedIn, GitHub, and Gmail with neon hover glows. | ✅ Verified |
| **Responsive Grid** | Fluid layouts optimized for Mobile (<480px), Phablet/Tablet (481px–1024px), and Desktop (>1024px). | ✅ Verified |

---

## 🌐 Deployment Option 1: GitHub Pages (Recommended)

GitHub Pages is free, provides HTTPS out of the box, offers global CDN distribution, and allows custom domain setup.

### Step-by-Step Instructions:

#### Method A: Using Git CLI (Recommended)
1. **Open PowerShell or Terminal** in the project directory:
   ```powershell
   cd "c:\Users\SRUSTI H P\OneDrive\Desktop\KAVYA"
   ```
2. **Initialize Git and commit all files**:
   ```bash
   git init
   git add .
   git commit -m "Initial release: Kavya Shree M D Cyberpunk Portfolio"
   ```
3. **Create a new repository on GitHub**:
   - Log into [GitHub](https://github.com).
   - Click **New Repository** (e.g., `kavya-portfolio` or `kavyashree-md.github.io`).
   - Keep the repository **Public** (required for free GitHub Pages).
   - Do **NOT** initialize with a README, .gitignore, or license (we already created them).
4. **Push your code to GitHub**:
   ```bash
   git branch -M main
   git remote add origin https://github.com/<YOUR_GITHUB_USERNAME>/<YOUR_REPOSITORY_NAME>.git
   git push -u origin main
   ```
5. **Enable GitHub Pages**:
   - Go to your repository on GitHub.
   - Navigate to **Settings** > **Pages** (under the "Code and automation" section).
   - Under **Build and deployment**:
     - **Source**: Select `Deploy from a branch`.
     - **Branch**: Select `main` and folder `/ (root)`.
     - Click **Save**.
6. **Access Your Live Website**:
   - Wait 1–2 minutes for the deployment workflow to complete.
   - Your site will be live at:
     ```
     https://<YOUR_GITHUB_USERNAME>.github.io/<YOUR_REPOSITORY_NAME>/
     ```
   *(Or `https://<YOUR_GITHUB_USERNAME>.github.io/` if named `<username>.github.io`)*.

---

#### Method B: Using GitHub Web Uploader (No CLI needed)
1. Log into [GitHub](https://github.com) and click **New Repository**.
2. Name it `kavya-portfolio`, set to **Public**, and click **Create repository**.
3. Click the link that says **"uploading an existing file"**.
4. Drag and drop all files from this folder into the upload window:
   - `index.html`
   - `Kavya.pdf`
   - `Certificate_KAVYA_SHREE_MD.pdf`
   - `picture.jpeg`
   - `smart_irrigation.jpg`
   - `ai_predictive_engine.jpg`
   - `unix_automation.jpg`
   - `boot_camp.jpeg`
   - `.nojekyll`, `robots.txt`, `sitemap.xml`, `.gitignore`
5. Click **Commit changes**.
6. Go to **Settings** > **Pages**, choose branch `main` and folder `/ (root)`, and click **Save**.

---

## ⚡ Deployment Option 2: Vercel (Instant 1-Click Deploy)

Vercel provides instant static asset delivery with global edge caching and free custom domains.

1. Go to [Vercel](https://vercel.com) and sign up / log in with GitHub.
2. Click **Add New...** > **Project**.
3. Import your GitHub repository (`kavya-portfolio`).
4. Keep the Framework Preset as **Other** (Root directory: `./`).
5. Click **Deploy**.
6. Your portfolio will deploy in under 15 seconds to a URL like:
   ```
   https://kavya-portfolio.vercel.app
   ```

---

## 🌍 Deployment Option 3: Netlify (Drag & Drop)

If you want an instant live URL without using Git or CLI:

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Sign in or continue as guest.
3. Drag and drop the `KAVYA` folder directly into the browser upload box.
4. Netlify will deploy it instantly and provide a live URL (e.g. `https://kavya-portfolio.netlify.app`).

---

## 🔗 Live Service Integration Pointers

### 1. Connecting a Live Contact Form Email Service
In `index.html` (lines ~7700–7740), replace the client-side simulation with a real email-sending API:
- **Resend API**: Call `https://api.resend.com/emails` with your API key from a backend serverless function.
- **Formspree** (No backend needed):
  Update the `<form>` tag:
  ```html
  <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="contact-form">
  ```
- **EmailJS** (Direct browser email sending):
  Add the EmailJS CDN script and call `emailjs.send("service_id", "template_id", params)`.

### 2. Connecting a Live LLM (OpenAI / Gemini) to AI Kavya
In `index.html` (lines ~7340–7380), the code contains pre-configured placeholders to connect the chatbot to GPT-4o or Gemini 1.5 Flash via a serverless proxy or edge route.

---

## ✅ Post-Deployment Verification Checklist

Once deployed, visit your live URL and confirm:
- [ ] Page loads with cyberpunk styling, fonts, and smooth animations.
- [ ] Clicking "View Resume" opens the full-screen modal with PDF preview.
- [ ] Clicking "Download Resume" downloads `Kavya_Shree_MD_Resume.pdf`.
- [ ] Clicking "View Certificate" in the timeline opens the Infosys certificate.
- [ ] AI Chatbot responds to prompts and chip clicks with typing animations.
- [ ] Contact form validates inputs and displays the confirmation box upon submission.
- [ ] Social links open Kavya's LinkedIn, GitHub, and email in new tabs.
- [ ] Testing on mobile device: Hamburger menu opens and closes seamlessly.
