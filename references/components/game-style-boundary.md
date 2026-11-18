# Game 实机风格边界

来源：`docs/design/game/README.md` 及其六篇控件文档。它是独立入口，不属于主组件库的官网气质默认值。

## 独立控件

- `AnimatedDialog`：分段入场的装饰弹窗。
- `RoundedSelect`：圆角触发器与灰色下拉面板。
- `RoundedButton` / `RoundedIconButton`：固定灰黄语气的圆角行动控件。
- `RoundedToggle` / `RoundedSwitch`：文字分段选择和 ON/OFF 开关。
- `BannerAlert` / `FullWidthAlert`：紧凑卡片与通栏确认提示。
- `ItemCard` / `ItemIcon`：稀有度、库存、分层图标和亮暗背景。
- `ItemTooltipCard` / `ItemHoverCard`：物品详情和悬浮预览。
- `EndfieldSplashScreen`：填入官方开屏素材的独立入口。

## 与主组件系统的区别

主入口默认支持亮/暗主题、语义令牌、可换主题色和官网工业编辑风；Game 入口是固定的灰黄游戏内语气，不随主主题翻转。不要把主入口按钮自动改成圆角游戏按钮，也不要把 Game 的官方图片扩散到主入口。

## 版权与实现

源仓库的 Game 入口包含 30 张官方图片，来自官方页面或社区转存，未授予使用方额外权利；MIT 许可不覆盖这些图片。创建 Skill 的示意、测试和生成物只使用原创几何、用户提供的素材或明确标注的占位图。

若用户明确要复现游戏 UI：

1. 先说明这是独立的游戏风格路线，并读取本文件和源仓库 Game 文档。
2. 优先复现布局、形状、稀有度层级、状态和交互，不复制官方素材。
3. 在交付报告里标记哪些规则是社区证据、哪些是推断。
4. 对任何官方 Logo、立绘、截图、字体或图片使用要求，保留用户的授权边界并提示核实权利。
