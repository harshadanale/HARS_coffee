# ☕ HARS — The Art of Coffee
### Premium Café Website · Kolhapur, Maharashtra

![HARS Coffee](https://images.unsplash.com/photo-1447933601403-0c6688de566e?w=1200&q=80&fit=crop)

> *"Where Every Sip Becomes Art"*

A fully animated, award-worthy café website built with pure **HTML, CSS, and Vanilla JavaScript** — no frameworks, no dependencies, no build tools. Just drop the files in a folder and open.

---

## 🗂️ File Structure

```
hars-coffee/
├── hars-coffee-warm.html     # Main website (open this)
├── golden-latte.png          # Custom product photo — Golden Latte
├── kyoto-pour-over.png       # Custom product photo — Kyoto Pour Over
└── README.md                 # You're reading this
```

> ⚠️ **All four files must be in the same folder** for the site to work correctly. The HTML references the video and images by filename.

---

## ✨ Features

### 🎨 Design
- Warm tan/caramel + dark espresso colour palette inspired by premium café UI
- **Fraunces** serif for headlines, **Inter** for body — Google Fonts, loaded automatically
- Highlighter-style keyword accents (the `Creativity`, `Coffee` pill effect)
- Glassmorphism cards and circular masked photography throughout
- Fully responsive across desktop, tablet, and mobile
- Dark/light mode toggle

### 🎬 Animations & Interactions
- Cinematic loader with progress bar and percentage counter
- Custom gold cursor with magnetic follower
- Staggered hero text reveal on load
- Scroll-triggered section reveals with stagger delays
- Magnetic button effect (buttons subtly follow the cursor)
- Infinite gold marquee ticker (pauses on hover)
- Floating card animation on hero
- Rotating dashed badge stamp (About section)
- Hover parallax on product circle images
- Smooth scroll navigation

### 📋 Sections (12 total)
| # | Section | Description |
|---|---------|-------------|
| 1 | **Hero** | Full-screen with circular coffee photo, badge stamp, floating card |
| 2 | **Marquee** | Infinite scrolling café keywords ticker |
| 3 | **About** | Brand story, barista photo, rotating stamp, feature list |
| 4 | **Menu** | 4 circular product cards with hover reveal — Crafted With Intention |
| 5 | **Flavours** | 4-card colour grid — A Colour for Every Coffee |
| 6 | **Process** | 4-step bean-to-cup journey cards |
| 7 | **Journey** | Timeline + photo grid — HARS history since 2019 |
| 8 | **Testimonials** | 3 review cards with real avatar photos |
| 9 | **Memberships** | 3-tier pricing — Connoisseur / Reserve / Atelier |
| 10 | **FAQ** | Animated accordion — 5 questions |
| 11 | **Contact** | Reservation form + Google Map embed + photo thumbnails |
| 12 | **Footer** | Navigation, newsletter signup, social links |

---

## 📅 Reservation System

The contact form is fully functional with **zero backend required** — all data is stored in the browser's `localStorage`.

### How it works
1. User fills in Name, Phone, Date, Guests (required) + Email, Special Requests (optional)
2. Live validation runs as they type — red error messages for invalid fields
3. On submit, a **unique Reservation ID** is generated (e.g. `HRS-LX4K2M`)
4. Data is saved to `localStorage` instantly — survives page refresh
5. A success modal pops up with booking confirmation details

### Owner Dashboard
Click **"📋 View All Reservations"** below the form to open the dashboard:
- Full table: ID · Name · Phone · Date · Guests · Email · Status
- Message preview per entry
- Individual row delete (✕ button)
- **Clear All** to reset
- Live count badge

### Data structure (per reservation)
```json
{
  "id": "HRS-LX4K2M",
  "name": "Arjun Rao",
  "phone": "+91 98765 43210",
  "date": "2026-07-15",
  "guests": "3",
  "email": "arjun@email.com",
  "message": "Window seat if possible",
  "status": "Confirmed",
  "created": "2026-07-04T10:32:00.000Z"
}
```

> 💡 To export reservations: open browser DevTools → Application → Local Storage → copy the `hars_reservations` key value.

---

## 🖼️ Images & Media

| Asset | Source | Used In |
|-------|--------|---------|
| `hars-bg.mp4` | Your upload | Hero circle, About circle, Experience panel |
| `golden-latte.png` | Your photo | Flavours — Golden Latte card |
| `kyoto-pour-over.png` | Your photo | Flavours — Kyoto Pour Over card |
| Frappuccino | Unsplash (`1572442388796`) | Menu card |
| Caramel Macchiato | Unsplash (`1534040385115`) | Menu card |
| Café Mocha | Unsplash (`1495474472287`) | Menu card |
| Turkish Coffee | Unsplash (`1514432324607`) | Menu card |
| Cold Brew | Unsplash (`1461023058943`) | Flavours card |
| Espresso | Unsplash (`1510591509098`) | Flavours card |
| Hero main | Unsplash (`1447933601403`) | Hero circle |
| About barista | Unsplash (`1509042239860`) | About circle |

> All Unsplash images load directly from `images.unsplash.com` CDN — no download needed.

---

## 🚀 Getting Started

### Option 1 — Open locally
```bash
# Clone or download the repo
git clone https://github.com/yourusername/hars-coffee.git
cd hars-coffee

# Just open the HTML file
open hars-coffee-warm.html
# or double-click it in Finder / File Explorer
```

### Option 2 — GitHub Pages (free hosting)
1. Push all 4 files to a GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)`
4. Your site will be live at `https://yourusername.github.io/hars-coffee/hars-coffee-warm.html`

