# seemabanalytics.com

Static website for Seemab Hassan, Healthcare Data Systems and Program Integrity. Built for GitHub Pages, no build step required.

## Structure

```
Website_Build/
├── index.html              Home
├── about.html              About
├── work.html               Work hub
├── recognition.html        Recognition
├── contact.html            Contact
├── 404.html                Fallback page
├── README.md               This file
├── work/
│   ├── medicare-part-d-prescriber-risk.html
│   ├── medicare-part-d-opioid.html
│   ├── medicare-part-b-drug-waste.html
│   ├── dme-program-integrity.html
│   ├── telehealth-program-integrity.html
│   ├── hospital-drg-billing.html
│   ├── home-health-hospice.html
│   └── healthcare-access-equity.html
└── assets/
    ├── css/site.css        Single stylesheet, all pages
    ├── figures/            Project figure PNGs (24 files)
    └── downloads/          Exhibit PDFs for download (8 files)
```

## Deployment to GitHub Pages

1. Create or use an existing repository named `seemabie/seemabie.github.io` or any repo with Pages enabled.

2. Copy the entire contents of this `Website_Build` folder to the repository root. The `index.html` must sit at the repository root, not inside a subfolder.

3. Push to the `main` branch.

4. In repository settings, navigate to Pages and set the source to `main` branch, root folder.

5. For the custom domain `seemabanalytics.com`, create a `CNAME` file at the repository root containing exactly one line: `seemabanalytics.com`. Then configure the DNS for the domain to point to GitHub Pages (the four A records, or an ALIAS to `seemabie.github.io`).

6. GitHub Pages will build and serve the site within a few minutes. Confirm by visiting the custom domain.

## Design notes

The site uses a system font stack: EB Garamond or Garamond for body, Helvetica Neue or Inter for headings. No fonts are loaded from a CDN. On macOS the user sees Helvetica Neue. On Windows the user sees Arial as the heading fallback. To self host EB Garamond and Inter, add font files to `assets/fonts/` and add corresponding `@font-face` rules at the top of `assets/css/site.css`.

The single stylesheet at `assets/css/site.css` controls every page. All design tokens (colors, spacing, typography) are defined there.

## Updating numbers

Every numerical claim on the site traces to the canonical claims traceability files in the parent project rebuild folders. To update a stat block: edit the relevant HTML page, update the matching `.stat-number` element, and re commit.

## Out of scope for this build

LinkedIn link, CV download link, SSRN preprint URLs, and any analytics or tracking scripts. These can be added later in a follow up pass when real URLs are available.
