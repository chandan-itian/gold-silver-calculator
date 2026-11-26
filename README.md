# Gold & Silver Live Bullion and Jewellery Bill Calculator (India)

**गोल्ड और सिल्वर लाइव बुलियन एवं ज्वैलरी बिल कैलकुलेटर (भारत)**

A clean, mobile-friendly, single-page web app that converts live international gold and silver spot prices into Indian bullion rates and builds a complete, transparent jewellery bill — metal value, import duty, making charges and GST — step by step.

🔗 **Live Demo:** https://chandan-itian.github.io/gold-silver-calculator/

---

## ✨ What it does

- **Live spot prices** — fetches live gold (XAU) and silver (XAG) spot prices in USD per troy ounce, and the live USD → INR rate, with automatic refresh every 60 seconds.
- **India landed rates** — converts the international spot into Indian rates per gram and per 10 grams, including import duty and GST.
- **Purity-wise rates** — one-click rate cards for gold **24K / 22K / 18K** and silver **999 / 925 / 800**, with and without GST.
- **Jewellery bill calculator** — enter the net weight, choose making charges (percentage or flat ₹/gram), and get a full receipt-style bill: metal value, making charge, taxable value, GST and final payable amount, with a visual breakdown bar.
- **Two GST modes** — ready-made jewellery (3% GST on the whole bill) and job-work (3% GST on metal + 5% GST on making charges), so there is no double GST.
- **City benchmarks** — Patna (Bihar) and Delhi benchmark rates for 24K / 22K / 18K, so you can compare the calculated rate with the local market.
- **Beginner guide** — built-in explanations of troy ounce, purity standards, BIS hallmarks (916 for 22K, 750 for 18K), import duty and GST rules.
- **Dark mode** — one-click light/dark theme, with all settings remembered in the browser.

---

## 🧮 How the calculation works

All calculations are done live in the browser — no server, no sign-up, no data leaves your device.

| Step | Formula |
| --- | --- |
| INR per troy ounce | Spot (USD/oz) × USD → INR rate |
| Pure base rate per gram | INR per troy ounce ÷ **31.1035** (1 troy ounce = 31.1035 g) |
| India rate (ex-GST) | Base rate × (1 + **15%** import duty) |
| India rate (incl. GST) | Ex-GST rate × (1 + **3%** GST) |
| 22K rate | 24K rate × (22 ÷ 24) = × **0.9167** |
| 18K rate | 24K rate × (18 ÷ 24) = × **0.7500** |
| Silver 925 | Fine silver rate × **0.925** |
| Metal value | Selected purity rate × net weight (g) |
| Making charge | Metal value × making % **or** flat ₹/gram × weight |
| GST (ready-made) | 3% on (metal value + making charge) |
| GST (job-work) | 3% on metal value + 5% on making charge |
| **Final payable** | **Metal value + making charge + GST** |

**Import duty (India, from 13 May 2026):** 15% total — 10% Basic Customs Duty (BCD) + 5% Agriculture Infrastructure Development Cess (AIDC).

---

## 🛠️ Built with

| Technology | Used for |
| --- | --- |
| **HTML5** | Page structure and semantic layout |
| **CSS3** | Responsive design, dark mode, sliders and receipt UI (no CSS framework) |
| **Vanilla JavaScript** | All calculations, live API sync, sliders, theme and bill logic — no JS framework |
| **Google Fonts** | Inter (numbers/Latin) + Noto Sans Devanagari (Hindi text) |
| **Gold-API.com** | Live XAU / XAG spot prices (USD/oz) |
| **ExchangeRate-API / Frankfurter** | Live USD → INR exchange rate |
| **Kitco** | Reference source for spot prices |
| **GitHub Pages** | Free hosting for the live site |

No build step, no backend, no database — the whole app is a single `index.html` file.

---

## 📁 Project structure

```
gold-silver-calculator/
├── index.html   # The complete app — HTML, CSS and JavaScript in one file
└── README.md    # This file
```

---

## ▶️ Run it locally

Just open the file in any modern browser — no server needed:

```bash
git clone https://github.com/chandan-itian/gold-silver-calculator.git
cd gold-silver-calculator
# Open index.html in your browser
```

Or serve it locally (optional):

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

---

## ⚠️ Disclaimer

Rates shown are indicative and based on live international spot prices plus the duty/GST rules above. Actual jeweller prices vary by city, shop, making charges and daily market movement (typically ₹50–₹150/gram local premium). Always confirm the final price with your jeweller before buying.

---

## 👤 Author

**Chandan Raj** ([@chandan-itian](https://github.com/chandan-itian))

Made for buyers and learners in India who want to understand exactly how a gold or silver jewellery bill is calculated.

---

<p align="center"><strong>Made with love ❤️ by Chandan Raj</strong></p>
