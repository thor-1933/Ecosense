<div align="center">

<img src="https://img.shields.io/badge/EcoSense-Know%20Your%20Footprint-00E5A0?style=for-the-badge&logoColor=white" alt="EcoSense"/>

# 🌿 EcoSense — Personal Carbon Intelligence Dashboard

**Know your footprint. Own your impact.**

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-thor--1933.github.io%2FEcosense-00E5A0?style=flat-square)](https://thor-1933.github.io/Ecosense/)
[![HTML](https://img.shields.io/badge/HTML5-Single%20File-E34F26?style=flat-square&logo=html5&logoColor=white)](https://github.com/thor-1933/Ecosense)
[![CSS](https://img.shields.io/badge/CSS3-Custom%20Design%20Tokens-1572B6?style=flat-square&logo=css3&logoColor=white)](https://github.com/thor-1933/Ecosense)
[![JavaScript](https://img.shields.io/badge/JavaScript-Vanilla%20ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://github.com/thor-1933/Ecosense)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![No Tracking](https://img.shields.io/badge/🔒%20Privacy-Zero%20Tracking-00E5A0?style=flat-square)](https://thor-1933.github.io/Ecosense/)

<br/>

> A free, private, zero-tracking carbon footprint calculator that gives you a personalised Carbon Score, compares you against India and global averages, and shows you exactly where to start reducing — all in a single, beautifully designed HTML file.

<br/>

![EcoSense Screenshot](https://thor-1933.github.io/Ecosense/preview.png)

</div>

---

## ✨ Why EcoSense?

Most carbon calculators are slow, clunky, require sign-ups, or bury you in ads. EcoSense was built as the opposite: a **single-file, instant, privacy-first** experience that respects your time and your data.

Fill in four inputs. Hit calculate. Get your number, your score, your rank against global benchmarks, and a concrete action plan — in under 10 seconds.

---

## 🚀 Features

### 🧮 Carbon Footprint Calculator
Input four lifestyle factors and get your estimated annual CO₂ footprint in kilograms:
- **Transport** — Car, Motorbike, Bus, Train, or Walk/Cycle
- **Diet** — Vegan, Vegetarian, Mixed, or Meat-heavy
- **Home Energy** — Low / Medium / High usage slider
- **Shopping & Consumption** — Minimal / Medium / Heavy slider

Real-time per-category estimates update as you adjust each input, so you can see the impact before you even click Calculate.

### 📊 Carbon Score (0–100)
Every result comes with a **Carbon Score** — a simple 0-to-100 metric where higher means greener. Color-coded as green, amber, or red, it gives you an at-a-glance read of your environmental standing without needing to interpret raw numbers.

### 🌍 Benchmarked Against Real Averages
Your result is automatically compared to:
- 🇮🇳 **India Average** — 1,900 kg CO₂/year
- 🌎 **Global Average** — 4,700 kg CO₂/year

An animated SVG ring chart shows all three figures simultaneously, making comparisons intuitive at a glance.

### 🌳 Real-World Equivalents
Numbers become meaningful when you see that your footprint equals:
- 🌳 X trees needed to offset it annually
- ✈️ Y long-haul flights worth of emissions
- 🥩 Z beef meals equivalent
- ⚡ N months of average Indian household electricity

### 💡 Personalised Reduction Tips
EcoSense identifies your **highest-emission category** and surfaces the top 3 most impactful tips specific to that area — not generic advice, but targeted actions ranked by estimated CO₂ savings.

### 🔥 Challenge Arena (Leaderboard)
Compete with friends, family, or colleagues in real time. Add your name to the **Arena**, and the leaderboard ranks everyone by CO₂ — lowest footprint wins. A built-in **Copy Challenge** button lets you share a pre-written challenge message to LinkedIn or WhatsApp in one tap.

### ⚡ Memoized Calculations
Results are cached using a `Map`-based memoization layer. If you re-calculate the same combination of inputs, the result is returned **instantly** with a badge confirming it came from cache — no redundant computation.

### 📋 One-Click Share
A pre-formatted share text is auto-generated with your score and key stats, ready to paste into LinkedIn, Twitter, or any social platform to inspire others.

### 🧪 Built-in Test Suite
Hit "Run Tests" in the footer to execute an inline unit test suite that validates the core calculation engine — right inside the browser, no build tools needed.

---

## 🛡️ Privacy First

> **No data leaves your device. Ever.**

- ❌ No accounts, no sign-ups
- ❌ No cookies, no analytics, no trackers
- ❌ No server calls (except Google Fonts, which can be self-hosted)
- ✅ All calculations run entirely in your browser
- ✅ Page refresh resets everything — nothing is stored

---

## 🏗️ Tech Stack

EcoSense is deliberately dependency-free.

| Layer | Approach |
|---|---|
| **Structure** | Semantic HTML5 with ARIA attributes for full accessibility |
| **Styling** | Pure CSS with a CSS custom properties (design token) system |
| **Logic** | Vanilla JavaScript ES6+ — no frameworks, no bundlers |
| **Fonts** | Space Grotesk (headings) + Inter (body) via Google Fonts |
| **Charts** | Hand-crafted SVG ring chart with CSS animations |
| **Deployment** | GitHub Pages — static hosting, zero configuration |

The entire app ships as **one `.html` file** — open it offline, host it anywhere, fork it instantly.

---

## 📐 How the Calculations Work

Emissions are computed from peer-reviewed emission factor estimates:

```
Total CO₂ = Transport Emissions + Diet Emissions + Energy Emissions + Shopping Emissions
```

| Category | Factor Source |
|---|---|
| Car | ~0.171 kg CO₂ per km (petrol) |
| Diet | Vegan: 1,500 kg → Meat-heavy: 3,300 kg per year |
| Home Energy | Low: 600 kg → High: 1,800 kg per year |
| Shopping | Minimal: 200 kg → Heavy: 1,400 kg per year |

Reference benchmarks: India average 1,900 kg/yr · Global average 4,700 kg/yr (IEA / World Bank estimates).

Carbon Score formula:
```
Score = max(0, 100 - round((userTotal / globalAverage) × 50))
```

---

## 🖥️ Getting Started

No install. No `npm install`. No build step.

**Option 1 — View live:**
👉 [https://thor-1933.github.io/Ecosense/](https://thor-1933.github.io/Ecosense/)

**Option 2 — Run locally:**
```bash
git clone https://github.com/thor-1933/Ecosense.git
cd Ecosense
# Open index.html in any browser
open index.html
```

**Option 3 — Fork & deploy your own:**
```bash
# Fork the repo on GitHub, then enable GitHub Pages
# Settings → Pages → Source: main branch / root
# Your copy will be live at: https://<your-username>.github.io/Ecosense/
```

---

## 📁 Project Structure

```
Ecosense/
└── index.html        ← The entire application (HTML + CSS + JS in one file)
```

That's it. No `node_modules`, no `package.json`, no build artifacts.

---

## ♿ Accessibility

EcoSense was built with accessibility as a first-class concern:

- Skip-to-content link for keyboard users
- All interactive elements have `aria-label` or `aria-live` attributes
- Radio buttons use proper `fieldset`/`legend` semantics
- SVG chart includes `<title>` and `role="img"`
- Full `:focus-visible` keyboard navigation styling
- Screen-reader-only labels via `.sr-only` utility class

---

## 🗺️ Roadmap

- [ ] Flight emissions calculator (air travel tab)
- [ ] Monthly vs annual toggle
- [ ] Offset recommendations with third-party links
- [ ] PWA support for offline use
- [ ] Dark/light theme toggle
- [ ] Shareable result card image (Canvas API)

---

## 🤝 Contributing

Contributions, bug reports, and feature ideas are welcome!

1. Fork the repository
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

For significant changes, please open an issue first to discuss what you'd like to change.

---

## 📜 License

This project is licensed under the **MIT License** — free to use, fork, modify, and distribute.

---

<div align="center">

Built with 💚 for a greener planet · **[Live Demo →](https://thor-1933.github.io/Ecosense/)**

*If EcoSense made you think about your footprint, give it a ⭐ — it helps others find it too.*

</div>
