# Patent Drafting App by Subin Khullar

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Hosted_with-GitHub_Pages-222222.svg?logo=github)](https://pages.github.com/)
[![PWA Ready](https://img.shields.io/badge/PWA-Offline%20Ready-green.svg)](#)
[![USPTO Compliant](https://img.shields.io/badge/USPTO-37%20CFR%201.84%20%7C%20MPEP%20608.02-informational.svg)](#)

> A client-side, browser-based US Patent Application drafting studio combining the text editing precision of **MS Word** with the vector schematic features of **MS PowerPoint**. Built-in with 35 U.S.C. § 112 consistency checking, antecedent tracking, USPTO drawing margin guidelines, multi-figure sheets, and native `.docx` & multi-page PDF exports.

---

## 🌟 Key Features

### 📄 Multi-Page Specification Drafting (MS Word Style)
- **Multi-Page Layout:** Letter-sized (`8.5" x 11"`) paginated pages with real-time drop shadows, custom headers, footers, and dynamic page counters (`Page X of Y`).
- **Editable Standard Sections:** Title of the Invention, Technical Field, **Summary of the Invention**, Abstract, Brief Description of the Drawings, and Detailed Description. You can edit any header on the fly.
- **Font & Style Controls:** Change typography on demand (Times New Roman, Arial, Courier New, Georgia, Calibri), select font size, and apply bold/italic/underline styling.
- **🟡 Dynamic Claim Term Highlighting:** 1-click toggle to highlight all tracked elements and claim terms simultaneously across the specification and claims.
- **Auto-Sync Numeral Extraction:** Type elements (e.g. `memory storage 106`) to automatically populate the Parts Ledger.
- **Native `.docx` Export:** Export the entire specification as an MS Word document with custom headers and all **Claims automatically appended at the end** in legal patent format.

### 📐 Multi-Figure Drawing Studio (MS PowerPoint Style)
- **Tabbed Figure Sheets:** Add, duplicate, switch, and delete multiple figures (`FIG. 1`, `FIG. 2`, etc.).
- **USPTO 37 CFR § 1.84 & MPEP § 608.02 Margin Compliance:**
  - Standard US Letter (`8.5" x 11"`) canvas with non-printing dashed guidelines.
  - Enforces minimum margins: **Top: 1.0"**, **Left: 1.0"**, **Right: 0.625" (5/8")**, and **Bottom: 0.375" (3/8")**.
  - Automatic centering of figure titles and sheet numbering (`Sheet X of Y`) inside the usable sight area.
- **Rich Vector Drawing Toolkit:**
  - **Shapes:** Rectangles, rounded boxes, circles/nodes, flowchart diamonds (decisions), and storage cylinders (databases).
  - **Lines & Connectors:** Orthogonal lines, directional signal arrows, dotted electrical lines, and callout leaders.
  - **Selection, Movement & Resizing:** Click to select shapes, drag to reposition, and scale dynamically using corner bounding handles.
  - **Freehand Sketching:** Smooth free-style drawing tool for custom mechanical profiles and organic contours.
  - **Standard Patent Icon Gallery:** 1-click insertion for Ground, Antenna, Resistor, Switch, CPU/Processor, Cloud Network, and Sensor.
- **Export All Figures as Unified PDF:** Generates a compiled, multi-page vector PDF containing all drawing sheets ready for patent filing.

### ⚖️ Claims Manager & Logic Engine
- **Tree & Hierarchy Builder:** Add and manage independent and dependent claims.
- **Dynamic Dependency Tracking:** Dropdown-driven dependencies with automatic parent-child validation.
- **Statutory Categories:** Classify claims by Apparatus/System vs. Method/Process.

### 🔍 Automated Consistency & Quality Checks
1. **Antecedent Basis Check (35 U.S.C. § 112(b)):** Flags elements introduced with *"the"* or *"said"* without preceding introduction via *"a"* or *"an"* across current and parent claims.
2. **Claim Hierarchy & Category Validation:** Catches circular references, forward dependencies, and claim type mismatches (e.g., apparatus claim depending on a method claim).
3. **Specification & Drawing Numeral Cross-Check:** Verifies that all numerals defined in the Ledger are cited in the Detailed Description and visible on the drawing sheets.

### 🔒 100% Client-Side & Offline PWA
- **Zero Server Uploads:** Your drafts and invention disclosures never leave your machine.
- **Installable PWA:** Install as a native desktop or mobile app via your browser's install button.
- **Portable Sessions:** Save and resume your work with local `.patent` JSON session files.

---

## 📂 Repository Structure

```text
├── index.html        # Core application: Multi-page editor, PowerPoint canvas, claims engine, and audit suite
├── manifest.json     # PWA manifest: Enables standalone app installation and vector branding
├── service-worker.js # Service worker: Cache-first engine enabling complete offline capability
├── README.md         # Comprehensive documentation and deployment guide
└── LICENSE           # MIT License

---

## 🛠️ Quick Deployment to GitHub Pages

1.	Fork or Clone this repository:
codeBash
```text
git clone https://github.com/<your-username>/<your-repository-name>.git

2.	In your repository on GitHub:
o	Navigate to Settings > Pages.
o	Under Build and deployment > Source, choose Deploy from a branch.
o	Under Branch, select main (or master) and / (root).
o	Click Save.

3.	Your drafting tool will be live in seconds at:
codeText
```text
https://<your-username>.github.io/<your-repository-name>/

---

## 📖 How to Use
1.	Set Up the Parts Ledger: Add primary components and numerals (e.g., controller 102, display 104) in the left sidebar.
2.	Draft the Specification: Edit sections on the multi-page canvas, adjust typography, or click 📄 + Add Spec Page to add pages. Click 🟡 Toggle Term Highlighting to check your element distribution.
3.	Build the Figures: Switch to the Figures & Drawing Studio (PPT) tab. Add tabs for FIG. 1, FIG. 2, etc. Draw block diagrams, flowchart decisions, and use the Patent Icons dropdown. Check that your drawings stay within the blue 37 CFR 1.84 margin guidelines.
4.	Draft Claims: Add independent and dependent claims in the Claims tab.
5.	Run Consistency Checks: Click ⚡ Run All Checks to identify missing antecedents, dependency logic issues, or omitted numerals.
6.	Export Your Filing Package:
o	Click 📥 Export Spec+Claims (.docx) for the complete written specification and claims.
o	Click 📑 Export All Figures as PDF for the USPTO-compliant drawing sheets.
o	Click 💾 Save Draft to keep a backup .patent state file.

---

## ⚖️ License
Distributed under the MIT License. See LICENSE for more information.

---

## 👤 Author
Subin Khullar
Patent Drafting App by Subin Khullar
