# Extraction Matrix

Use this matrix to prevent the skill from becoming a visual summary that omits implementation decisions. Mark a row complete only after reading the named source and checking the corresponding code or story where applicable.

| Area | Primary source | Implementation cross-check | Story/example cross-check | Status |
| --- | --- | --- | --- | --- |
| Design philosophy and six principles | `docs/design/overview.md` | `README.md` | `ContentPage`, `DispatchPage` | complete for survey |
| Website surface | `docs/design/surfaces/website.md` | `theme.css`, core components | `ContentPage` | pending extraction |
| Cloud surface | `docs/design/surfaces/cloud.md` | button and surface tokens | `SettingsPage` / cloud references | pending extraction |
| Game UI surface | `docs/design/surfaces/game-ui.md` | main tokens plus `src/game` boundary | `DepotPage`, `GameStylePage` | pending extraction |
| Promotional surface | `docs/design/surfaces/promotional.md` | motif utilities | steps and editorial examples | pending extraction |
| Color | `docs/design/foundations/color.md` | `theme.css` | theme takeover and switch stories | pending extraction |
| Typography | `docs/design/foundations/typography.md` | `theme.css` font and text tokens | page and section-title stories | pending extraction |
| Shape | `docs/design/foundations/shape.md` | `theme.css`, `utilities.css` | motif stories and button/card stories | pending extraction |
| Layout | `docs/design/foundations/layout.md` | layout classes in stories | all four page stories | pending extraction |
| Motion | `docs/design/foundations/motion.md` | keyframes in `theme.css` and `motion.ts` | browser motion checks | pending extraction |
| Texture | `docs/design/foundations/texture.md` | `utilities.css`, `Texture` | motif stories | pending extraction |
| Iconography | `docs/design/foundations/iconography.md` | `packages/ui/src/icons` | icon button and navigation stories | pending extraction |
| Imagery | `docs/design/foundations/imagery.md` | image helpers and media components | content/list page stories | pending extraction |
| Corner and wedge motifs | `docs/design/elements/corner-and-wedge.md` | `utilities.css`, tabs/item slot | `CornerAndWedge` story | pending extraction |
| Brackets and markers | `docs/design/elements/brackets-and-markers.md` | `CornerBrackets`, `BracketTitle` | motif stories | pending extraction |
| Stripes and strips | `docs/design/elements/stripes-and-strips.md` | `Hatch`, `HazardStripe`, `RegistrationStrip` | motif stories | pending extraction |
| Section title | `docs/design/elements/section-title.md` | `SectionTitle` | section-title stories | pending extraction |
| Ghost and micro text | `docs/design/elements/ghost-and-micro-text.md` | `GhostText` | motif stories and page headers | pending extraction |
| Grid, contour, dots | `docs/design/elements/grid-contour-dots.md` | `Texture` and utilities | texture stories | pending extraction |
| HUD overlays | `docs/design/elements/hud-overlays.md` | `Viewfinder`, `TickRing`, `RecIndicator` | motif stories | pending extraction |
| Component sizes and states | `docs/design/components/README.md` | component source/tests | component stories | pending extraction |
| Buttons and navigation | `docs/design/components/button.md`, `navigation.md` | button/nav components | controls and `DispatchPage` | pending extraction |
| Cards, panels, media | `docs/design/components/card.md` | card/panel components | `ContentPage`, `ListPage` | pending extraction |
| Forms | `docs/design/components/form.md` | form components and tests | `SettingsPage` | pending extraction |
| Feedback | `docs/design/components/feedback.md` | feedback components | `SettingsPage`, `DepotPage` | pending extraction |
| Overlays | `docs/design/components/overlay.md` | Base UI-backed components | overlay stories and browser checks | pending extraction |
| Data display | `docs/design/components/data-display.md` | table/data components | `DispatchPage`, `ListPage` | pending extraction |
| Game-style boundary | `docs/design/game/README.md` | `packages/ui/src/game` | `GameStylePage` | pending extraction |
| Anti-patterns and rights | `overview.md`, `NOTICE.md` | package boundary | all examples | pending extraction |

## Completion rule

An area is complete for the skill only when the reference rule, implementation behavior, and at least one realistic composition have been compared. If a cross-check is unavailable, record the exact missing path in `PROJECT_PROGRESS.md`.
