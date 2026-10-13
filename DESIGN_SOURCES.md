# Source-informed design review

Reviewed 13 October 2026. The source material was retrieved and read through the web tool. GitHub archives/raw downloads into the working container were unavailable, so these are **source-informed applications of the guidance**, not a claim that a skill plugin, search generator, or complete framework was installed or executed.

Star counts below are rounded counts on the whole repository as displayed by GitHub at review time. They are not skill-specific usage counts or a universal ranking of design quality.

| Repository | Stars, approximately | What was read | Applied here |
|---|---:|---|---|
| [Anthropic Skills](https://github.com/anthropics/skills) | 180,900 | `frontend-design/SKILL.md`; `webapp-testing/SKILL.md` | Context-appropriate restraint, clear type hierarchy, a controlled reading width, and actual browser inspection rather than assuming the result looks correct. |
| [UI UX Pro Max](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill) | 135,400 | `SKILL.md`; `references/quick-reference.md` | Consistent semantic styles, prioritizing accessibility and reflow, and checking focus, text enlargement, touch targets, and responsive behavior. |
| [Vercel Agent Skills](https://github.com/vercel-labs/agent-skills) | 32,400 | The linked Web Interface Guidelines | Native anchors, visible focus, descriptive labels, image dimensions, safe wrapping, and batched layout measurements. |
| [Academic Pages](https://github.com/academicpages/academicpages.github.io) | 17,700 | `_includes/archive-single.html` | Title-first bibliographic entries, clear publication metadata, and directly associated resources. |
| [al-folio](https://github.com/alshedivat/al-folio) | 16,200 | `_pages/publications.md` | Publications as a complete academic record rather than promotional tiles. No Jekyll or plugin infrastructure was added. |

## Exact guideline locations

- https://raw.githubusercontent.com/anthropics/skills/main/skills/frontend-design/SKILL.md
- https://raw.githubusercontent.com/anthropics/skills/main/skills/webapp-testing/SKILL.md
- https://raw.githubusercontent.com/nextlevelbuilder/ui-ux-pro-max-skill/main/.claude/skills/ui-ux-pro-max/SKILL.md
- https://raw.githubusercontent.com/nextlevelbuilder/ui-ux-pro-max-skill/main/.claude/skills/ui-ux-pro-max/references/quick-reference.md
- https://raw.githubusercontent.com/vercel-labs/web-interface-guidelines/main/command.md
- https://raw.githubusercontent.com/academicpages/academicpages.github.io/master/_includes/archive-single.html
- https://raw.githubusercontent.com/alshedivat/al-folio/main/_pages/publications.md

The approved baseline already used a Minimal Light-inspired profile/content structure, informed by Jon Barron's publication presentation and Academic Pages. That structure is retained, not replaced with another theme:
- https://github.com/yaoyao-liu/minimal-light
- https://github.com/jonbarron/jonbarron.github.io

## Concrete revision decisions

1. **Availability:** replace the ambiguous combined date sentence with two explicitly paired role/date rows. Repeat the distinction in Contact and page/social metadata.
2. **Typography:** use a single family and named text roles. Raise body text from 16 to 17 pixels and give the main column a 696-pixel maximum width. Dates, roles, employers, statuses, and descriptions remain visually distinct.
3. **Profile:** reduce portrait prominence slightly and move contact links out of the narrow mobile biography/photo grid. Under enlarged text, the profile wraps into a normal stack instead of squeezing the name into a tiny column.
4. **Publication alignment:** put the number in a small separate gutter so wrapped titles, author lists, venue lines, and resources have consistent left edges.
5. **Navigation:** add small, unobtrusive heading permalinks. Do not change weight on active navigation, which avoids width shifts. Honor explicit fragment clicks near the bottom of the page, where several short sections share a viewport.
6. **Reading and interaction:** standardize paragraph/entry spacing, focus indication, native link behavior, and touch-link dimensions. Avoid hidden content and runtime dependencies.
7. **Content integrity:** preserve the approved education, experience, projects, publication titles and author lists. Keep their numbers, comparison scopes, and links; do not invent publication statuses or technical outcomes.

The brief takes priority over template demonstrations. Promotional hero text, animation, counters, result cards, elaborate interactions, and extra font families were deliberately not imported.

## Attribution and execution scope

The resulting CSS and optional navigation implementation were rewritten for this static page. No external font files, complete template distribution, skill runner, or third-party runtime code is shipped. This document records the source influences; it is not a claim that the site is an official implementation of any repository.
