---
name: endfield-ui-design
description: "Design, restyle, or audit interfaces using the Endfield UI industrial editorial design language derived from the endfield-ui research repository. Use when the task explicitly asks for Endfield UI, industrial editorial, or this skill's design system; do not activate for generic sci-fi styling or for copying official game assets."
---

# Endfield UI Design

Use this skill to transfer a visual system across web, app, dashboard, editorial, and game-like interface work while preserving the target project's framework, content, accessibility, and interaction requirements.

## Start here

Before choosing motifs, identify:

1. The job: build a new surface, restyle an existing surface, or audit a result.
2. The dominant surface family: website, cloud page, game UI, or promotional material.
3. The content-led focal anchor, information density, theme, and one structural signature.
4. The target stack and existing tokens/components that should be reused.

Read only the references needed for the job:

- Evidence, source levels, and rights boundary → [evidence-and-sources.md](references/evidence-and-sources.md)
- Extraction coverage and source cross-checks → [extraction-matrix.md](references/extraction-matrix.md)
- Design philosophy and surface choice → [design-philosophy.md](references/design-philosophy.md) and [design-surfaces.md](references/design-surfaces.md)
- Foundations → `references/foundations/` and [token-inventory.md](references/token-inventory.md)
- Motifs → `references/elements/`
- Components → [components/README.md](references/components/README.md), plus the family guides in `references/components/`
- Game-style UI and image rights boundary → [game-style-boundary.md](references/components/game-style-boundary.md)
- Examples, anti-patterns, and verification → `references/examples/`

## Stable decisions

- Treat paper, ink, and a signal color as the base language; color has semantic roles.
- Derive the macro layout from the content before adding cuts, wedges, brackets, grids, stripes, ghost type, or HUD overlays.
- Keep the four surface families distinct. The website and cloud page are not interchangeable, and game-style UI is a separate system with a separate asset boundary.
- Use shape, typography, texture, and motion to communicate meaning. Do not apply every motif to every component.
- Keep evidence labels attached to rules. A community observation or inference must not be rewritten as a measured fact.
- Use original or user-supplied imagery. Do not copy official logos, screenshots, character art, proprietary fonts, or the 30 official images in the source repository's game entry.

## Build and audit

For new work, state the selected surface family, theme anchor, signature, and intentionally omitted motifs before implementation. For restyling, preserve content, routes, data, and information architecture unless the user asks otherwise. For audits, report concrete issues by file/selector/region and classify them as structure, semantic color/shape, density, accessibility, responsive behavior, or rights boundary.

Implement the states the artifact needs: default, hover where applicable, focus-visible, selected, disabled, loading, empty, error, and success. Verify keyboard access, readable contrast, long-content wrapping, reduced motion, and narrow/wide layouts.

Before handoff, run the relevant checks in [visual-checklist.md](references/examples/visual-checklist.md). A page must still have a clear hierarchy when yellow and decorative texture are removed, and it must not mix website, game UI, and promotional conventions without an explicit reason.
