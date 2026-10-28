# AI Economy Viewer Board

A static, single-page explanation of the AI economy’s capital flows, value capture, and household exposure. The circular diagram follows capital from savings to infrastructure; the inner return path represents equity and wage risk. Five regional panels contain six jurisdiction cards, with the United States and Canada shown separately.

**This is a mechanism illustration, not a prediction or investment advice. Figures are dated snapshots.** Institutional investment is not automatically a hedge against job loss. Buyout eligibility does not establish AI replacement. Sovereign investment is distinct from personal pension ownership.

## Open the board

The site uses HTML, inline CSS, SVG, and vanilla JavaScript. There are no packages, frameworks, build steps, or external fonts. Enable GitHub Pages in repository **Settings → Pages → Deploy from a branch**, selecting **main** and **/ (root)**.

For local viewing, run `python3 -m http.server 8000` in this directory and open `http://localhost:8000`. Opening the HTML directly with a file URL does not reliably allow the browser to fetch the JSON.

## Files

- `index.html`: self-contained rendering, styling, and interactions.
- `data/snapshot.json`: all displayed content, figures, dates, labels, and source metadata. Edit this file alone to update the board.
- `LICENSE.md`: content licensed under CC BY 4.0; code under MIT.
- [Model paper](ai-bottleneck-theory-v01.md) and [regional research note](pension-capital-and-ai.md): background analysis.

## Evidence policy

Snapshot values reproduce the supplied brief exactly; the renderer does not round, recalculate, or substitute values. Each metric has `value`, `label`, `source_name`, `source_url`, and `date`. A null source URL means the exact link was not supplied; the board explicitly labels it pending. A supplied link is not a claim of independent verification. The source list is generated from the same metric objects as the board.

The requested Q3 badge is retained, but the snapshot also contains October developments. The page discloses this mismatch; each figure’s date takes precedence. Regional circuit lines are qualitative illustrations, not quantitative resistance scores. The headline is a mechanism framing, not a proven causal statement about every household.

## Quarterly updates

1. Review each metric against its original source. Preserve the current snapshot in Git history before changing it.
2. Edit `data/snapshot.json` only. Enter the exact published value as a string, its scope in `label`, publisher in `source_name`, a precise HTTPS link in `source_url`, and the relevant reporting period in `date`. Do not silently turn commitments into deployed capital or targets into current allocations.
3. Resolve pending citations when exact sources become available. Keep unknown dates explicitly unknown. Match categories and denominators before drawing comparisons.
4. Update `badge`, `timing_note`, and explanatory text to match the reporting period. Keep forecasts, targets, and realized figures distinguishable.
5. Serve locally. Check the diagram, all regional cards, keyboard tooltips, source links, and mobile stack. Check the browser console and confirm the JSON request succeeds.
6. Commit and push. GitHub Pages republishes from the configured branch without a build step.

The page uses text insertion rather than HTML insertion for snapshot content. Source URLs should be reviewed as HTTPS URLs. All numeric content is held in JSON; layout coordinates and visual styling constants remain in the page.
