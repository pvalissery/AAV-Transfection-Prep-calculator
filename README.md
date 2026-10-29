# Viral Vector Transfection Calculator 🧫

**TL;DR:** A zero-dependency, browser-based calculator for viral vector production (AAV/Lentivirus). It handles the math for multi-plasmid transfections, PEI ratios, and OptiMEM volumes across different dish sizes so you don't have to. 

Try it live here: [Insert your GitHub Pages link here]

## Why build this?
If you've spent any time in a wet lab doing viral production, you know the drill: someone passes down a legacy Excel sheet (in my case, `PV_AAV6_production.xlsx`), you change one cell, accidentally break a hidden formula, and suddenly your PEI-to-DNA ratio is completely off. 

I built this to take the math out of the hood. It ports the logic of standard vector production spreadsheets into a clean, foolproof web UI. It handles the stoichiometry for packaging plasmids (like psPAX2 and pMD2.G) alongside various transfer plasmids (mR-CD55, BSG-mNG, etc.) without the risk of overwriting a cell. 

## Features
*   **Scale on the Fly:** Instantly toggle calculations between standard 6 ml and 10 ml culture dishes, or scale up to multi-dish batches.
*   **Dynamic Ratios:** Automatically calculates the exact volumes (in µl) and masses (in ng) for your Donor/Transfer DNA, Envelope, and Packaging plasmids based on your specific construct.
*   **PEI & OptiMEM Optimization:** Standardized calculations for total culture volume, keeping PEI and OptiMEM ratios tight for maximum transfection efficiency.
*   **Client-Side Only:** No backend, no servers, no data collection. It runs entirely in your browser using Vanilla JavaScript. 
*   **Bench-Friendly UI:** Built with a high-contrast, responsive Tailwind CSS layout so you can easily read the numbers off your phone or a lab tablet while wearing gloves.

## Under the Hood
This is a static web app. No build steps or heavy frameworks required.
*   **HTML5 / Vanilla JS:** Core logic and DOM manipulation.
*   **Tailwind CSS:** For the styling via CDN (keeps the repo lightweight).

## Usage
Since it's completely client-side, you can just click the GitHub Pages link to use it immediately. 

If you want to run it locally or tweak the baseline plasmid concentrations:
1. Clone the repo: `git clone https://github.com/yourusername/aav-calculator.git`
2. Open `index.html` in any modern web browser.
3. Edit the JS variables in the `<script>` tag if you need to adjust stock concentrations or add new constructs.

## Contributing
If you have a different transfection reagent protocol (e.g., Lipofectamine instead of PEI) or want to add AAV-specific helper plasmid ratios (like pHelper/RepCap), feel free to open a PR or fork it for your own lab's specific protocols.