# Immunological Laboratory Reference Values

Enter a patient's age and see age-specific reference values for serum immunoglobulins, IgG subclasses,
lymphocyte subsets, T-cell subsets and B-cell subsets from ten sources side by side.

- One column per source, so every number is traceable to its study. The limit type (laboratory interval,
  5th–95th, 10th–90th percentile, interquartile range, observed min–max) is printed under each source name,
  with the 95% confidence interval where a study reports one (Aksu 2006).
- "Limits and sources" lets the user keep only the limit types and studies they want.
- Counts and percentages of the same cell type sit next to each other in one table per section.
- "All sources" column: lowest lower limit to highest upper limit among the sources shown (an overview, not a reference interval).
- A bar in each cell draws the source's range on a scale shared by the row, with a tick at the median.
- Units switch for the whole page: mg/dL ↔ g/L and cells/µL ↔ ×10⁹/L.
- Compact view (ranges only) and "All on one page" (every section together).
- Selecting a marker's name opens every age group from every source, with a one-line description of the marker.
- Notes appear automatically for the age entered (for example maternal IgG in early infancy). Markers on which sources
  disagree widely are tagged "sources differ"; groups of fewer than 20 subjects are flagged with their n.
- Dark mode by default, with a light-mode switch. Works on phones. The current view can be printed or saved as CSV.

## Use

Open `index.html` in any browser. It is one self-contained file: no build step, no server, no internet connection needed.

## Publish with GitHub Pages

1. Create a repository and upload `index.html` (and this README) to its root.
2. Settings → Pages → Source: "Deploy from a branch" → `main`, `/ (root)` → Save.
3. After a minute the page is live at `https://<username>.github.io/<repository>/`.

A link such as `…/#age=1096d` opens the page at that age (in days).

## Data

The data sit in the `DATA` object inside `index.html`: `studies`, `params` (with `about` text), and `series`
(one per study and marker; each row has `a`/`z` = age range in days, `v` = [lower, median or mean, upper],
optional `n`, `ci`, and `f` for a suspected misprint).

Sources: Mayo Clinic Laboratories; Aksu 2006; Shearer 2003; Tosato 2015; Äärimaa 2025; Piątosa 2010;
Duchamp 2014; Morbach 2010; Children's Mercy Kansas City; National Jewish Health chart. Full citations are on the page.

## Limits of the data

- Limits from different sources are not interchangeable; they depend on assay, population and percentile definition.
- Age groups printed as closed ranges (for example 7–8 years) are taken to run up to the start of the next group.
- Counts are shown in cells/µL; values published as ×10³/µL or ×10⁹/L were converted.
- Not covered: cord blood, preterm infants, Saudi or Gulf cohorts.
- Two Shearer 2003 absolute counts look like misprints in the paper and are flagged on the page.
- The +/– marker labels of Duchamp 2014 absolute counts were read from a damaged PDF text layer; check against the paper.
- Marker descriptions and age notes are general background written for this page, not taken from the cited studies; have a clinician review them before publishing.
- For reference only. The reporting laboratory's validated intervals take precedence.
