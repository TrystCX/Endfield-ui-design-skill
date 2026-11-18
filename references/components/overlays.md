# 浮层

来源：`docs/design/components/overlay.md` 与 Base UI-backed overlay components。

## 类型

- `Tooltip`：短说明，指针或键盘聚焦触发，不能承载关键操作。
- `Popover` / `HoverCard`：补充信息或轻操作，靠近触发元素。
- `DropdownMenu` / `ContextMenu`：命令集合，支持复选项和一层子菜单时明确层级。
- `Dialog`：需要确认或输入；`Drawer`：侧向工作区；`FlyoutBar`：短暂的边缘行动带。

## 通用行为

从触发侧以 4–8px 方向位移进入，遮罩和阴影服从表面主题。打开时把焦点放入浮层，Escape 关闭并把焦点还给触发元素；点击外部关闭只在不丢失输入时启用。浮层挂到同一 overlay 层，后打开者盖在先打开者上。

## 触屏与窄屏

不要依赖 hover 才能获取关键内容。宽度不足时，菜单和筛选转换为抽屉或全屏面板；表单弹层保持可滚动且不裁切焦点环。

## 避免

- 手写只支持鼠标的定位和焦点。
- 用 tooltip 代替可见的 label 或错误说明。
- 用毛玻璃和大阴影覆盖所有内容（云游戏页除外的明确场景）。
