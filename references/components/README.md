# 组件证据索引

来源：`docs/design/components/README.md`、`button.md`、`navigation.md`、`card.md`、`form.md`、`feedback.md`、`overlay.md`、`data-display.md`，并与 `packages/ui/src/components/` 和 `apps/docs/stories/` 交叉检查。

## 通用规格

| 档位 | 高度 | 字号 | 水平内边距 | 典型用途 |
| --- | --- | --- | --- | --- |
| `sm` | 32px | 14px | 12px | 工具栏、表格内、紧凑面板 |
| `md` | 40px | 16px | 16px | 默认控件 |
| `lg` | 56px | 20px | 24px | 首屏行动、移动端主要按钮 |

交互组件按需覆盖：默认、悬停、按下、`focus-visible`、选中/当前、禁用、加载、错误、成功和空状态。状态不能只靠颜色表达；加载不能造成布局跳动；点击区域至少 40 × 40px。

## 组件族与来源

| 组件族 | 设计文档 | 实现目录 | 组合案例 |
| --- | --- | --- | --- |
| Button / IconButton / ButtonGroup / Toolbar | `button.md` | `components/button`, `icon-button`, `toolbar` | `DispatchPage`, button stories |
| SideRail / TopBar / NavMenu / Tabs / Pagination | `navigation.md` | `side-rail`, `top-bar`, `nav-menu`, `tabs`, `pagination` | `DispatchPage`, navigation stories |
| Panel / Accordion / MediaCard / Carousel / ImageViewer / ItemSlot | `card.md` | corresponding component directories | `ContentPage`, `ListPage`, `DepotPage` |
| Field / Input / Select / Combobox / Choice / Slider / DatePicker | `form.md` | corresponding component directories | `SettingsPage`, form stories |
| Alert / Toast / Progress / Loader / EmptyState / CompletionBanner | `feedback.md` | corresponding component directories | `SettingsPage`, `DepotPage` |
| Dialog / Drawer / DropdownMenu / Popover / HoverCard / FlyoutBar | `overlay.md` | corresponding component directories | overlay stories, `DispatchPage` |
| Tag / Badge / Stat / Table / DataRow / Timeline / Schedule | `data-display.md` | corresponding component directories | `DispatchPage`, `ListPage` |

## API translation rules

- Use semantic variants such as `action`, `control`, `light`, `danger`; do not expose raw color names.
- Use `sm`, `md`, `lg`; do not expose arbitrary radius and cut switches for every component.
- Use `tone="neutral|info|success|warning|danger"` for semantic status.
- Native elements are preferred for buttons, links, and form controls. Complex overlays and focus management may use an accessibility primitive equivalent to Base UI.
- A link-capable component should preserve `href` or accept the target framework's link-rendering hook without changing its visual semantics.
- Decorative brackets, textures, ghost text, and registration strips are hidden from assistive technology.
- Keep `data-theme="dark"` and `data-theme="inverse"` at the surface/container level so components consume semantic tokens.

## Reading order for implementation

1. Read the relevant component document for purpose, state, behavior, accessibility, and do/don't rules.
2. Inspect the matching source directory for actual DOM, token usage, and motion.
3. Inspect its tests for keyboard, disabled, error, and edge behavior.
4. Inspect the matching Storybook story for visual variants and narrow-container behavior.
5. Inspect the relevant browser check before claiming responsive or interaction correctness.
