# WSACA Tools

A growing collection of free, open-source tools developed by the **Washington State Association of County Assessors** to support our members and the homeowners we serve.

**[→ Visit the WSACA Tools site](https://mav2clu50.github.io/WSACA/)**

These tools are free to use. Any Washington county assessor's office is welcome to link to them directly, embed them on their own website, or adapt them for local needs.

---

## Why this exists

Modern infrastructure should be a shared resource across all 39 county assessor offices — not something every county has to build, license, or maintain on its own. Tools that one county needs are usually tools every county needs. WSACA builds them once, maintains them collectively, and makes them freely available.

The screening tool currently hosted here is the first WSACA tool. More will follow — appeal flowcharts, deferral estimators, whatever the assessor community decides to build together.

---

## Available Tools

### Property Tax Exemption Screening Tool

A guided screening tool that helps Washington homeowners check whether they may qualify for the expanded **Property Tax Exemption for Senior Citizens and People with Disabilities** under the program changes taking effect in tax year 2027.

The tool walks users through eligibility requirements, calculates an estimated combined disposable income using an abbreviated version of DOR's Form 63 0036, and returns a screening result tailored to their county's income thresholds.

**Two versions are available:**

- **[v2 (current)](https://mav2clu50.github.io/WSACA/v2/)** — The actively-maintained version. Includes a 2026-vs-2027 threshold comparison panel, an income spectrum visualization, a 5% buffer "you're close — please call your assessor" branch, A/B/C level labels paired with DOR's Threshold 1/2/3 terminology, click-to-reveal RCW citations throughout, a tailored "documents to bring" list generated from the applicant's actual inputs, and a printable result document that opens in a new browser tab.

- **[v1 (original)](https://mav2clu50.github.io/WSACA/v1/)** — The first published version. Same eligibility logic and 2027 threshold data, with a simpler presentation. Preserved for reference and for any member counties that initially integrated against it.

The landing page at the root of this site routes users to the recommended version (v2) while keeping v1 reachable.

Both versions reflect the program changes enacted by Engrossed Substitute Senate Bill 6162 (2026), including the new income thresholds for tax years 2027–2029, the standard deduction option, the consolidated State School Levy, the rental income deduction, and the updated benefit amounts at each level.

This is a screening tool only — it does not make official determinations of eligibility. Final eligibility is always determined by the applicant's county assessor.

---

## Repository Structure

```
WSACA/
├── index.html       ← landing page (version chooser, project intro)
├── wsaca-logo.png   ← WSACA logo, referenced by both the landing page and the tool
├── v1/index.html    ← original screening tool (preserved)
├── v2/index.html    ← current screening tool
└── README.md        ← this file
```

Each HTML file is fully self-contained — no external CSS, no JavaScript framework dependencies, no third-party API calls. The tools run entirely in the browser. Hosting is GitHub Pages.

---

## Using these tools at your county

If you're a Washington county assessor's office and would like to:

- **Link from your county website** — point to either `https://mav2clu50.github.io/WSACA/` (the landing page) or `https://mav2clu50.github.io/WSACA/v2/` (direct to the screening tool), whichever fits your context better.
- **Embed in your existing page** — the screening tool can be loaded inside an iframe. Reach out if you need help with sizing or integration.
- **Adapt for local needs** — the source is on GitHub. Fork the repo, customize, host wherever works for you. Attribution appreciated but not required.

If you spot something that's out of date or incorrect, the fastest way to flag it is to open an Issue using the **Issues** tab above. Bug reports, suggestions, and contributions are all welcome.

---

## Maintenance

Tools in this repository are maintained on a best-effort basis by WSACA leadership. Income thresholds, statutory references, and program details will be updated as the Department of Revenue publishes revised data and as legislation changes the program.

These tools were developed collaboratively with AI assistance and with feedback from member counties, the Department of Revenue, and the assessor community.

---

## Credits

Maintained by the Washington State Association of County Assessors.

Initial release: 2026.
