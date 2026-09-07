# Kaylan Moonsamy — Portfolio Website

A dark-themed, animated personal portfolio built with plain **HTML, CSS and JavaScript**
(no frameworks, no build step) — ready to deploy on **GitHub Pages**.

## What's included

```
portfolio/
├── index.html              Main page — all sections live here
├── css/
│   └── style.css           All styling (dark theme, cyan accent, animations)
├── js/
│   └── script.js           All interactivity (typewriter, scroll reveal, particles, tilt, nav)
├── images/
│   └── profile-placeholder.svg   Placeholder profile picture — swap this out
└── README.md                This file
```

## Sections currently on the page

- **Home** — animated intro with a typewriter effect and a particle background
- **About** — who you are + "What I Do" cards
- **Skills** — all skill categories and certifications pulled from your CV
- **Projects** — ElevateED, DUT Residence Management System, Truck Delivery Management System (each linking to your GitHub repo)
- **Websites** — a placeholder area for live demo links once you deploy your projects (this portfolio's own GitHub Pages link is wired up automatically)
- **Interests** — a clearly marked placeholder, ready for you to fill in your hobbies
- **Contact** — email, phone, GitHub, location

## Things left for you to fill in

1. **More photos (optional).** Your headshot is already wired up as `images/profile.jpg`
   and shown in the About section. If you want to swap it for a different one later, just
   replace that file (keep the name `profile.jpg`, or update the `src` on the `<img id="profileImg">`
   tag in `index.html`). You can add more photos anywhere else you'd like (project
   screenshots, etc.) the same way.

2. **Interests / hobbies section.** Already filled in (gym, gaming, fishing, hiking,
   anime, volleyball, soccer, learning, tech, forex trading). To add more later, open
   `index.html`, find `<section id="interests">` and copy one of the existing
   `.interest-card` blocks for a consistent look.

3. **Live website links.** Once you deploy ElevateED, the Residence Management System
   or the Truck Delivery System somewhere, replace the "Coming Soon" card in the
   `<section id="websites">` block with real links, following the pattern of the
   first card.

4. Double check your phone number / email in `index.html` if anything changes.

## Running it locally

Just open `index.html` in your browser — everything is self-contained, no server or
build tools required. For live-reload while editing, you can use the VS Code
"Live Server" extension, or run:

```bash
python3 -m http.server 8000
```

and visit `http://localhost:8000`.

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `kaylan-443.github.io` for a personal
   root-domain site, or any name like `portfolio` for a project site).
2. Push this folder's contents to that repository:
   ```bash
   git init
   git add .
   git commit -m "Initial portfolio site"
   git branch -M main
   git remote add origin https://github.com/kaylan-443/<your-repo-name>.git
   git push -u origin main
   ```
3. On GitHub, go to **Settings → Pages**.
4. Under "Build and deployment", set **Source** to `Deploy from a branch`,
   pick the `main` branch and `/ (root)` folder, then **Save**.
5. GitHub will give you a live URL, usually:
   - `https://kaylan-443.github.io/` (if the repo is named `kaylan-443.github.io`)
   - `https://kaylan-443.github.io/<repo-name>/` (for any other repo name)

It can take a minute or two for the site to go live after your first deploy.

## Notes on tech choices

Everything here is static HTML/CSS/JS by design — that's exactly what GitHub Pages
serves natively, with no backend needed. Python wasn't used since there's no dynamic
server logic required for a static portfolio; if you later want a contact form that
actually sends emails, you'd typically wire the form up to a free service like
Formspree or EmailJS rather than needing your own Python backend.

## Customizing colors

All colors are defined as CSS variables at the top of `css/style.css` under `:root`.
Change `--accent` and `--accent-2` to restyle the whole site's accent color in one place.
