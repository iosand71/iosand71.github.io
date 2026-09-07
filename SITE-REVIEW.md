# Personal site review

Reviewed on 7 September 2026 using the repository and local Chrome rendering. The live domain could not be retrieved by the browsing tool, so findings describe the local site.

The site has a distinctive personal motif, but the homepage behaves like a splash screen: visitors see the site name and a motto without learning who Andrea is or what they can explore. The strongest improvement is to introduce the person and bring the existing work onto the homepage.

| Priority | Finding | Proposed improvement |
| --- | --- | --- |
| High | The visible homepage has no introduction, project summaries, or next action. | Consider a short introduction, a clear project link, and an about section. These were explored in the first proposal and subsequently removed at the owner's request. |
| High | All four projects are behind a hamburger menu, even on desktop. | Show all four on the homepage with descriptive links, geographic scope, and update dates. |
| High | The international notebook says 23 November 2022; the other three say 17 November 2022. | Label the collection as historical and show dates before a visitor opens a notebook. |
| Medium | The grey gradient, black panels, and image-based quote dominate the page. | Use a warm neutral background, restrained red accents, clearer type hierarchy, and a text version of the motto. Preserve its Japanese theme. |
| Medium | The homepage loads KaTeX CSS and two KaTeX scripts despite containing no equations. | Omit these from the proposed homepage. The current preview uses a local font, original images, and no JavaScript or third-party requests. |
| Medium | The title is generic; the description promises articles that are not visible. The RSS feed links to a `/posts/` directory absent from this repository. | Use a descriptive title and accurate description. Repair or retire the stale feed when updating the production site. |
| Medium | A personal introduction, recent work, and contact details are absent. | Add a specific bio, one or two current projects with outcomes, and an approved contact or professional profile link. These need real information from the owner. |

## Adopted homepage

The owner selected the version closest to the original and requested replacing the homepage with it. It retains the original grey background image, black header, centered site name, Ki logo, and original motto image. Changes are limited to responsive sizing, consistent alignment, descriptive alternative text, and keyboard focus. The archive and about section are absent from the homepage. The archived pages remain available at their existing URLs. The recommendations above describe the initial evaluation; the editorial redesign was not retained.

- Local homepage: <http://127.0.0.1:8000/>
- Files: `index.html` and `css/home.css`.
- Italian is retained to match the existing site and notebooks.
- The preview file, comparison link, and noindex directive have been removed. The notebooks are unchanged.

## Verification

The current preview was checked in Chrome at widths of 1440 and 390 pixels. Both screenshots were inspected; neither layout had horizontal overflow or broken images. The page has one main heading and a skip link to the main content. Git whitespace checks passed.

The preview includes visible keyboard focus styles and descriptive alternative text for the motto. This was a targeted browser check, not a full accessibility audit. The existing notebook visualizations were not revalidated.

The homepage is ready to publish, with a canonical URL, social sharing metadata, and a logo link to the site root. Deployment is a separate step from committing these changes.
