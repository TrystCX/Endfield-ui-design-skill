# 按钮与导航

来源：`docs/design/components/button.md`、`navigation.md`，以及 `packages/ui/src/components/button`, `side-rail`, `top-bar`, `tabs`, `pagination`。

## 变体

`action` 表达主要行动；`control` 表达中性控制；`light` 表达浅色或辅助行动；`danger` 表达不可逆或风险操作；`text` 仅在已有清晰上下文时使用。用 `sm/md/lg` 表示密度，形状由变体决定，不提供任意圆角/切角组合。

## 状态与行为

默认、hover、pressed、focus-visible、disabled、loading 和 link 形态必须保持尺寸稳定。加载时保留图标/占位位置，避免布局跳动。链接形态保留可访问的当前状态和禁用语义；路由接入应通过渲染钩子或适配器，不复制按钮样式。

侧轨适合宽屏高频导航，窄屏转换为顶栏 + 全屏菜单；展开文字浮在主舞台上，不推挤内容。当前项优先用滑动底块、左缘条或填充反转。页签、分页和导航器分别承担章节、页码和短状态，不要互换语义。

## 实现与验收

优先使用原生 `button` / `a`，图标按钮必须有 accessible name，焦点环在切角外层。检查键盘顺序、触屏命中区、悬停不可用时的等价操作、窄屏菜单和当前项语义。

## 避免

- 用黄色边框包住所有按钮。
- 悬停放大、上浮或增加巨大阴影。
- 把侧轨在手机上缩成不可读的窄列。
- 用颜色名作为公共 API。
