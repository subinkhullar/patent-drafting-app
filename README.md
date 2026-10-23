# Patent Drafting App by Subin Khullar

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/Hosted_with-GitHub_Pages-222222.svg?logo=github)](https://pages.github.com/)
[![PWA Ready](https://img.shields.io/badge/PWA-Offline%20Ready-green.svg)](#)
[![USPTO Compliant](https://img.shields.io/badge/USPTO-37%20CFR%201.84%20%7C%20MPEP%20608.02-informational.svg)](#)
[![Statutory Coverage](https://img.shields.io/badge/Claims-Apparatus%20%7C%20Method%20%7C%20CPP%20%7C%20Chemistry-purple.svg)](#)

> A client-side, browser-based US Patent Application drafting suite combining the structured text processing of **MS Word** with the vector schematic features of **MS PowerPoint**. Built-in with 35 U.S.C. § 112 consistency checking, antecedent tracking, page overflow auto-balancing, multi-figure vector studio with USPTO margin guides, specialized chemistry and computer program product (CPP) claim support, and native `.docx` & multi-page PDF exports.

---

## 🌟 Key Features

### 📄 Specification Drafting (MS Word Style)
- **Multi-Page Layout with Overflow Detection:** Paginated Letter-sized (`8.5" x 11"`) sheets with drop shadows, page numbering (`Page X of Y`), and real-time vertical overflow detection.
- **Dynamic Page Insertion & Splitting:**
  - Insert pages anywhere using **"📄 Insert Page Below"** or append via **"📄 + Insert Page at End"**.
  - Visual warning (`⚠️ Text exceeds printable page limit!`) with a **"Split to Next Page"** button when content overflows.
  - One-click **"⚖️ Auto-Balance Overflowing Pages"** to cleanly distribute text across pages.
- **Editable Standard Sections:** Title of the Invention, Technical Field, **Summary of the Invention**, Abstract of the Disclosure, Brief Description of the Drawings, and Detailed Description. All section headers are directly editable.
- **Typography & Formatting:** Real-time font switching (Times New Roman, Arial, Courier New, Georgia, Calibri), font size adjustment (10pt–14pt), and inline formatting (**B**, *I*, <u>U</u>).
- **🟡 Dynamic Claim Term Highlighting:** One-click toggle to highlight tracked elements and introduced claim terms simultaneously across the entire specification and claims tree.
- **Auto-Sync Numeral Extraction:** Type component-numeral pairs (e.g., `memory storage 106`) to auto-populate the active Reference Parts Ledger.
- **Native `.docx` Export:** Generates an MS Word document complete with all custom headers, formatted paragraphs, and all **Claims automatically appended at the end** under `"WHAT IS CLAIMED IS:"`.

---

### ⚖️ Claims Manager (Apparatus, Method, CPP, & Chemistry)
- **Multi-Category Statutory Coverage:** Dedicated claim creation buttons and dependency management for:
  - **Apparatus / System Claims**
  - **Method / Process Claims**
  - **Computer Program Product (CPP / CRM) Claims:** Pre-configured 35 U.S.C. § 101 / *Alice*-compliant Non-Transitory Computer-Readable Storage Medium templates.
  - **Chemical Composition Claims:** Markush grouping templates (*"selected from the group consisting of..."*), weight percentages (`wt%`), active ingredients, carriers, and excipients.
- **Context-Aware Dependent Claims:** Clicking **"+ Dependent Claim"** automatically inherits the correct statutory class and dependency preamble (e.g., *"The non-transitory computer-readable storage medium of claim X..."* or *"The composition of claim X..."*).
- **Interactive Hierarchy Tree:** Easily reorder, modify dependencies, adjust categories, or delete claims on the fly.

---

### 📐 Multi-Figure Drawing Studio (MS PowerPoint Style)
- **Tabbed Figure Sheets:** Add, duplicate, switch, and delete multiple figure sheets (`FIG. 1`, `FIG. 2`, etc.), each preserving its own vector layer.
- **USPTO 37 CFR § 1.84 & MPEP § 608.02 Margin Compliance:**
  - Standard US Letter (`8.5" x 11"`) canvas rendered with non-printing dashed guidelines.
  - Enforces minimum margin boundaries: **Top: 1.0"**, **Left: 1.0"**, **Right: 0.625" (5/8")**, and **Bottom: 0.375" (3/8")**.
  - Automatically renders centered figure headings and sheet numbering (`Sheet X of Y`) inside the usable sight area.
- **Rich Vector Toolkit:**
  - **Shapes & Flowcharts:** Process rectangles, rounded boxes, circular terminals, decision diamonds, and database/storage cylinders.
  - **Lines & Connectors:** Orthogonal connector lines, directional signal arrows, dotted electrical lines, and callout leaders.
  - **Interactive Transform Controls:** Move, position, and resize shapes using corner bounding handles.
  - **Freehand Sketching:** Smooth free-drawing mode for custom mechanical contours and sketches.
  - **Standard Patent Icon Gallery:** One-click insertion for Electrical Ground, RF Antenna, Resistor, Switch, CPU / Microprocessor, Cloud Network, and Sensor.
- **Multi-Page Drawing PDF Export:** Compiles all figure sheets into a single, unified vector PDF (`letter` portrait) ready for filing.

---

### 🔍 Automated Consistency & Quality Checks
Run modular audits or a comprehensive review with a single click:
1. **Antecedent Basis Audit (35 U.S.C. § 112(b)):** Flags elements introduced with *"the"* or *"said"* without preceding indefinite introduction (*"a"* or *"an"*). Features smart exceptions for IUPAC nomenclature, chemical terms (`wt%`, `pH`, solvent mixtures), and CPP boilerplate (`processor`, `instructions`, `operations`).
2. **Claim Hierarchy & Category Audit:** Catches circular references, forward dependencies, and cross-category conflicts (e.g., apparatus claim depending on a chemical composition claim).
3. **Specification, Drawing & Overflow Audit:** Verifies that all numerals defined in the Ledger are cited in the specification and visible on drawing sheets, while flagging any pages that exceed physical print margins.

---

### 🔒 100% Client-Side, Private & Offline (PWA)
- **Zero Server Uploads:** Your confidential drafts, invention disclosures, and claims never leave your browser sandbox.
- **Progressive Web App (PWA):** Installable as a native desktop or mobile application via Chrome, Edge, Safari, or Firefox.
- **Service Worker Caching:** Fully operational without an active internet connection.
- **Portable Project Files:** Save and resume complete drafting sessions anytime via local `.patent` JSON state files.

---

## 📂 Repository Structure

```text
├── index.html        # Unified application shell: multi-page Word editor, PPT canvas, claims validator, and audit engine
├── manifest.json     # Web app manifest: enables standalone desktop/mobile installation with vector icon assets
├── service-worker.js # Cache-first service worker: provides full offline drafting support
├── README.md         # Comprehensive documentation and deployment guide
└── LICENSE           # MIT open-source license