# Slideshow banner

## Contract and plan

- Role and placement: homepage content banner in `templates/index.json`.
- Context: merchant-selected images and nested theme blocks; no product context.
- Section owner: `sections/slideshow.liquid` owns shared vertical/horizontal content placement, dimensions, autoplay and controls.
- Block owner: `blocks/slideshow-slide.liquid` owns media and dynamic content. Existing child blocks retain typography, sizing and CTA contracts.
- Composition: two starter slides with Heading and Button; merchants can add, remove and reorder slides and content. No section-specific slide cap.
- Foundation: existing hero container, color schemes, page margins, heading/button blocks and Swiper runtime.
- Custom CSS: homepage section centers child text and buttons, styles heading text and places navigation around centered current/total pagination. New slides inherit it.
- Shared placement: opt-in section setting preserves per-slide positioning when disabled. With it enabled, column flex maps vertical placement to justify-content and horizontal placement to align-items. Mobile inherits these settings.
- Runtime: existing `assets/slideshow.js` with fraction pagination subscribing to slide index changes and cleaning up on section unload. Single-slide controls retain existing hidden behavior.
- Images: source photography was not supplied; image-picker placeholders remain until merchant selection.
- CTA: `shopify://collections/all` opens the store's all-products collection.

## Validation checklist

| Key | Status | Evidence |
| --- | --- | --- |
| contract | pass | Existing slideshow/hero and theme block contracts reused. |
| schema | pass | Valid JSON, categorized slide preset and categorized child allow-list. |
| ranges | pass | All 1,324 range settings audited; zero violations. |
| liquid-css | pass | Section settings map to root variables consumed by shared placement CSS. |
| javascript | pass | Fraction pagination verified for normal slides, native/manual loops, wrap and listener cleanup. |
| static-responsive | pass | Shared placement applies at both breakpoints; mobile heading size uses section Custom CSS. |
| diff | pass | git diff --check passed. |
| theme-check | pass | Zero errors, 33 existing warnings. |
| runtime-responsive | blocked | Live preview not inspected. Verify all nine positions and fit/custom/full content widths on desktop/mobile. |
| accessibility | blocked | Verify prev/next, paging and CTA keyboard navigation in preview. |
| editor | blocked | Verify add/remove/reorder/select/reload and that new slides inherit placement and Custom CSS. |
| visual | blocked | Select source photos and compare banner/controls against reference. |
| release | blocked | Preview checks remain; no commit, push or deployment performed. |
