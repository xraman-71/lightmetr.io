# lightmetr.io
⚡ Free browser-based electricity bill calculator. Two tools: meter-reading &amp; appliance-based estimator. Live preview, PDF &amp; Excel export, 15 currencies. No login, no backend, no data stored. Pure HTML/CSS/JS.


# ⚡ ElectroCalc — Electricity Bill Generator Tools

> **Two free, browser-based electricity bill calculators. No backend. No login. No data stored.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Visit%20Site-5c3d2e?style=for-the-badge&logo=googlechrome&logoColor=white)](https://xraman-71.github.io/lightmetr.io/)
[![License](https://img.shields.io/badge/License-MIT-3d85a8?style=for-the-badge)](LICENSE)
[![HTML](https://img.shields.io/badge/Built%20With-HTML%2FCSS%2FJS-b8886a?style=for-the-badge&logo=html5&logoColor=white)](https://xraman-71.github.io/lightmetr.io/)
[![Zero Backend](https://img.shields.io/badge/Backend-None-2b5f7a?style=for-the-badge)](https://xraman-71.github.io/lightmetr.io/)

---

## 🔗 Live Demo

**→ [https://xraman-71.github.io/lightmetr.io/](https://xraman-71.github.io/lightmetr.io/)**

---

## 📖 Overview

**ElectroCalc** is a pair of purpose-built, frontend-only electricity bill estimation tools. Whether you have your meter readings on hand or just want to estimate costs by listing your appliances, ElectroCalc generates a professional, downloadable bill preview — entirely inside your browser.

No servers. No accounts. No data ever leaves your device.

---

## 🛠️ The Two Tools

### ⚡ Tool 1 — Meter-Based Electricity Bill Generator
[`electricity_bill_generator.html`](electricity_bill_generator.html)

Enter your **previous and current meter readings** to generate a complete bill with consumer details, itemized charges, and a professional PDF/Excel download.

**Key inputs:**
- Consumer name, meter number, location, billing month
- Previous & current kWh readings (units auto-calculated)
- Per-unit energy rate, fixed charge, other charges
- Tax/duty percentage
- Currency (15 supported)

---

### 🔌 Tool 2 — Appliance-Based Bill Estimator
[`appliance_bill_generator.html`](appliance_bill_generator.html)

Don't have meter readings? **Add your appliances individually** — enter wattage, quantity, daily usage hours, and days used. The tool rolls everything into a detailed, itemized bill.

**Key inputs:**
- Appliance name, wattage (W), quantity
- Hours used per day, number of days
- Per-unit rate, fixed charge, tax
- Currency (15 supported)

---

## ✨ Features

| Feature | Meter Tool | Appliance Tool |
|---|:---:|:---:|
| Live bill preview (real-time) | ✅ | ✅ |
| PDF download (A4 formatted) | ✅ | ✅ |
| Excel export | ✅ | ✅ |
| Print support | ✅ | ✅ |
| 15 international currencies | ✅ | ✅ |
| Fixed & other charges | ✅ | ✅ |
| Tax / duty (%) | ✅ | ✅ |
| Inline input validation | ✅ | ✅ |
| Per-appliance kWh breakdown | ❌ | ✅ |
| Meter number field | ✅ | ❌ |
| Pre-loaded sample appliances | ❌ | ✅ |
| Zero data stored/transmitted | ✅ | ✅ |
| Works offline (after load) | ✅ | ✅ |
| Mobile responsive | ✅ | ✅ |
| Auto-generated bill number & date | ✅ | ✅ |

---

## 🚀 Getting Started

### Option 1 — Use the Live Site
Open **[https://xraman-71.github.io/lightmetr.io/](https://xraman-71.github.io/lightmetr.io/)** in any modern browser. No installation required.

### Option 2 — Run Locally
```bash
# Clone the repository
git clone https://github.com/xraman-71/lightmetr.io.git

# Navigate into the folder
cd lightmetr.io

# Open the landing page directly in your browser
open index.html

# Or open individual tools
open electricity_bill_generator.html
open appliance_bill_generator.html
```

> No build step, no `npm install`, no dependencies to resolve. Just open and use.

---

## 🧮 Calculation Logic

### Meter-Based Tool
```
Units Consumed   = Current Reading − Previous Reading
Energy Charge    = Units × Per-Unit Rate
Subtotal         = Energy Charge + Fixed Charge + Other Charges
Tax Amount       = Subtotal × (Tax % / 100)
Total Payable    = Subtotal + Tax Amount
```

### Appliance-Based Tool
```
Per Appliance kWh = (Watts / 1000) × Hours/Day × Days × Quantity
Total kWh         = Sum of all appliance kWh values
Energy Charge     = Total kWh × Per-Unit Rate
Subtotal          = Energy Charge + Fixed Charge + Other Charges
Tax Amount        = Subtotal × (Tax % / 100)
Total Payable     = Subtotal + Tax Amount
```

---

## 🌍 Supported Currencies

| Symbol | Currency | Symbol | Currency |
|:---:|---|:---:|---|
| ₹ | Indian Rupee (INR) | $ | US Dollar (USD) |
| £ | British Pound (GBP) | € | Euro (EUR) |
| ¥ | Japanese Yen (JPY) | A$ | Australian Dollar (AUD) |
| C$ | Canadian Dollar (CAD) | AED | UAE Dirham |
| ৳ | Bangladeshi Taka (BDT) | ₨ | Pakistani Rupee (PKR) |
| RM | Malaysian Ringgit | ₦ | Nigerian Naira (NGN) |
| R | South African Rand (ZAR) | ฿ | Thai Baht (THB) |
| S$ | Singapore Dollar (SGD) | | |

---

## 👥 Who Is It For?

- 🏠 **Homeowners & Tenants** — Estimate bills before they arrive; identify energy-hungry appliances
- 🏢 **Small Business Owners** — Break down electricity costs by equipment and manage overheads
- 📊 **Accountants & Billing Staff** — Generate clean bill previews for records or client reporting
- 🎓 **Students & Educators** — Understand billing mechanics hands-on for coursework
- 🏗️ **Property Managers** — Quick utility cost estimates across multiple units
- ⚡ **Energy Consultants** — Demonstrate appliance load impact to clients on the fly

---

## ⚠️ Disclaimer

Bills generated by ElectroCalc are **for estimation and preview purposes only**. They are **not** official utility bills and carry no legal standing. ElectroCalc is not affiliated with any electricity distribution company, government utility board, or energy regulator.

Do not use generated documents as evidence of billing, payment, or debt in any legal, financial, or regulatory context.

---

## 🏗️ Tech Stack

```
├── HTML5          — Structure and semantic markup
├── CSS3           — Custom properties, Grid, Flexbox, responsive design
├── Vanilla JS     — All calculations and DOM manipulation
├── jsPDF v2.5.1   — Client-side A4 PDF generation (Cloudflare CDN)
├── SheetJS v0.18.5 — Client-side Excel (.xlsx) generation (Cloudflare CDN)
└── Google Fonts   — Playfair Display + DM Sans (requires internet)
```

**Architecture:** Each tool is a single self-contained `.html` file. No framework, no build system, no backend.

**Browser Support:** Chrome 100+, Firefox 100+, Safari 15+, Edge 100+

---

## 📁 File Structure

```
lightmetr.io/
├── index.html                      # Landing page (this site)
├── electricity_bill_generator.html # Tool 1 — Meter-based calculator
├── appliance_bill_generator.html   # Tool 2 — Appliance-based estimator
└── README.md
```

---

## 🔒 Privacy

- ✅ **Zero data collected** — nothing is ever sent to a server
- ✅ **No cookies** — no session or tracking data stored
- ✅ **No analytics** — no usage tracking of any kind
- ✅ **No login required** — anonymous by design
- ✅ **Works offline** — core functionality requires no internet after first load

All calculations, PDF generation, and Excel export happen entirely inside your browser's JavaScript engine.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).  
Free to use, modify, and distribute with attribution.

---

<div align="center">
  <strong>⚡ ElectroCalc</strong> — Free electricity bill estimation. No signup. No nonsense.<br/>
  <a href="https://xraman-71.github.io/lightmetr.io/">https://xraman-71.github.io/lightmetr.io/</a>
</div>
