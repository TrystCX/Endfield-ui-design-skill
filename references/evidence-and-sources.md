# Evidence and Sources

This reference records where the skill's rules come from. Read it when adding a rule, resolving a disagreement between documents and code, or reporting confidence.

## Repository identity

- Repository: `icaruszezen/endfield-ui`
- Local snapshot: `endfield-ui-main/`
- Verified branch: `main`
- Verified commit: `68c81171caa644ed73e98cb1d13c78439930c1f6`
- Verification date: 2026-11-18
- Verification method: compare the upstream recursive Git tree with the local file list and Git blob hashes

The local snapshot is content-complete for that commit, but it does not include the repository's Git history. Do not claim that commit history, issues, or pull-request discussion was reviewed unless it is separately retrieved.

## Evidence levels

| Level | Meaning | How the skill uses it |
| --- | --- | --- |
| `实测` | A value read directly from a measured public page | Treat as the strongest numeric evidence; preserve units and source date. |
| `观察` | A visible phenomenon in public material | Describe the observed behavior without inventing a token or universal rule. |
| `社区` | A project-author or community conclusion not independently verified | Keep the label; use as a hypothesis or implementation reference. |
| `推断` | A recommendation made by the source documentation | Present as guidance, not as an official fact. |

The source documents sometimes use a fifth practical category: implementation detail. Use it when describing behavior found in source code or tests, and keep it separate from visual evidence.

## Primary source map

### Design language

- `docs/design/overview.md` — positioning, six principles, surface map, common mistakes, reading order, evidence policy, asset boundary.
- `docs/design/foundations/color.md` — neutral scale, signal and semantic colors, theme inversion, contrast, forced colors, theme takeover.
- `docs/design/foundations/typography.md` — font roles, type scale, Chinese/Latin pairing, technical microcopy.
- `docs/design/foundations/shape.md` — shape semantics, radii, borders, shadows, cut corners, contrast between shape families.
- `docs/design/foundations/layout.md` — off-center composition, page skeletons, spacing, breakpoints, responsive rules.
- `docs/design/foundations/motion.md` — timing, easing, state transitions, entrance and exit behavior, reduced motion.
- `docs/design/foundations/texture.md` — texture inventory, contrast budget, restraint rules.
- `docs/design/foundations/iconography.md` — icon grid, stroke and fill behavior, status treatment.
- `docs/design/foundations/imagery.md` — image roles, processing, crop and fallback behavior.

### Recurring motifs

- `docs/design/elements/corner-and-wedge.md`
- `docs/design/elements/brackets-and-markers.md`
- `docs/design/elements/stripes-and-strips.md`
- `docs/design/elements/section-title.md`
- `docs/design/elements/ghost-and-micro-text.md`
- `docs/design/elements/grid-contour-dots.md`
- `docs/design/elements/hud-overlays.md`

### Surface families

- `docs/design/surfaces/website.md` — official website surface; measured evidence.
- `docs/design/surfaces/cloud.md` — cloud-game page; measured evidence and documented deviations from the website system.
- `docs/design/surfaces/game-ui.md` — in-game interface; community-weighted evidence.
- `docs/design/surfaces/promotional.md` — promotional/editorial material; observation plus community evidence.

### Components and implementation

- `docs/design/components/README.md` — component taxonomy, shared sizes, states, themes, links, accessibility, implementation order.
- `docs/design/components/button.md`
- `docs/design/components/navigation.md`
- `docs/design/components/card.md`
- `docs/design/components/form.md`
- `docs/design/components/feedback.md`
- `docs/design/components/overlay.md`
- `docs/design/components/data-display.md`
- `packages/ui/src/styles/theme.css` — semantic and raw tokens, motion variables, keyframes, theme inversion, reduced motion.
- `packages/ui/src/styles/utilities.css` — motif utility implementations.
- `packages/ui/src/components/README.md` — component conventions and implementation notes.
- `packages/ui/src/components/*` — component source and tests.

### Examples and checks

- `apps/docs/stories/ContentPage.stories.tsx` — website-style composition.
- `apps/docs/stories/DispatchPage.stories.tsx` — dense application shell and data surface.
- `apps/docs/stories/SettingsPage.stories.tsx` — form and feedback flow.
- `apps/docs/stories/ListPage.stories.tsx` — search, filtering, grid/list, pagination, and responsive behavior.
- `apps/docs/stories/DepotPage.stories.tsx` — game-like page using the main component system.
- `apps/docs/stories/GameStylePage.stories.tsx` — separate game-style entry; treat as a boundary case.
- `apps/docs/browser-checks/*.check.ts` — browser-level behavior, theme, responsive, accessibility, and forced-colors checks.

## Asset and rights boundary

`NOTICE.md` states that the repository's original documents, diagrams, tokens, component code, and original icons are MIT-licensed, while the separate game-style entry contains 30 official images without a license grant. The skill must not copy those images, logos, screenshots, proprietary fonts, or other official assets into `assets/`.

Use the source project's original SVG diagrams only as research references. When a visual example is needed inside this skill, create a self-authored diagram or use clearly marked placeholder content.

## Conflict resolution

When sources disagree, use this order:

1. A direct measured value in the relevant surface's measurement file.
2. The surface-specific design document.
3. The shared foundation document.
4. Component documentation and implementation.
5. Storybook examples and browser checks.
6. Community references and inference.

Record the disagreement and its resolution in the relevant reference instead of silently normalizing it.
