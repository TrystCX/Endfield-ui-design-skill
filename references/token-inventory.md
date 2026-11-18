# 设计令牌清单

来源：`endfield-ui-main/packages/ui/src/styles/theme.css`。这是转译时的参考快照；如源码与本文件不一致，以 `theme.css` 为准。令牌应映射到目标技术栈的语义变量，不要把这些值散落到组件实现中。

## 语义表面与状态

### 亮色主题

| 令牌 | 值 |
| --- | --- |
| `surface` | `#FFFFFF` |
| `surface-raised` | `#FAFAFA` |
| `surface-sunken` | `#F2F2F2` |
| `surface-muted` | `#E6E6E6` |
| `surface-inverse` | `#191919` |
| `ink` | `#191919` |
| `ink-secondary` | `#626262` |
| `ink-tertiary` | `#8A8A8A` |
| `ink-disabled` | `#B3B3B3` |
| `ink-inverse` | `#FFFFFF` |
| `line` | `#D9D9D9` |
| `line-strong` | `#B3B3B3` |
| `action` | `#FFFA00` |
| `action-pressed` | `#EEEA00` |
| `on-action` | `#191919` |
| `accent-ink` | `#6B5D00` |
| `accent-ink-inverse` | `action` |
| `control` | `#383838` |
| `control-hover` | `#484848` |
| `control-pressed` | `#282828` |
| `on-control` | `#EEEEEE` |
| `button` | `#383838` |
| `button-hover` | `#484848` |
| `button-pressed` | `#282828` |
| `on-button` | `#EEEEEE` |
| `disabled` | `#B3B3B3` |
| `on-disabled` | `#626262` |
| `focus` | `#191919` |
| `scrim` | `rgb(0 0 0 / 0.5)` |
| `danger` | `#DE0909` |
| `success` | `#007F43` |
| `warning` | `#B74E00` |
| `info` | `#25759F` |

### 暗色主题

| 令牌 | 值 |
| --- | --- |
| `surface` | `#141414` |
| `surface-raised` | `#1F1F1F` |
| `surface-sunken` | `#000000` |
| `surface-muted` | `#282828` |
| `surface-inverse` | `#FAFAFA` |
| `ink` | `#FAFAFA` |
| `ink-secondary` | `#B3B3B3` |
| `ink-tertiary` | `#8A8A8A` |
| `ink-disabled` | `#626262` |
| `ink-inverse` | `#191919` |
| `line` | `#383838` |
| `line-strong` | `#626262` |
| `action` | `#FFFA00` |
| `action-pressed` | `#EEEA00` |
| `on-action` | `#191919` |
| `accent-ink` | `#FFFA00` |
| `accent-ink-inverse` | `#6B5D00` |
| `control` | `#383838` |
| `control-hover` | `#484848` |
| `control-pressed` | `#282828` |
| `on-control` | `#EEEEEE` |
| `button` | `rgb(255 255 255 / 0.2)` |
| `button-hover` | `rgb(255 255 255 / 0.3)` |
| `button-pressed` | `rgb(255 255 255 / 0.15)` |
| `on-button` | `#D9D9D9` |
| `disabled` | `#282828` |
| `on-disabled` | `#626262` |
| `focus` | `#FFFA00` |
| `scrim` | `rgb(0 0 0 / 0.7)` |
| `danger` | `#F74040` |
| `success` | `#00D872` |
| `warning` | `#FC6C00` |
| `info` | `#2D8FC2` |

`data-theme="inverse"` swaps the surface, ink, accent, button, focus, scrim, and status groups using the inherited opposite-theme values. Nested inverse blocks do not keep flipping indefinitely.

## Raw color tokens

