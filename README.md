# Endfield UI Design

`endfield-ui-design` is a Codex skill for designing, restyling, and auditing interfaces with the industrial editorial language documented by the [`icaruszezen/endfield-ui`](https://github.com/icaruszezen/endfield-ui) research repository.

The skill is framework neutral. It keeps website pages, cloud-game pages, game-style UI, and promotional material as separate surface families, and it records whether a rule is measured, observed, community-sourced, or inferred.

## Install

Copy this repository's skill files into your Codex skills directory:

```powershell
$skillsRoot = if ($env:CODEX_HOME) {
  Join-Path $env:CODEX_HOME 'skills'
} else {
  Join-Path $HOME '.codex\skills'
}

Copy-Item -Path .\SKILL.md, .\agents, .\references -Destination (Join-Path $skillsRoot 'endfield-ui-design') -Recurse -Force
```

The skill is automatically discoverable for requests that explicitly ask for Endfield UI, industrial editorial UI, or this design system. It should not activate for generic sci-fi styling or for copying official game assets.

## Contents

- `SKILL.md` — the concise routing and execution instructions.
- `references/` — design philosophy, surfaces, foundations, motifs, tokens, components, examples, evidence, and rights guidance.
- `tests/` — a framework-free forward-test fixture with screenshots and recorded results.
- `PROJECT_PROGRESS.md` — source survey, evidence policy, and validation record.
- `NOTICE.md` — provenance, nonofficial status, and asset boundary.

## Validate

Run the bundled skill validator from a Codex installation:

```powershell
python "$HOME\.codex\skills\.system\skill-creator\scripts\quick_validate.py" .
```

To inspect the forward-test fixture locally:

```powershell
python -m http.server 8000 --directory .\tests
```

Then open `http://localhost:8000` in a browser. The fixture uses original text and CSS geometry; it does not bundle official game images, logos, or fonts.

## GitHub upload

This folder is already a standalone Git repository with an initial commit. After creating an empty GitHub repository, replace the placeholder remote and push:

```powershell
git remote add origin https://github.com/<your-account>/<your-repository>.git
git branch -M main
git push -u origin main
```

## Scope and rights

This is an unofficial design-system skill. It does not represent Hypergryph, GRYPHLINE, or any rights holder. Do not add official screenshots, character art, logos, proprietary fonts, or other game assets to this repository. See `NOTICE.md` before publishing derivative work.
