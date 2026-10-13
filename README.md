# Magesh K — VR Developer Portfolio & Hosting Guide

This guide explains how to host this portfolio website online with all gallery images and the resume download fully functioning.

---

## 📁 1. Project Structure Checklist

Before deploying, ensure your folder structure looks exactly like this:

```text
magesh-vr-portfolio/
│
├── index.html                   # Main portfolio webpage
├── Magesh_K_Resume.pdf          # Downloadable PDF resume
├── README.md                    # Project documentation & hosting guide
│
└── images/                      # Project gallery screenshots
    ├── simulation-environment.png
    ├── training-mode.jpg
    ├── object-interactions.jpg
    └── assessment-data.jpg
```

> **Important (Case Sensitivity)**: Web hosting providers (like GitHub Pages and Vercel) run on Linux servers, which are case-sensitive. Always preserve exact filenames and folder names (e.g., lowercase `images/` and matching file extensions `.png`, `.jpg`, `.pdf`).

---

## 🚀 2. Recommended Hosting Options

Choose any of the three free hosting methods below:

### Option A: Deploy with Vercel (Recommended — Fastest & Zero Config)

Since your software portfolio is already hosted on Vercel (`my-portfolio-dmt1.vercel.app`), this is the easiest and fastest method.

#### Via GitHub & Vercel Dashboard:
1. Push your folder to a GitHub repository (see [Section 3](#-3-pushing-to-github-step-by-step)).
2. Go to [vercel.com](https://vercel.com) and log in.
3. Click **"Add New..."** → **"Project"**.
4. Select your `magesh-vr-portfolio` repository from GitHub.
5. Keep all default settings (Framework Preset: **Other**, Root Directory: `./`).
6. Click **Deploy**.
7. In ~15 seconds, your site is live with an automatic HTTPS URL (e.g., `https://magesh-vr-portfolio.vercel.app`).

#### Via Vercel CLI (Direct Terminal Upload):
1. In your terminal, run:
   ```bash
   npx vercel
   ```
2. Follow the 3 prompts (Log in → Link existing project: No → Deploy).
3. Run `npx vercel --prod` to push directly to production.

---

### Option B: Deploy with GitHub Pages (Free with your GitHub account)

Host directly on your GitHub profile (`https://magesh-03-k.github.io/magesh-vr-portfolio/`):

1. Initialize git and push to GitHub (see [Section 3](#-3-pushing-to-github-step-by-step)).
2. Open your repository on [github.com/Magesh-03-K](https://github.com/Magesh-03-K).
3. Go to **Settings** (tab at the top) → **Pages** (on the left menu).
4. Under **Build and deployment**:
   - **Source**: Select `Deploy from a branch`.
   - **Branch**: Select `main` and folder `/(root)`.
5. Click **Save**.
6. Wait 1–2 minutes, then refresh the page. GitHub Pages will display your live URL!

---

### Option C: Deploy with Netlify Drop (Instant Drag-and-Drop, No Git Required)

If you want a live link in 30 seconds without running any commands:

1. Go to [app.netlify.com/drop](https://app.netlify.com/drop).
2. Open File Explorer on Windows to `C:\learn_coding\`.
3. Drag and drop the whole `magesh-vr-portfolio` folder into the browser window.
4. Netlify will deploy it instantly and give you a live URL.
5. (Optional) You can customize the site name in Netlify's **Site configuration** → **Change site name**.

---

## 🛠️ 3. Pushing to GitHub (Step-by-Step)

Open PowerShell or Command Prompt in `C:\learn_coding\magesh-vr-portfolio`:

```powershell
# 1. Navigate to the project directory
cd "C:\learn_coding\magesh-vr-portfolio"

# 2. Initialize Git
git init

# 3. Add all files (including images folder and PDF)
git add .

# 4. Check that all files and images are staged
git status

# 5. Commit the files
git commit -m "Initial commit: VR portfolio with project gallery images and resume"

# 6. Set the main branch
git branch -M main

# 7. Create a new public repository on GitHub named 'magesh-vr-portfolio'
# Then link your local repo to GitHub (replace with your repo URL):
git remote add origin https://github.com/Magesh-03-K/magesh-vr-portfolio.git

# 8. Push to GitHub
git push -u origin main
```

---

## ✅ 4. Post-Deployment Verification Checklist

Once deployed to your live URL, verify the following:

- [ ] **Gallery Images**: Scroll to **01 / Featured Project → Project Gallery** and check that all 4 thumbnails load:
  - Simulation Environment (`images/simulation-environment.png`)
  - Training Mode (`images/training-mode.jpg`)
  - Object Interactions (`images/object-interactions.jpg`)
  - Assessment Data (`images/assessment-data.jpg`)
- [ ] **Lightbox Modal**: Click each card to confirm that the full-size preview, title, tags, and caption pop up cleanly.
- [ ] **Resume Download**: Click the **Download Resume** button in the Hero section and in the Contact section to confirm `Magesh_K_Resume.pdf` downloads and opens properly.
- [ ] **Social Links**: Confirm GitHub, LinkedIn, and Email links direct to your profiles.

---

## 🔄 5. How to Update Content in the Future

Whenever you add new screenshots, update your resume, or change text:

1. Replace the file locally (e.g., overwrite `Magesh_K_Resume.pdf` with your updated resume, or add images in `images/`).
2. Run:
   ```bash
   git add .
   git commit -m "Update resume and gallery assets"
   git push origin main
   ```
3. Vercel or GitHub Pages will automatically re-build and publish the updates within seconds!
