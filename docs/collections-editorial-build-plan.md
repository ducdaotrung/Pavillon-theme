# Collections editorial

## Build plan and ownership

Homepage content section after Timeless Radiance. Reuse Collections with tabs with an opt-in `editorial` presentation; classic instances keep their two-column presentation. The section owns layout, spacing, background, media ratio and title/count controls. Item blocks own selected collection, custom title/image and dynamic Heading/Text/Button/Group content. Global Theme Settings own typography and color tokens. Existing collections-with-tabs JavaScript owns tab activation, keyboard navigation, inactive-panel inertness and editor lifecycle.

Defaults: dynamic Collections header followed by Suspense, Overtone, Ondine and Gossamer items. Desktop places navigation beside a panel containing portrait media and introduction; mobile stacks the active panel and tabs using existing section behavior. Selected tab has italic/underlined title. Counts are actual collection product counts. No per-section item cap. No sample product counts or photograph paths are supplied.

All child allow-lists reference existing categorized block presets. Item preset defines editable introduction composition. Header is dynamic rather than a fixed slot. Search of local templates and section groups found no pre-existing Collections with tabs instances before insertion, so no local saved header migration was required. Existing remote instances of this section may need their static `look-header` converted into a dynamic Header block; preserve their child content when migrating.

Homepage item introductions use Selected collection: title, rich description and SHOP ALL URL come from the selected collection. Blank descriptions are omitted. Custom blocks remain available as an alternate source, preserving previously saved content. Each item needs a store collection and custom image/collection image to match the reference photography.

## Validation

| Key | Status | Evidence |
| --- | --- | --- |
| contract | pass | Existing section, media, theme-block and global typography contracts reused. |
| schema | pass | Classic/editorial selector, categorized item preset, dynamic header and child allow-list. |
| ranges | pass | 1,325 settings checked across sections/blocks/global schema; no violations. |
| liquid-css | pass | Conditional editorial layout and section settings mapped to existing CSS variables. |
| js | pass | Syntax and mocked initialization, click, keyboard wrap, inert-panel and reload checks passed. |
| theme-check | pass | Zero errors; 32 baseline warnings. |
| diff | pass | git diff --check. |
| responsive-runtime | blocked | Live desktop/mobile layout and real photography not inspected. |
| editor | blocked | Add/remove/reorder/select/reload of dynamic header, items and introduction children needs live verification. |
| accessibility | blocked | Real-browser tab focus, nested CTA navigation and screen-reader behavior need verification. |
| remote-migration | blocked | Remote saved instances have not been inspected. |
| release | blocked | Preview checks remain; no commit, push or deployment performed. |

Collection title supports Custom font size (16–116px, step 1, default 64px). Homepage selects Custom at 64px. Collections header spacing below is 32px on desktop and mobile.
