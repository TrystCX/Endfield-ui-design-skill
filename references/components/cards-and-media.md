# 卡片、面板与媒体

来源：`docs/design/components/card.md` 与 `Panel`, `MediaCard`, `Carousel`, `ImageViewer`, `ItemSlot`, `List` 实现。

## 选择容器

- `Panel`：内容分组和章节容器，优先表面差与单条边线。
- `List` / `DataRow`：同类内容与可比较数据，选中态用整行语义，不给每行独立卡片阴影。
- `MediaCard`：图像、标题、类型和日期；播放记号是小黄色方块。
- `Carousel`：一组内容的连续查看；翻页圆钮和计数承担方向。
- `ImageViewer`：在原比例、焦点和键盘可达的弹层内查看大图。
- `ItemSlot`：矩阵资源和库存；可选中、聚焦、锁定、稀有度和新标记，但必须保持可比较的格子尺度。

## 状态与响应式

支持默认、hover、selected、disabled、loading、empty、error 和 expanded（适用时）。媒体、长标题和标签在窄容器里换行或在自己的区域滚动；不要把整个页面撑宽。卡片图片失败时保留标题、类型和行动。

## 避免

- 所有内容一律包成卡片。
- 用玻璃、发光和厚重阴影制造层级。
- 用大半透明圆形播放按钮覆盖媒体。
- 让装饰边框影响内容尺寸或焦点。
