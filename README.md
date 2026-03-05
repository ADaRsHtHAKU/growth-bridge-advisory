# Growth Bridge Advisory — Website

> **Build Smart. Grow Strong.**  
> A fully responsive, static consulting portfolio site built with plain HTML, CSS, and vanilla JavaScript.

---

## 📁 Project Structure

```
growth-bridge-advisory/
│
├── index.html              ← Main HTML (entry point)
│
├── css/
│   ├── variables.css       ← Design tokens (colours, shadows, radii)
│   ├── base.css            ← Reset, typography, shared utilities, footer
│   ├── header.css          ← Fixed nav, logo, hamburger, mobile menu
│   ├── hero.css            ← Hero section
│   ├── sections.css        ← About, Services, Insights, Why Us, Contact
│   ├── animations.css      ← Scroll fade-up classes
│   └── responsive.css      ← Media queries (≤900px, ≤600px)
│
├── js/
│   └── main.js             ← Hamburger, scroll animations, smooth scroll
│
├── assets/                 ← Place images, favicon, OG image here
│
├── .vscode/
│   └── settings.json       ← Recommended VS Code workspace settings
│
├── .gitignore
└── README.md
```

---

## 🖥️ Opening in VS Code

### 1. Clone or download the project

**If you cloned from GitHub:**
```bash
git clone https://github.com/YOUR_USERNAME/growth-bridge-advisory.git
cd growth-bridge-advisory
code .
```

**If you downloaded the ZIP:**
1. Extract the ZIP
2. Open VS Code → **File → Open Folder** → select `growth-bridge-advisory/`

### 2. Install the Live Server extension (one-time)

1. In VS Code press `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (Mac)
2. Search **"Live Server"** by Ritwick Dey
3. Click **Install**

### 3. Launch the site locally

- Right-click `index.html` in the Explorer panel → **"Open with Live Server"**
- Or click **"Go Live"** in the VS Code status bar at the bottom right

The site opens at `http://127.0.0.1:5500` and auto-reloads on every file save.

### Recommended VS Code extensions

| Extension | Purpose |
|-----------|---------|
| Live Server | Instant local dev server with hot-reload |
| Prettier | Auto-format HTML, CSS, JS |
| CSS Peek | Jump to CSS definitions from HTML |
| IntelliSense for CSS | Autocomplete class names in HTML |

---

## 🚀 Hosting on GitHub Pages (free)

### Step 1 — Create the GitHub repository

1. Go to [github.com](https://github.com) and log in (or sign up)
2. Click the **+** icon → **New repository**
3. Name it `growth-bridge-advisory` (or anything you like)
4. Set visibility to **Public** (required for free GitHub Pages)
5. Leave "Add README" **unchecked** (we already have one)
6. Click **Create repository**

### Step 2 — Push your code

In your terminal, from inside the project folder:

```bash
# Initialise git (skip if already done)
git init

# Stage all files
git add .

# First commit
git commit -m "Initial commit — Growth Bridge Advisory website"

# Link to your GitHub repo (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/growth-bridge-advisory.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. On GitHub, go to your repo → **Settings** tab
2. Scroll down to **Pages** in the left sidebar
3. Under **Source**, choose **Deploy from a branch**
4. Select branch: `main` | folder: `/ (root)`
5. Click **Save**

Within 1–2 minutes your site is live at:
```
https://YOUR_USERNAME.github.io/growth-bridge-advisory/
```

### Step 4 — Every future update

```bash
git add .
git commit -m "describe your change"
git push
```

GitHub Pages automatically redeploys within ~60 seconds.

---

## 🌐 Hosting on Netlify (free, with form handling)

### Option A — Drag & Drop (fastest)

1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag your entire `growth-bridge-advisory/` folder onto the deploy zone
3. Done — Netlify Forms are active automatically (no backend needed)

### Option B — Connect to GitHub (recommended for ongoing work)

1. Log into Netlify → **Add new site → Import an existing project**
2. Choose **GitHub** → authorise → select your repo
3. Build settings:
   - Build command: *(leave blank — this is a static site)*
   - Publish directory: `.` (or leave blank)
4. Click **Deploy site**

The contact form (`data-netlify="true"`) works out of the box.  
Submissions appear in **Netlify → Forms** and can send email notifications.

### Custom domain (optional)

**Netlify:** Site Settings → Domain Management → Add custom domain  
**GitHub Pages:** Settings → Pages → Custom domain

---

## 📬 Contact Form Notes

### Netlify (default setup)
The form in `index.html` already has:
```html
<form name="contact" method="POST" data-netlify="true" action="/thank-you">
  <input type="hidden" name="form-name" value="contact" />
  ...
</form>
```
This works automatically — no backend required.

### InfinityFree / PHP hosting
Change the form's `action` attribute to `"contact.php"` and create a `contact.php` file using [PHPMailer](https://github.com/PHPMailer/PHPMailer) with your SMTP credentials.

---

## 🎨 Customisation Guide

| What to change | Where |
|----------------|-------|
| Brand colours  | `css/variables.css` → `:root` |
| Fonts          | `index.html` `<head>` Google Fonts link + `css/base.css` |
| Nav links      | `index.html` `<header>` section |
| Hero text      | `index.html` `#hero` section |
| Service cards  | `index.html` `#services` section |
| Blog posts     | `index.html` `#insights` section |
| Contact email  | Wire via Netlify Forms dashboard or `contact.php` |
| Favicon        | Add `favicon.ico` to root, link in `<head>` |

---

## 📄 License

MIT — free to use and modify for personal or commercial projects.
