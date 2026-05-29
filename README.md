# 🎮 GAMELAND — Animated Gaming Website

A premium, fully animated gaming website built with **GSAP**, **Three.js**, and vanilla HTML/CSS/JS. Dark aesthetic, custom cursor, preloader, video hero, WebGL transitions, and a full multi-page layout.

---

## 📸 Preview

> **Live pages:** `index.html` · `about.html` · `contacts.html` · `product.html`

---

## 🗂 Project Structure

```
gameland/
├── index.html              # Home — hero video slider, discover, story, CTA
├── about.html              # About — team, pillars, stats, mission
├── contacts.html           # Contacts — form, social links, info
├── product.html            # Product — coming soon, countdown, subscribe
│
├── assets/
│   ├── fonts/
│   │   ├── zentry-regular.woff2
│   │   ├── robert-regular.woff2
│   │   ├── robert-medium.woff2
│   │   └── general.woff2
│   └── img/
│       ├── favicon.ico
│       ├── about.webp / about-600.webp / about-1200.webp
│       ├── entrance.webp / entrance-600.webp / entrance-1200.webp
│       ├── contact-1.webp / contact-1-600.webp / contact-1-1200.webp
│       ├── contact-2.webp / contact-2-600.webp / contact-2-1200.webp
│       └── swordman.webp / swordman-600.webp / swordman-1200.webp
│
├── files/
│   ├── music.mp3
│   ├── feature-1.mp4
│   ├── feature-2.mp4
│   ├── feature-3.mp4
│   ├── feature-4.mp4
│   └── feature-5.mp4
│
├── css/
│   └── index.min.css
│
└── js/
    └── index.min.js
```

---

## ✨ Features

### Home (`index.html`)
- Animated **preloader** with progress bar and status messages
- Full-screen **video hero** with WebGL displacement transitions (Three.js)
- Mini video preview thumbnail that cycles on click
- **About** section with scroll-triggered mask clip animation
- **Discover** grid — 5 video feature cards + tilt effect (js-tilt)
- **Story** section with parallax tilt image
- **CTA** section with mouse-parallax decorative images
- Sticky header with scroll blur + mobile burger menu
- Background **audio toggle** with animated icon bars

### About (`about.html`)
- Full-viewport hero with `about.webp` background + gradient overlay
- Animated stat counters (2.4M players, 140+ games, 60+ countries, $4.2B assets)
- 4-pillar focus grid with inline SVG icons
- Team member grid with avatar initials
- CTA linking to contacts page

### Contacts (`contacts.html`)
- Split layout — info left, form right
- Decorative `swordman` + `contact` images as background art
- Contact info items (email, location, response time)
- Working **email subscribe form** with success state (no backend needed)
- Social links: Dribbble, GitHub, Discord

### Product (`product.html`)
- **Live countdown timer** (90-day launch target) with flip animation on seconds
- Email **waitlist subscribe form** with success confirmation
- Animated pulsing status badge
- 4 product preview cards (Radiant, Nexus, Zigma, Azul) with status tags
- Scan-line + grid background animation

---

## 🛠 Tech Stack

| Technology | Usage |
|---|---|
| HTML5 | Page structure |
| CSS3 | Animations, layout, responsive design |
| JavaScript (ES6+) | Interactions, countdown, form handling |
| [GSAP 3](https://gsap.com) | Scroll animations, text reveals, transitions |
| [Three.js r83](https://threejs.org) | WebGL displacement shader on hero video |
| Custom Fonts | Zentry, Robert, General (self-hosted `.woff2`) |

---

## 🚀 Getting Started

### 1. Clone or download

```bash
git clone https://github.com/Rafayalmani/gameland.git
cd gameland
```

### 2. Run locally

Open with any local server — the site uses ES modules so it **won't work** by just double-clicking `index.html`.

**Option A — VS Code Live Server**
```
Right-click index.html → Open with Live Server
```

**Option B — Python**
```bash
python -m http.server 5500
# then open http://localhost:5500
```

**Option C — Node**
```bash
npx serve .
```

### 3. Open in browser

```
http://127.0.0.1:5500
```

---

## 📄 Pages & Navigation

| Page | File | Nav Link |
|---|---|---|
| Home | `index.html` | GAMELAND logo / Nexus |
| About | `about.html` | About |
| Contacts | `contacts.html` | Contacts |
| Product | `product.html` | PRODUCT button (header) |

---

## 🎨 Design System

| Token | Value |
|---|---|
| Background | `#000000` |
| Accent | `#c7fb50` (neon yellow-green) |
| Secondary accent | `#00ffe0` (cyan — success states) |
| Body font | Robert Regular / Robert Medium |
| Display font | Zentry Regular |
| UI labels font | General |
| Border subtle | `rgba(255,255,255,0.07)` |
| Text muted | `rgba(255,255,255,0.35)` |

---

## 📱 Responsive

- Mobile-first layout with breakpoints at `600px` and `768px`
- Burger menu on mobile with animated toggle
- Hero font scales from `3.5rem` (mobile) to `10rem+` (desktop)
- Product grid auto-fits columns based on available width

---

## 🔧 Customisation

### Change the launch countdown date (`product.html`)
```js
// Line ~310 in product.html <script>
var launchDate = new Date();
launchDate.setDate(launchDate.getDate() + 90); // change 90 to your target days
```
Or set a fixed date:
```js
var launchDate = new Date('2026-12-01T00:00:00');
```

### Change contact email (`contacts.html`)
```html
<a href="mailto:team@example.com">team@example.com</a>
```

### Update social links (all pages)
```html
<a href="https://dribbble.com/YOUR_USERNAME" ...>
<a href="https://github.com/YOUR_USERNAME" ...>
<a href="https://discord.gg/YOUR_SERVER" ...>
```

### Swap hero videos (`index.html`)
Replace the `src` attributes on the `<video>` tags or update `feature-1.mp4` through `feature-5.mp4` in `/files/`.

---

## 📦 Build

The CSS and JS are pre-built (`index.min.css` / `index.min.js`). If you have access to the source build system:

```bash
npm install
npm run build
```

> If no `package.json` is present, the minified files are the final output — edit the HTML/CSS directly or add your own build step.

---

## 🪪 Credits

| Role | Name |
|---|---|
| Design & Development | [Rafay Almani](https://github.com/Rafayalmani) |
| Animation Library | [GSAP by GreenSock](https://gsap.com) |
| WebGL | [Three.js](https://threejs.org) |

---

## 📬 Contact

- **GitHub:** [github.com/Rafayalmani](https://github.com/Rafayalmani)
- **Dribbble:** [dribbble.com/rafayalmani](https://dribbble.com/rafayalmani)
- **Discord:** [discord.gg/Rafayalmani](https://discord.gg/Rafayalmani)
- **Email:** team@example.com

---

## 📝 License

© 2026 GAMELAND. All rights reserved.  
Built and designed by **Rafay Almani**.