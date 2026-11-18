# Endfield UI Design Skill Progress

## Project status

- Current phase: Phase 5 — packaged for GitHub and ready for distribution
- Skill name: `endfield-ui-design`
- Skill version: `0.4.0-github-package`
- Started: 2026-11-18
- Source repository snapshot: `icaruszezen/endfield-ui`
- Verified upstream commit: `68c81171caa644ed73e98cb1d13c78439930c1f6`

## Repository survey

The local snapshot at `endfield-ui-main/` matches the verified upstream `main` tree at the commit above:

- 760 files in the upstream tree
- 760 local files
- No path differences
- No content mismatches after comparing Git blob hashes
- 39 design Markdown documents
- 35 original SVG diagrams in `docs/design/assets/`
- 86 UI component directories
- 109 Storybook story files
- 30 game-style image assets

The snapshot contains the working tree but not the upstream Git history. Commit-level provenance is therefore recorded from the GitHub API, while file content is verified against the upstream tree.

## Source priority

1. `endfield-ui-main/docs/design/`
2. `endfield-ui-main/packages/ui/`
3. `endfield-ui-main/apps/docs/`
4. Example stories and screenshots
5. `README.md`, `CHANGELOG.md`, `ROADMAP.md`, `NOTICE.md`

## Evidence policy

Preserve the source project's four levels without upgrading them:

- `实测` — a value read directly from a measured public page
- `观察` — a visible phenomenon observed in public material
- `社区` — a project-author or community conclusion not independently verified here
- `推断` — a recommendation made by the design documentation

Every extracted rule must keep its source level and point to the original file. A rule derived from implementation behavior may be recorded as implementation evidence, but it must not be presented as an official visual fact.

## Confirmed material

- `docs/design/overview.md` defines the industrial editorial positioning, six principles, three primary surfaces, the cloud-page exception, document map, evidence levels, and asset boundary.
- `docs/design/foundations/` contains Color, Typography, Shape, Layout, Motion, Texture, Iconography, and Imagery.
- `docs/design/elements/` contains the seven recurring motifs required by the project brief.
- `docs/design/surfaces/` separates website, cloud, game UI, and promotional surfaces.
- `docs/design/components/` defines component families, sizes, states, behavior, accessibility, and do/don't guidance.
- `docs/design/game/` defines a separate game-style entry and its asset risk boundary.
- `packages/ui/src/styles/theme.css` is the implementation source of truth for semantic and raw tokens.
- `packages/ui/src/styles/utilities.css` contains reusable motif utilities.
- `packages/ui/src/components/` contains the implementation and unit tests for the component system.
- `apps/docs/stories/` contains individual component states plus complete page compositions.
- `apps/docs/browser-checks/` contains browser-level checks for interaction, responsive behavior, themes, and forced colors.

## Open gaps to resolve

- The local snapshot does not include upstream commit history or issue discussion.
- Game UI evidence is intentionally community-weighted; do not rewrite it as measured fact.
- The source project's browser checks are available; independent forward tests are now recorded under `endfield-ui-design/tests/`.
- The skill must remain usable outside React and Tailwind; source implementation patterns need to be translated into framework-neutral decisions. The first cross-stack guidance is now recorded, but needs forward testing.
- Official images in `packages/ui/src/game` must not be copied into this skill's assets. Use original diagrams or generated placeholders instead.

## Planned phases

1. Survey and evidence registration — this document and `endfield-ui-design/references/evidence-and-sources.md`.
2. Extract the design system — philosophy, surfaces, foundations, motifs, tokens, components, and anti-patterns. (complete for current source snapshot)
3. Write the cross-stack skill — concise router in `SKILL.md`, detailed references loaded on demand. (complete for current source snapshot)
4. Run forward tests — new page, migration, isolated components, themes, breakpoints, and surface separation. (complete for first pass)
5. Revise, validate, package, and install — quick validation, artifact review, installation into the user's Codex skills directory, and standalone GitHub packaging. (complete for current source snapshot)

## Next actions

- Continue component-specific source cross-checks when a future revision needs a deeper rule.
- Re-run the browser fixture after any future change to tokens, routing, or surface separation.
- Add framework-specific adapters only when a real target project requires them.

## Completed in the current phase

- Added `references/design-philosophy.md` and `references/design-surfaces.md`.
- Added all eight foundation references under `references/foundations/`.
- Added all seven motif references under `references/elements/`.
- Added `references/token-inventory.md` with semantic, raw, typography, shape, motion, and layer tokens.
- Added component guidance, page examples, component examples, anti-patterns, and visual checklist.
- Added the independent Game-style boundary reference covering its controls, fixed theme, and 30-image rights boundary.
- Installed the verified skill into the local Codex skills directory and compared all 44 source/installed file hashes.
- Created the standalone `endfield-ui-design-github` package with GitHub README, license, notice, ignore rules, and an initial repository commit.
- Updated `SKILL.md` with routing, surface separation, evidence, rights, and verification instructions.
- Ran a manual repository inventory against the verified upstream tree.

## Forward-test results

The framework-free fixture at `endfield-ui-design/tests/` was served locally and inspected in a real browser. It uses original CSS geometry and no official assets.

- New website-family page: verified visually at desktop and mobile sizes.
- Before/after migration: verified; the after state uses asymmetry, semantic signal color, edge information, and less card uniformity.
- Independent components: verified; buttons, form field, navigation state, success feedback, and data role are present and keyboard focus moves to the field.
- Light/dark themes: verified by real browser toggle and screenshot inspection.
- Responsive widths: verified automatically at 375×900, 768×900, 1280×900, and 1920×900; all report no horizontal overflow.
- Surface separation: verified visually; website, game UI, and promotional cards have different base, density, shape, and editorial treatment.
- Known polish note: at 375px the sticky topbar actions wrap into two rows. They remain visible and usable; this is recorded rather than hidden with overflow.

## Validation notes

- The bundled runtime initially lacked `PyYAML`, and its Windows namespace resolution made the temporary package import unusable.
- The official validator was then rerun with a UTF-8-compatible minimal YAML shim and passed: `Skill is valid!`.
