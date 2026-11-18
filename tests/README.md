# Forward Test Plan

The fixture in `index.html` is a real framework-free implementation of the first Skill pass. It uses original CSS geometry and text, not source-repository official images.

| Test | Evidence target | Result |
| --- | --- | --- |
| 1. New page | Website-family page with a content-led hero, signal budget, and asymmetry | `verified` — desktop screenshot inspected |
| 2. Style migration | Generic card layout becomes semantic industrial editorial structure | `verified` — before/after pair inspected at desktop and mobile |
| 3. Independent components | Button, form, navigation, feedback, and data states remain usable alone | `verified` — DOM state inspected; main action moves focus to the field |
| 4. Light/dark themes | Semantic tokens preserve hierarchy and readable states | `verified` — real browser toggle inspected in both themes |
| 5. Responsive widths | Rail/topbar change, grids collapse, no page-level horizontal overflow | `verified` — automated widths 375/768/1280/1920 all report no overflow |
| 6. Surface separation | Website, game UI, and promotional language remain visibly distinct | `verified` — three surface cards inspected and compared |

## Run evidence

- Browser: Microsoft Edge executable, headless automation for repeatable checks; ChatGPT in-app browser for visual inspection.
- Viewports checked: 375×900, 768×900, 1280×900, 1920×900.
- Automated output: `artifacts/results.json`.
- Inspected screenshots: `artifacts/fixture-375.png`, `artifacts/fixture-768.png`, desktop in-browser screenshot, and dark-theme in-browser screenshot.
- Observed issue: at 375px the action controls wrap into two rows in the sticky topbar. This is intentional and remains usable; it is recorded for a later polish pass rather than hidden with overflow.

Record browser dimensions, observed defects, and fixes here. A screenshot generated without visual inspection is not a passing result.