### Option 3 — Netlify (recommended, free)
1. Drag and drop the folder at [netlify.com/drop](https://netlify.com/drop)
2. Done. Live URL in 30 seconds.

---

## 🛠️ Customisation Guide

### Change the shop address / phone
Search for `Shahupuri` and `98765 43210` in the HTML and replace with your actual details.

### Replace the background video
Swap `hars-bg.mp4` with your own `.mp4` file — keep the same filename, or update the `<source src="">` tags in the HTML (there are 5 of them).

### Replace product images
Find the `<img src="...">` tag next to the menu item name you want to change and point it to your own image file or URL.

### Update menu prices
Search for `₹171`, `₹87`, etc. and change to your actual prices.

### Update colours
All colours are CSS variables at the top of the `<style>` block:
```css
:root {
  --tan: #C4923A;          /* Primary caramel accent */
  --tan-bg: #C9A256;       /* Main background */
  --espresso: #2A1B0E;     /* Dark sections + text */
  --cream: #FAF4E8;        /* Light text + card bg */
}
```

### Add more menu items
Copy any `.menu-card` block and paste it into the `.menu-grid` div. The grid auto-adjusts.

---

## 📦 Dependencies

None. Zero. Everything is vanilla.

| Technology | Version | Usage |
|-----------|---------|-------|
| HTML5 | — | Structure |
| CSS3 | — | Animations, layout, variables |
| JavaScript ES6+ | — | Interactions, localStorage |
| Google Fonts | CDN | Fraunces + Inter typefaces |
| Unsplash CDN | Free | Stock coffee photography |
| Google Maps Embed | Free | Kolhapur map in contact section |

---

## 🌐 Browser Support

| Browser | Support |
|---------|---------|
| Chrome 90+ | ✅ Full |
| Firefox 88+ | ✅ Full |
| Safari 14+ | ✅ Full |
| Edge 90+ | ✅ Full |
| Mobile Chrome | ✅ Full |
| Mobile Safari | ✅ Full |

> The custom cursor is hidden on touch devices automatically.

---

## 📍 Business Details (Update These)

```
Name:     HARS Coffee
Location: Kolhapur, Maharashtra, India
Address:  12, Station Road, Shahupuri, Kolhapur 416001
Phone:    +91 98765 43210
Email:    hello@harscoffee.in
Hours:    Mon–Fri 8am–8pm · Sat–Sun 8am–9pm
WhatsApp: https://wa.me/919876543210
```

---

## 📄 License

This project is for personal/commercial use by **HARS Coffee, Kolhapur**. 
Stock photography sourced from [Unsplash](https://unsplash.com) under the [Unsplash License](https://unsplash.com/license).

---

<div align="center">

Made with ☕ for **HARS Coffee · Kolhapur**

*Est. 2019 — Where Every Sip Becomes Art*

</div>
