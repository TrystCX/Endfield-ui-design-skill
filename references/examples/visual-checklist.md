# 视觉与行为检查

Run the checks that match the artifact. Record the result as `verified`, `partial`, `blocked`, or `not tested`; a generated screenshot that was not inspected is not verified.

## Surface and hierarchy

- Can the dominant surface family be named in one sentence?
- Is the focal anchor derived from the content and task?
- Does the layout remain coherent when yellow and decorative texture are removed?
- Are website, cloud, game UI, and promotional conventions kept separate?

## Color and semantics

- Does each color have a role that survives theme changes?
- Are light-surface emphasis labels using a readable dark accent token instead of raw yellow?
- Are danger, success, warning, data, region, notice, gain, and rarity colors used for their defined meanings?
- Were real contrast checks run on the actual background and state, including disabled and focus states?

## Typography and content

- Does readable CJK text remain the primary reading layer?
- Is every English micro-label real, useful, and legible?
- Are numbers, dates, identifiers, and asset sources real or clearly marked as placeholders?
- Do long labels wrap without breaking controls or forming vertical digits?

## Responsive behavior

- Check at least 375px, 768px, 1280px, and 1920px for component-library work.
- Check the cloud page's 1180px and 2560px root-size boundaries only when building that surface.
- Decide which desktop sidebars become top bars, drawers, pagination, or contained horizontal scroll on narrow screens.
- Ensure decorative layers cannot create overflow or intercept pointer events.

## Interaction and accessibility

- Check keyboard navigation, focus-visible rings, disabled behavior, and accessible names for icon-only controls.
- Check hover-only affordances on touch devices; the task must remain usable without hover.
- Check loading, empty, error, success, and reduced-motion states where the artifact needs them.
- Check forced-colors or system high-contrast behavior for controls that normally rely on fills or shadows.

## Rights boundary

- Do not add official logos, character art, screenshots, proprietary fonts, or the source repository's game images unless the user supplied the asset and explicitly chose to use it.
- Prefer self-authored diagrams and clearly marked placeholders for examples.
