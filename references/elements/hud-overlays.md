# 测绘叠层

来源：`docs/design/elements/hud-overlays.md`、`Viewfinder`、`TickRing`、`ScrollHint`、`RecIndicator`、`Kbd`。

- 刻度圆环适合仪器、地图半径、角色详情和目标对象；刻度是方向和量值信息，不是背景花纹。
- 刻度尺和坐标读数用于真实的尺寸、距离、时间、版本或进度；不伪造数据。
- 取景角与准星标记图像或对象边界，保持低对比，不裁掉焦点环。
- 滚动提示只提示还有内容，不让页面被滚动动画接管。
- 录制指示使用短词、色点和可读文本；键位提示用真实可操作的键名或 `kbd`。
- 所有测绘叠层都是辅助层，`aria-hidden`、`pointer-events: none` 和局部裁切应默认开启。
