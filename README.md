# Minxing Zhang — academic personal website

A static, single-page academic homepage. No installation, package manager, font download, or build command is required.

## Publish

Extract the ZIP and upload its **contents**, not the ZIP itself, to the root of the existing website repository. Keep `index.html`, `portrait.jpg`, and `Minxing_Zhang_CV.pdf` together. Include `.nojekyll`, `robots.txt`, and `sitemap.xml` as well. Do not delete an existing `CNAME` file when updating a repository using a custom domain.

The deployment files are:
- `index.html`: content, CSS, and the small optional navigation enhancement.
- `portrait.jpg`: original photograph, unchanged.
- `Minxing_Zhang_CV.pdf`: finalized CV, unchanged.
- `.nojekyll`: static-site marker.
- `robots.txt` and `sitemap.xml`: crawler metadata for the existing canonical domain.

The Markdown documents describe the design references and tests; they are not needed for the rendered page.

## Availability

The two role types intentionally have different dates:

**Internships:** Summer 2027 and Fall 2027.  
**Full-time:** Spring 2028.

The About section, Contact section, page description, and social description all use this distinction. Update all four locations together in future edits. No expected graduation date has been inferred from this availability.

## Editing

Edit the semantic sections directly in `index.html`. CSS tokens at the beginning define font sizes, colors, spacing, and reading width. Keep the established section order, all publication author lists, comparison scopes, and submission labels unless their facts change.

The work, project, education, and publication-title/author text was checked against the previously approved version. The nine public publications/preprints remain separate from the two internship manuscripts described in Experience. No anonymous manuscript PDF is bundled.

Use the existing HTML structures for new entries. Do not turn company names, job roles, dates, and paragraph text into identical headings. Keep paper/code/project links beside the relevant work, and retain descriptive accessible names for repeated link labels.

The stylesheet uses Arial/Helvetica/system fallbacks. No font files are distributed. Core content, contact links, PDF links, and native section navigation work with JavaScript disabled. JavaScript only improves section highlighting and decides whether the desktop sidebar fits in the viewport.

If the domain changes, update the canonical link, Open Graph metadata, structured data, robots.txt, and sitemap.xml. Browser-rendered print layout is not a replacement for the separately provided two-page CV.

No live website was modified during this revision.
