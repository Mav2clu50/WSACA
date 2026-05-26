# WSACA Tools

Free, open-source tools for the public work of property tax assessment. Built once, shared freely, and improved together.

County assessors do essential public work, often with limited staff and budgets. Some of the tools they need are too small or specialized to be worth building and maintaining commercially — but they are needed all the same. This repository is a small, growing collection of tools like that, developed by the Washington State Association of County Assessors (WSACA) and free for any county assessor's office to use.

**Live site:** https://mav2clu50.github.io/WSACA/

## The idea

A few simple commitments shape every tool here:

- **Built once, shared with all.** A small rural county gets exactly the same tool as the largest urban one.
- **Open by default.** The code, methods, and assumptions behind every tool are open to inspection. Anything that affects the public should be something the public can examine.
- **Free, and free to stay that way.** No logins, no fees, no data collection, nothing to lock into.

These tools were built with substantial help from AI. That is stated plainly here, and again on each tool, because work done for the public should be honest about how it was made.

## The tools

### Property Tax Exemption Screening Tool

*For homeowners.* A screening tool that helps Washington homeowners check whether they may qualify for the expanded 2027 property tax exemption program for senior citizens and people with disabilities.

In 2026 the Washington State Legislature passed Engrossed Substitute Senate Bill 6162, which substantially expanded the property tax exemption program beginning in tax year 2027 — new income thresholds, new deductions, a consolidated state school levy, and larger benefits at every qualification level. In 2025, Engrossed House Bill 1106 lowered the disabled veteran service-connected evaluation requirement from 80% to 40%, effective for the same 2027 tax year.

The tool walks a homeowner through five questions — county, age or disability status, ownership and occupancy, household composition, and income — and returns a clear, county-specific answer about whether they may qualify, at what level, and what they would save. It is not an official determination; only the county assessor can make that. But it gets the homeowner to the assessor's office with the right expectations and the right documents.

No login, no data collection, no installation. It runs in any browser and points the applicant toward their local county assessor for the official determination.

**Current version:** [/v3/](https://mav2clu50.github.io/WSACA/v3/)

#### Versions

Three versions are available. The current version reflects multiple rounds of feedback from member counties. Older versions are preserved for reference and for counties that integrated against earlier releases.

**Version 3 — current.** Incorporates feedback from San Juan County on top of all earlier feedback. Key improvements:

- Rental income deduction handled separately from gross income, parallel to the standard/itemized choice (per RCW 84.36.383(2)(b)(v)). The v2 release incorrectly grouped this with itemized medical deductions; v3 corrects the calculation.
- Documents-to-bring list grouped by category in the printable result — Identity and residence, Eligibility basis, Household considerations, Income documentation, Deduction documentation — with empty categories filtered out based on the user's actual inputs.
- Refined statutory citations: the veteran 40% threshold change is correctly attributed to EHB 1106 (2025); ESSB 6162 (2026) is retained for the income thresholds, standard deduction, rental income deduction, and school levy consolidation provisions.
- Improved accessibility: semantic heading hierarchy, focus management on county selection, debounced screen reader announcements, and color contrast brought to WCAG AA on dark backgrounds.
- Refined disability requirement language matching DOR's actual policy.
- Capital gains losses add-back explicitly called out in the income line and reminder note.
- New-construction caveat on the taxable value freeze, on screen and in the printed result.
- Trust document handling broken out as its own line in the documents list.

**Version 2 — previous.** The first full guided release: a 2026-vs-2027 threshold comparison panel, A/B/C level labels paired with DOR's Threshold 1/2/3 terminology, an income spectrum visualization, a 5% buffer "please call" branch for users just over the Level C threshold, a tailored documents list, click-to-reveal RCW citations, a printable result, and a direct link to the user's county assessor. Functional but superseded by v3. Live at [/v2/](https://mav2clu50.github.io/WSACA/v2/).

**Version 1 — original.** The first published version: the same eligibility logic and 2027 threshold data, with a simpler presentation and fewer guided features. Preserved for reference. Live at [/v1/](https://mav2clu50.github.io/WSACA/v1/).

### Sales Ratio Analysis

*For assessor offices.* A self-contained sales ratio analysis tool for assessor staff to use during the assessment cycle, before certified values are finalized.

Upload a validated sales file and the tool produces IAAO 2025-grounded ratio statistics, vertical equity diagnostics, and modifier recommendations. It is built to support in-cycle analysis and is **not a substitute for the official vertical equity report**.

- Accepts CSV or Excel (.xlsx) sales files with automatic column mapping
- Overall ratio diagnostics: median, COD, PRD, and PRB with IAAO threshold flags
- Time adjustment, vertical equity, and stratified analysis by neighborhood or use code
- Modifier recommendations to support assessment cycle decisions
- Runs entirely in the browser; no data leaves the analyst's machine

**Tool:** [/sales-ratio/](https://mav2clu50.github.io/WSACA/sales-ratio/)

## How these tools are built

Each tool is plain HTML, CSS, and JavaScript — no build step, no framework, no external dependencies beyond a Google Font. Each is a single self-contained file that runs entirely in the browser, with no backend and no data transmission. The repository is structured to hold multiple tools side by side as the collection grows.

The tools were built with substantial help from AI and refined through feedback from WSACA member counties.

## Using and adapting the tools

Every tool here is open source and free to use. Any assessor's office — in Washington or anywhere else — is welcome to:

- Link to a live tool from a county website
- Embed it via iframe
- Fork the repository and host a county-branded version
- Suggest improvements via issue or pull request

Nothing about the approach is specific to Washington. If the model is useful, use it.

## Acknowledgments

Built by Danny Hagen, Skagit County Assessor and current WSACA President.

The Property Tax Exemption Screening Tool was developed with feedback from many WSACA member counties — most consistently Whatcom County (Falon Hoven, Chief Deputy Assessor), along with substantive review from Thurston (Steven Drew, JJ), Spokane (Tom, Jess), Pierce, Skamania (Gabe), Yakima, and San Juan (Melanie Correll, Annie Minich, Megen). Initial inspiration came from a draft DOR flyer prepared by Thurston County.

The Sales Ratio Analysis tool was developed with feedback from Yakima, Clark, and Whatcom counties.

The WSACA Public Engagement Committee provided structural feedback during development.

## About WSACA

The Washington State Association of County Assessors is a standing professional organization representing the elected and appointed assessors of Washington's 39 counties. WSACA works alongside the Washington Association of County Officials (WACO) to advance the practice of property assessment statewide.

## License

This repository is open source. It is published with the intent that any county assessor's office — in Washington or elsewhere — may freely use, adapt, embed, or extend these tools for the benefit of the homeowners they serve. See [LICENSE](LICENSE) for the full terms.
