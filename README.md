# ✦ Personal Portfolio Template

A dark, animated single-page portfolio built in **vanilla HTML, CSS, and JavaScript** — no frameworks, no build tools, no dependencies except one font API and EmailJS for the contact form.

![Preview](https://images.unsplash.com/photo-1555066931-4365d14bab8c?w=1200&q=80)

---

## ✦ Features

- **Animated intro** — letters scatter on load
- **Ambient background** — floating red glow orbs + occasional plane flyover
- **Section 01 — About** — flip card with your info
- **Section 02 — Selected Work** — exploding computer animation reveals project cards with 3D flip
- **Section 03 — Photography** — scroll-driven fan of photos, slides in, lightbox on click + full gallery page
- **Section 04 — Interests** — staggered card reveal
- **Section 05 — Skills** — four-column skill grid
- **Section 06 — Playlist** — audio visualizer bar animation fades into section
- **Section 07 — Contact** — EmailJS-powered form, sends directly to your inbox
- **Recruiter View** — side panel with your key stats for recruiters
- **Custom cursor** — red dot that follows your mouse
- **Avatar chatbot** — answers basic questions about you
- **Unique section color themes** — each section has its own dark palette

---

## ✦ File Structure

```
portfolio/
├── index.html          ← Main portfolio (rename portfolio-template.html → index.html)
├── gallery.html        ← Full photo gallery page
└── README.md
```

---

## ✦ Setup — Step by Step

### Step 1 — Clone or download

```bash
git clone https://github.com/your-username/portfolio.git
cd portfolio
```

Or just download the ZIP and unzip it.

---

### Step 2 — Find and replace your info

Open `index.html` in any text editor (VS Code recommended) and search-replace the following placeholders:

| Placeholder | Replace with |
|---|---|
| `Your Name` | Your full name |
| `your-github-username` | Your GitHub username |
| `your-linkedin-id` | Your LinkedIn profile ID |
| `your@email.com` | Your email address |
| `Your Role` | e.g. Software Engineer |
| `Your Company` | e.g. Google |
| `Your City, Country` | e.g. San Francisco, CA |
| `Project One` | Your first project name |
| `Project Two` | Your second project name |
| `Project Three` | Your third project name |
| `YOUR_EMAILJS_PUBLIC_KEY` | Your EmailJS public key |
| `YOUR_EMAILJS_SERVICE_ID` | Your EmailJS service ID |
| `YOUR_EMAILJS_TEMPLATE_ID` | Your EmailJS template ID |

---

### Step 3 — Set up EmailJS (contact form)

So visitors can email you directly from the site:

1. Go to [emailjs.com](https://emailjs.com) and create a free account
2. **Add a Service** → choose your email provider (Gmail recommended) → connect your account → copy the **Service ID**
3. **Create a Template** → set:
   - **To Email**: your email address
   - **Subject**: `{{title}}`
   - **Body**: include `{{name}}`, `{{email}}`, `{{message}}`
   - Copy the **Template ID**
4. **Account** → copy your **Public Key**
5. Replace the three `YOUR_EMAILJS_*` placeholders in `index.html`

---

### Step 4 — Replace placeholder photos

The gallery and photography section use Unsplash placeholder images. Replace the URLs in the `URLS` array inside the photography JS section and in `gallery.html` with your own photos (Cloudinary, your own CDN, or relative paths work fine).

---

### Step 5 — Customise your projects

In `index.html` find the three project cards (search for `epc0`, `epc1`, `epc2`) and update:

- Project name
- Description (front and back of card)
- Tech tags
- GitHub link

---

### Step 6 — Customise the Recruiter View

Search for `id="rec-panel"` and update the stats, target roles, and skill bars to reflect your actual skills and percentages.

---

### Step 7 — Push to GitHub

```bash
# 1. Create a new repo on github.com (name it whatever you like)

# 2. Initialise git in your project folder
git init
git add .
git commit -m "Initial commit — portfolio template"

# 3. Connect to your GitHub repo
git remote add origin https://github.com/your-username/your-repo-name.git
git branch -M main
git push -u origin main
```

---

### Step 8 — Deploy (free options)

**GitHub Pages** (easiest):
1. Go to your repo → **Settings** → **Pages**
2. Source: **Deploy from a branch** → select `main` → `/ (root)`
3. Your site will be live at `https://your-username.github.io/your-repo-name`

**Netlify** (recommended — instant, custom domain):
1. Go to [netlify.com](https://netlify.com) → **Add new site** → **Import from Git**
2. Connect GitHub → select your repo → deploy
3. Live in ~30 seconds at a free `.netlify.app` URL

**Vercel**:
1. Go to [vercel.com](https://vercel.com) → **New Project** → import your repo
2. No config needed — deploys instantly

---

## ✦ Customisation Tips

- **Colors**: All CSS variables are at the top of `<style>`. Change `--red` and `--red2` to any accent color.
- **Fonts**: Uses [Fontshare](https://fontshare.com) — Clash Display (headings) + Satoshi (body). Swap in any Fontshare or Google Font.
- **Sections**: Each section is clearly commented. Delete any section you don't need.
- **Plane animation**: The SVG plane is baked in as base64. To replace it, convert your own SVG to base64 and swap the string in the `atob()` call.
- **Avatar chatbot**: Update the `kb` object in the JS with your own answers.

---

## ✦ Browser Support

Works in all modern browsers. Requires JavaScript enabled.

---

## ✦ License

MIT — use it however you want, no attribution required. A star on the repo is always appreciated ✦
