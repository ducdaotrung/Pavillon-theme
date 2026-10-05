# Timeless Radiance

Plan: compose the existing Collection tabs section below the homepage Slideshow. The section owns carousel spacing and controls; collection-tab blocks own merchant-selected collections; existing Header, Tab layout and Product Card contracts supply content and presentation. Preserve existing static composition without a schema migration. No global typography or product settings are changed.

Default composition: Timeless *Radiance* heading, New Arrivals and Best Sellers tabs, four desktop columns with next-card preview, two mobile columns and a narrow progress bar. Section Custom CSS aligns desktop heading/tabs on one row, keeps the native stacked mobile flow, enables the slash divider defined in the section stylesheet and portrait media framing. All fonts use global settings. Existing carousel/tab JavaScript handles tab changes and editor lifecycle.

Collections are intentionally unassigned until the merchant chooses store resources. Product photos, product types, titles, prices and badges come from actual products and shared Product Card settings.

| Check | Status | Evidence |
| --- | --- | --- |
| contract/schema | pass | Existing section preset/settings and categorized blocks reused; no schema edits or new limits. |
| composition | pass | Valid homepage JSON; two ordered collection tabs; original Slideshow preserved. |
| custom-css | pass | Section-scoped CSS is below the 500-character limit. |
| diff | pass | git diff --check. |
| responsive-runtime | blocked | Desktop/mobile preview remains unverified. |
| editor | blocked | Verify tab/collection selection, add/remove/reorder and reload in Theme Editor. |
| accessibility | blocked | Verify native tab arrow-key navigation and product-link focus in preview. |
| visual | blocked | Requires selected collections and product photography; exact reference match remains unverified. |
| release | blocked | Preview QA remains; no commit, push or deployment performed. |
