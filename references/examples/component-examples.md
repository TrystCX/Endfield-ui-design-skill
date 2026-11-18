# 组件案例

从源仓库 Storybook 的组件故事中提取的复用方式：

- `Button`：展示 `action`、`control`、`light`、`danger` 与 `sm/md/lg`，并验证 hover、pressed、focus、disabled、loading、icon-start 和 link 形态。
- `SectionTitle`：展示标准、色带和竖排侧签；在窄容器中测试英文长词换行和装饰隐藏。
- `Tabs`：展示标准、胶囊和楔形变体；当前项以箭头、底块或填充表达。
- `Panel` / `List`：展示表面差、单边线、列表选中与深色行带；避免每行独立阴影。
- `Field` / `Input` / `Select`：展示帮助、错误、禁用、焦点和不同主题面板。
- `Dialog` / `Drawer` / `Popover`：展示触发方向、遮罩、Escape、焦点回收和窄屏宽度。
- `Table` / `DataRow` / `Stat`：展示密集读数、排序、展开、语义色和横向滚动。
- `Texture` / `CornerBrackets` / `Viewfinder`：展示装饰层的 `aria-hidden`、不挡点击、低对比和主题继承。

在其他技术栈中保留这些视觉与交互约束，替换渲染、状态和路由机制即可。
