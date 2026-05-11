# WSACA Property Tax Exemption Screening Tool

A free, open-source screening tool that helps Washington homeowners check whether they may qualify for the expanded 2027 property tax exemption program for senior citizens and people with disabilities. Built by the Washington State Association of County Assessors (WSACA) to be used freely by any of Washington's 39 county assessor offices.

**Live site:** [mav2clu50.github.io/WSACA/](https://mav2clu50.github.io/WSACA/)

## What this is

In 2026 the Washington State Legislature passed Engrossed Substitute Senate Bill 6162, which substantially expanded the property tax exemption program beginning in tax year 2027. New income thresholds. New deductions. A consolidated state school levy. Larger benefits at every qualification level. In 2025, Engrossed House Bill 1106 also lowered the disabled veteran service-connected evaluation requirement from 80% to 40%, effective for the same 2027 tax year.

This tool walks a homeowner through five questions — county, age or disability status, ownership and occupancy, household composition, and income — and returns a clear, county-specific answer about whether they may qualify, at what level, and what they'd save. It's not an official determination. Only the county assessor can make that. But it gets the homeowner to the assessor's office with the right expectations and the right documents.

No login. No data collection. No installation. Just a tool that runs in any browser and points the applicant toward their local county assessor for the official determination.

## Versions

Three versions are available. The current version reflects multiple rounds of feedback from member counties. Older versions are preserved for reference and for counties that integrated against earlier releases.

### Version 3 — current, recommended

Live at [/v3/](https://mav2clu50.github.io/WSACA/v3/).

Incorporates feedback from San Juan County (Annie Minich, Melanie Correll, Megen) on top of all earlier feedback. Key v3 improvements:

- **Rental income deduction handled separately** from gross income, parallel to the standard/itemized choice (per RCW 84.36.383(2)(b)(v)). The v2 release incorrectly grouped this with itemized medical deductions; v3 corrects the calculation.
- **Documents-to-bring list grouped by category** in the printable result document — Identity and residence, Eligibility basis, Household considerations, Income documentation, Deduction documentation. Empty categories are filtered out based on the user's actual inputs.
- **Refined statutory citations** based on county assessor feedback. The veteran 40% threshold change is correctly attributed to EHB 1106 (2025); ESSB 6162 (2026) is retained for the income thresholds, standard deduction, rental income deduction, and school levy consolidation provisions.
- **Improved accessibility:** semantic heading hierarchy (H1 → H2 → H3 → H4), focus management on county selection, screen reader announcements debounced to avoid interrupting users mid-input, color contrast brought to WCAG AA on dark backgrounds.
- **Refined disability requirement language:** "Requires physician's affidavit, or if the disability is permanent, a determination by SSA or VA is acceptable" — matches DOR's actual policy.
- **Capital gains losses add-back** explicitly called out in the income line and reminder note.
- **New-construction caveat** on the taxable value freeze, both on screen and in the printed result.
- **Trust document handling** broken out as its own line in the documents list.
- All v2 features below are retained.

### Version 2 — previous version

Live at [/v2/](https://mav2clu50.github.io/WSACA/v2/).

The first full guided release. Includes:

- 2026-vs-2027 threshold comparison panel, county-specific
- A/B/C level labels paired with DOR's Threshold 1/2/3 terminology
- Income spectrum visualization showing where the user lands relative to county thresholds
- 5% buffer "you're close — please call" branch for users just over the Level C threshold
- Tailored documents-to-bring list based on inputs
- Click-to-reveal RCW citations throughout
- Printable result document
- Direct link to the user's county assessor's website

Functional but superseded by v3.

### Version 1 — original release

Live at [/v1/](https://mav2clu50.github.io/WSACA/v1/).

The first published version of the screening tool. Same eligibility logic and 2027 threshold data, with a simpler presentation and fewer guided features. Preserved for reference and for member counties that initially integrated against it.

## How counties can use this

The tool is published under an open license. Any county assessor's office in Washington (or anywhere else) is welcome to:

- Link to the live tool from a county website
- Embed it via iframe
- Fork the repository and host a county-branded version
- Suggest improvements via issue or pull request

The tool is intentionally county-agnostic. It includes income thresholds for all 39 Washington counties and adapts its result to whichever county the user selects.

## Acknowledgments

The tool was built collaboratively with feedback from many WSACA member counties — most consistently from Whatcom County (Falon Hoven, Chief Deputy Assessor), along with substantive review and improvements from Thurston (Steven Drew, JJ), Spokane (Tom, Jess), Pierce, Skamania (Gabe), Yakima, and San Juan (Melanie Correll, Annie Minich, Megen). The WSACA Public Engagement Committee provided structural feedback during the development cycle.

Initial inspiration came from a draft DOR flyer prepared by Thurston County. The screening tool grew from there into an interactive, county-specific resource.

## How it was built

The tool was built with AI assistance and refined through feedback from member counties. It's plain HTML, CSS, and JavaScript — no build step, no framework, no external dependencies beyond a Google Font. Each version is a single self-contained HTML file. The repository is structured to support future tools alongside this one as WSACA's tool chest grows.

## About WSACA

The Washington State Association of County Assessors is a standing professional organization representing the elected and appointed assessors of Washington's 39 counties. WSACA works alongside the Washington Association of County Officials (WACO) to advance the practice of property assessment statewide.

## License

This repository is published with the intent that any Washington county assessor's office may use, adapt, embed, or extend the tool for the benefit of homeowners in their county. See LICENSE for details.