| Group | Tokens |
| --- | --- |
| Neutrals | `neutral-0 #FFFFFF`, `neutral-50 #FAFAFA`, `neutral-100 #F2F2F2`, `neutral-200 #E6E6E6`, `neutral-300 #D9D9D9`, `neutral-400 #B3B3B3`, `neutral-500 #8A8A8A`, `neutral-600 #626262`, `neutral-700 #484848`, `neutral-800 #383838`, `neutral-850 #282828`, `neutral-900 #191919`, `neutral-950 #141414` |
| Signal | `signal #FFFA00`, `signal-pressed #EEEA00`, `signal-deep #E6DE01`, `signal-ink #6B5D00` |
| Roles | `notice #FC6C00`, `gain #BCE41D`, `data #2A84B4`, `region #06A2A2`, `alert #F62A2A`, `confirm #00D872`, `special #904EF0` |
| Alert fill | `alert-fill #DE0909`, `alert-fill-hover #C40808`, `alert-fill-pressed #A80707` |
| Rarity | `rarity-1 #24BAFC`, `rarity-2 #904EF6`, `rarity-3 #FCBA00`, `rarity-4 #FC6C00` |
| Registration | `reg-magenta #EC008C`, `reg-cyan #00AEEF`, `reg-yellow #FFF200` |

## Typography

| Group | Token | Value |
| --- | --- | --- |
| Font | `font-sans` | HarmonyOS Sans SC → Noto Sans SC → Source Han Sans SC → PingFang SC → Microsoft YaHei → system-ui |
| Font | `font-display` | Archivo → Montserrat → HarmonyOS Sans SC; width variation 125 |
| Font | `font-latin` | Outfit → Urbanist → HarmonyOS Sans SC |
| Font | `font-tech` | Space Grotesk → HarmonyOS Sans SC; tabular figures |
| Font | `font-mono` | JetBrains Mono → Cascadia Code → system monospace |
| Text | `micro` | 0.625rem / 1 |
| Text | `xs` | 0.75rem / 1.25 |
| Text | `sm` | 0.875rem / 1.4 |
| Text | `base` | 1rem / 1.6 |
| Text | `lg` | 1.25rem / 1.2 |
| Text | `xl` | 1.5rem / 1.1 |
| Text | `2xl` | 2rem / 1.1 |
| Text | `3xl` | 2.5rem / 1 |
| Text | `4xl` | 3.25rem / 1 |
| Text | `5xl` | 4.5rem / 1 |
| Text | `6xl` | 6rem / 1 |
| Text | `ghost` | `clamp(5rem, 10.4vw, 12.5rem)` / 1, letter spacing `-0.04em` |

Other text tokens: `tracking-ghost -0.04em`; `tracking-label 0.05em`.

## Shape, shadow, timing, layering

| Group | Tokens |
| --- | --- |
| Radius | `radius-xs 2px`, `radius-sm 4px`, `radius-md 6px`; use full radius for capsules and circles |
| Shadow | `shadow-xs 0 0 4px rgb(0 0 0 / .25)`, `shadow-sm 0 0 8px rgb(0 0 0 / .25)`, `shadow-md 0 0 12px rgb(0 0 0 / .3)`, `shadow-lg 0 0 24px rgb(0 0 0 / .3)`, `shadow-rail 0 0 12px rgb(0 0 0 / .1)` |
| Easing | `standard ease`, `emphasis ease-in-out`, `exit ease-out` |
| Duration | `instant 50ms`, `fast 200ms`, `base 300ms`, `slow 400ms`, `slower 600ms` |
| Motion shift | `motion-shift 4px`, `motion-shift-lg 8px` |
| Motif size | `cut-sm 6px`, `cut-md 10px`, `cut-lg 16px`, `hatch-size 6px` |
| Layers | `z-float 100`, `z-nav 200`, `z-overlay 300`, `z-toast 400`, `z-loader 1000` |

## Motion names

The source registers: `flicker`, `fill`, `scroll-hint`, `breathe`, `marquee`, `spin`, `spin-slow`, `blink`, `slide-in`, `turn-in`, `fade-in`, `indeterminate`, `indeterminate-y`, `pulse`, `bracket-in`, `shift-in`, and `wipe-in`.

Use them only when the corresponding state or content justifies the motion. Respect `prefers-reduced-motion: reduce`: animation and transition durations collapse to approximately zero, delays are removed, and scrolling becomes automatic.
