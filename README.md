# Patent Drafting App by Subin Khullar

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Hosted_with-GitHub_Pages-222222.svg?logo=github)](https://pages.github.com/)
[![Pure Vanilla JS](https://img.shields.io/badge/Stack-HTML5%20%7C%20CSS3%20%7C%20Vanilla%20JS-yellow.svg)](#)

> A lightweight, browser-based, client-side US Patent Application drafting suite inspired by the document workflow of MS Word and the schematic drawing tools of MS PowerPoint. Designed with built-in 35 U.S.C. § 112 consistency checking, antecedent tracking, and drawing numeral synchronisation.

---

## 🌟 Key Features

### 📄 Specification Drafting (MS Word Style)
- **Standardised Patent Sections:** Formatted fields for Title of the Invention, Technical Field, Abstract, and Detailed Description.
- **Reference Numeral Tracker:** Live extraction of part-numeral pairings (e.g., `processor 102`) directly from the specification into a dynamic parts ledger.
- **1-Click Text Inserter:** Quickly inject elements and reference numerals directly into draft text at the cursor position.

### ⚖️ Claims Manager & Logic Engine
- **Tree & Hierarchy Builder:** Add and manage independent and dependent claims seamlessly.
- **Dynamic Dependency Tracking:** Maintain clean parent-child claim references with dropdown-driven dependencies.
- **Claim Categorisation:** Tag claims by statutory classes (Apparatus/System vs. Method/Process).

### 📐 Patent Figures & Schematics (MS PPT Style)
- **Vector Canvas:** Native `<canvas>` tools for drawing blocks/rectangles, circular nodes, connector lines, and text/lead lines.
- **USPTO-Compliant Standards:** Monochromatic black-and-white vector aesthetics with clear text callouts.
- **Instant Export:** Export drawing sheets as high-resolution `.png` files suitable for drawing sheet submissions.

### 🔍 Automated Consistency & Quality Checks
Run modular or comprehensive audits with a single click:
1. **Antecedent Basis Check (35 U.S.C. § 112(b)):** Flags elements introduced with *"the [element]"* or *"said [element]"* without a preceding indefinite article (*"a [element]"* or *"an [element]"*) in the claim or its dependency tree.
2. **Claim Hierarchy & Category Validation:** Catches circular dependencies, forward dependencies, and claim type mismatches (e.g., apparatus claim depending on a method claim).
3. **Specification & Drawing Numeral Cross-Check:** Verifies that all numerals defined in the Ledger are properly discussed in the Detailed Description and illustrated in the figure canvas.

### 🔒 100% Client-Side & Private
- **Zero Server Uploads:** Your legal drafts, inventions, and claims never leave your browser.
- **Portable Project Files:** Save and load your complete drafting sessions as `.patent` (JSON) files.
- **PDF Export:** Ready for print formatting and PDF export via your browser's print dialog (`Ctrl + P` / `Cmd + P`).

---

## 🚀 Live Demo

Try the live tool on GitHub Pages:  
👉 **`https://<your-username>.github.io/<your-repository-name>/`**  
*(Replace `<your-username>` and `<your-repository-name>` with your actual repository details)*

---

## 📂 Repository Structure

```text
├── index.html        # Core application shell: UI layout, Word/PPT engines, claims logic, and audit tools
├── manifest.json     # PWA configuration: enables standalone desktop/mobile installation & app styling
├── service-worker.js # Offline cache controller: stores application assets locally for zero-latency, offline use
├── README.md         # Comprehensive project documentation, feature walkthroughs, and deployment steps
└── LICENSE           # MIT open-source software license
