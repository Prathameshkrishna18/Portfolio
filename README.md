# Prathamesh Chavan — Personal Portfolio Website

A responsive personal portfolio website built with HTML5, CSS3, Bootstrap-based styling, and vanilla JavaScript (jQuery + a few small plugins for animations, carousels, and scroll effects).

## Structure

```
.
├── index.html      → The entire single-page site (Home, About, Resume, Projects, Contact)
├── css/            → Stylesheets (Bootstrap-icon libs, animation, carousel, and the main style.css)
├── js/             → jQuery + plugin scripts (carousel, animation, scroll effects) + main.js
├── fonts/           → Icon font files (Flaticon, IcoMoon, Ionicons, Open Iconic)
└── images/          → Site images and project thumbnails
```

This is a **static site** — no build step, no server-side code, no dependencies to install. Opening `index.html` directly in a browser (or serving the folder with any static file host) is all that's needed.

## Before you deploy — a few things worth updating

- The **"Download Resume"** and **"Download CV"** buttons currently link to `#` (placeholder). Upload your resume PDF into the repo (e.g. `resume.pdf`) and update those two `href="#"` links in `index.html` to point to it.
- The **Facebook icon** in the footer social links also points to `#` — either add your real profile URL or remove that `<li>`.

## Deploy — Option 1: GitHub Pages

1. Create a new **public** GitHub repository (e.g. `portfolio`).
2. Push these files to the repo root (see git commands below).
3. On GitHub, go to your repo → **Settings → Pages**.
4. Under **Build and deployment → Source**, select **Deploy from a branch**.
5. Under **Branch**, select `main` and folder `/ (root)`, then **Save**.
6. Wait 1–2 minutes — GitHub will publish your site at:
   `https://<your-username>.github.io/<repo-name>/`

```bash
git init
git add .
git commit -m "Initial commit - portfolio website"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Deploy — Option 2: Vercel

**Via the Vercel dashboard (no CLI needed):**
1. Push this repo to GitHub first (steps above).
2. Go to [vercel.com](https://vercel.com) → sign in with GitHub → **Add New… → Project**.
3. Select your `portfolio` repository → click **Import**.
4. Vercel auto-detects it as a static site (no framework, no build command needed) — leave the defaults.
5. Click **Deploy**. In under a minute you'll get a live URL like `https://<repo-name>.vercel.app`.

**Via the Vercel CLI (alternative):**
```bash
npm install -g vercel
cd portfolio          # this project's folder
vercel                # follow the prompts, accept defaults for a static site
vercel --prod         # promote to your production URL
```

Both platforms are free for a static personal portfolio like this one, and both auto-redeploy whenever you push new commits to GitHub.
