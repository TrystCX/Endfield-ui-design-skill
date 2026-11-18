# 色彩

来源：`docs/design/foundations/color.md` 与 `packages/ui/src/styles/theme.css`。数值保留原始十六进制；主题和表面变化使用语义令牌。

## 基本规则

- 大面积只用中性色；信号色只表达行动、当前项、选中或进度。
- 角色色各有职责，不能互相替代，也不能作为无意义装饰。
- 主题色可以接管 `action` 相关令牌；`danger`、`success`、`warning` 的语义不能丢。
- 每个文字、边线和填充都在它实际所在的表面上验算对比度。

## 中性色阶

| 令牌 | 值 | 典型用途 |
| --- | --- | --- |
| `neutral-0` | `#FFFFFF` | 页面底、导航轨 |
| `neutral-50` | `#FAFAFA` | 卡片、弹窗、翻页钮 |
| `neutral-100` | `#F2F2F2` | 凹陷区、标签值底、图标钮底 |
| `neutral-200` | `#E6E6E6` | 悬停底、激活底、分页条 |
| `neutral-300` | `#D9D9D9` | 分隔线、未激活图标 |
| `neutral-400` | `#B3B3B3` | 强分隔线、禁用文字、装饰线稿 |
| `neutral-500` | `#8A8A8A` | 三级文字、括号、装饰 |
| `neutral-600` | `#626262` | 次级文字 |
| `neutral-700` | `#484848` | 中性控件悬停 |
| `neutral-800` | `#383838` | 中性控件底、深色标签 |
| `neutral-850` | `#282828` | 中性控件按下 |
| `neutral-900` | `#191919` | 主文字、反转块 |
| `neutral-950` | `#141414` | 标题、暗色页面底 |

官网灰阶是纯灰。纯黑 `#000000` 只用于暗色主题的最深凹陷区或需要完全压暗的版块。

## 信号与角色色

| 令牌 | 值 | 语义 |
| --- | --- | --- |
| `signal` | `#FFFA00` | 行动、当前导航、选中环、进度填充 |
| `signal-pressed` | `#EEEA00` | 黄色控件按下态 |
| `signal-deep` | `#E6DE01` | 黄底分隔线或更深按下档 |
| `signal-ink` | `#6B5D00` | 亮色表面上的强调文字 |
| `notice` | `#FC6C00` | 通知、倒计时、数量 |
| `gain` | `#BCE41D` | 增益与数值增加 |
| `data` | `#2A84B4` | 量值图表、流程数据 |
| `region` | `#06A2A2` | 地区或机构主题 |
| `alert` | `#F62A2A` | 危险；不作普通装饰 |
| `confirm` | `#00D872` | 成功、确认、充裕 |
| `special` | `#904EF0` | 特殊、战术或高稀有度 |
| `rarity-1..4` | 蓝、紫、金、橙 | 稀有度阶梯 |

黄色在白底上的对比度只有 1.11:1，不能直接当正文或细线。黄底压 `neutral-900`；亮底上的强调文字使用 `signal-ink`；暗色表面上的强调文字可直接用 `signal`。

## 亮暗主题与反转块

亮色主题默认：`surface #FFFFFF`、`surface-raised #FAFAFA`、`surface-sunken #F2F2F2`、`ink #191919`。暗色主题默认：`surface #141414`、`surface-raised #1F1F1F`、`surface-sunken #000000`、`ink #FAFAFA`。

组件使用 `surface`、`ink`、`action`、`accent-ink`、`button` 等语义令牌；不要在组件里写固定十六进制色。反转块使用局部 `data-theme="inverse"`，让表面、文字、焦点和控件按反面主题取值。

## 主题色接管

局部主题只覆盖 `action`、`action-pressed`、`accent-ink`、`accent-ink-inverse` 四类令牌，并重新验算对比度。危险、成功和警告不随主题接管。一个界面通常只有一个主导主题色；字体和纹理可以随主题改变，但不应只做机械换色。

## 常见错误

- 把黄色铺满背景或给每张卡片加黄色描边。
- 在白底上使用黄色正文、黄色细线或黄色禁用态。
- 用橙色表示错误、用红色做普通装饰、用彩虹色替代语义。
- 使用颜色名作为组件 API（如 `color="yellow"`），应使用 `variant="action"` 或 `tone="danger"`。
