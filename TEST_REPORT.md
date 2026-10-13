# Website validation report

Revision date: 13 October 2026.

## Execution method and limitations

The actual final HTML was rendered with Python Playwright and Chromium 144.0.7559.96. Browser policy blocked HTTP localhost navigation and `file://` navigation. Testing therefore loaded the complete document with `page.set_content()`. Only in the temporary browser fixture, `portrait.jpg` was replaced with a data URI holding the exact same image bytes. The delivered HTML continues to reference `portrait.jpg` normally.

This tests the rendered DOM, CSS, scripts, native fragment links, keyboard behavior, and reflow. It is **not** a live deployment test, HTTP-header audit, or Safari/Firefox certification. No axe, Lighthouse, HTML5 conformance validator, screen-reader user study, or recruiter study was run. External-source pages were retrieved with the web tool rather than rendered in this browser.

## Content and assets

- 3 work/internship entries, 5 research project entries, and 9 publications/preprints are present.
- Normalized education, experience, and project text matches the approved input.
- Publication titles and complete author lists match the input.
- All original link destinations are retained; descriptive link labels and section permalinks are added.
- Publication 7's award capitalization was standardized; its meaning is unchanged.
- No duplicate IDs or missing internal anchor targets were found.
- Internships are explicitly Summer 2027 and Fall 2027; full-time availability is Spring 2028.
- The CV and portrait are byte-identical to the supplied originals.
- No remote font, stylesheet, or script dependency is required for rendering.
- HTML: 44,066 bytes. HTML plus portrait: 69,566 bytes before HTTP compression. This is a file-size measurement, not a network-performance score. The CV is fetched only when its link is opened.

Asset SHA-256:

```text
Minxing_Zhang_CV.pdf  6484eaed591fdda54d64646c034cc589f736c9485adf8ff8633aaec26e6f041a
portrait.jpg         3a0582426cd74a99aa2ac016e04db1873963a1631309b6fe53bf38c2f046ccad
```

## Responsive and visual checks

Widths checked: 320, 344, 360, 375, 390, 414, 430, 540, 640, 768, 820, 912, 1023, 1024, 1100, 1280, 1366, 1440, 1536, 1920 CSS pixels.

Every tested width completed without detected viewport overflow or clipped text containers. The original portrait loaded successfully. Full desktop and mobile screenshots and individual section screenshots were inspected; the review covered About, Education, all three work entries, all projects, all nine publications, talks, honors, skills, and Contact.

Additional conditions:
- 200% root text size at 1280×900 and 390×844.
- Landscape touch viewport, 844×390.
- Short desktop viewport, 1280×720.
- Increased line, letter, word, and paragraph spacing.
- JavaScript disabled at 390×844.
- Reduced-motion preference enabled.

No detected overflow or clipped text containers remained in these conditions. The sticky sidebar is disabled when its content is too tall; on narrow layouts its computed CSS remains non-sticky regardless of the fit flag. Enlarged-text testing is not the same as testing every browser's zoom implementation.

## Interaction checks

- First keyboard focus reaches Skip to content; activating it focuses the main content.
- Keyboard traversal found no focused anchor wholly outside the viewport.
- Section permalinks become visible on keyboard focus with a solid outline.
- Every section-navigation link produces the correct fragment and active state.
- Top section targets align about 24 pixels below the viewport top; bottom sections remain constrained by the document's natural scroll extent.
- Clicking Honors or Skills near the bottom correctly preserves that active section rather than incorrectly selecting Contact.
- Zero JavaScript page errors were captured.
- Reduced-motion mode had zero running animations; the design contains no decorative animation in the first place.

## Color checks

Computed text contrast against the white page:
- Main text: 12.84:1.
- Headings: 11.67:1.
- Secondary text: 6.12:1.
- Links: 7.39:1.

These checks cover the named text tokens. They are not a complete accessibility certification. High-contrast forced-colors support is included in CSS, but native operating-system high-contrast mode was not exercised.

## Printing

An internal browser-print export produced five pages; rendered pages were inspected for gross clipping, blank pages, and lost content. Long work descriptions may continue across pages. This export is for testing only and is not bundled as a new CV. The downloadable two-page CV is unchanged.

## External link checks

21 unique paper/profile/project/tutorial destinations were attempted through the web tool. 11 returned readable destination content: the Person Distillation DOI, sequential-release arXiv paper, MPCEval repository, Person Distillation website and source repository, Jian Pei's website, Li Xiong's website, Liang Zhao's website, Divesh Srivastava's website, KDD tutorial website, and PAKDD tutorial page.

10 endpoints were blocked or unavailable to the tool, so their live status could not be verified:
- MPCEval DOI: 10.1145/3770855.3817574
- Generalizability survey DOI: 10.1145/3794858
- Knowledge-distillation membership-inference DOI: 10.1145/3820356.3820359
- Data-buyer privacy DOI: 10.1109/MIC.2024.3398626
- CSGAN DOI: 10.1109/MDM58254.2023.00032
- Spatial prediction DOI: 10.1145/3605358
- Spatial interpolation DOI: 10.1145/3557915.3561008
- Google Scholar profile
- Minxing Zhang's LinkedIn profile
- Yaron Kanza's LinkedIn profile

Tool blocking is not evidence of a broken link. Those links were preserved; none was silently replaced. All bundled local asset paths exist and internal fragment targets resolve in the HTML. Clicking a PDF or external page was not part of the injected-document browser test.

## Issues found and corrected during this pass

- The combined hiring sentence obscured which dates belonged to each role type.
- Contact links were unnecessarily constrained by the mobile portrait/profile grid.
- Enlarged text squeezed the profile name into a very narrow column; the layout now wraps naturally.
- Publication numbers did not provide consistent hanging alignment for long titles.
- Padding on anchor targets exposed the previous section after a navigation click; spacing now uses margins.
- Bottom-of-page scroll logic overwrote explicit Honors/Skills selections with Contact.
- Small skills-column layout was replaced with stacked definitions where needed.

No live site, repository, account, or uploaded original was modified.
