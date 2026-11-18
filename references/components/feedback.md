# 反馈、加载与状态

来源：`docs/design/components/feedback.md` 与 `Alert`, `Toast`, `Progress`, `ProgressRing`, `Spinner`, `Skeleton`, `EmptyState`, `Loader`, `CompletionBanner` 实现。

## 语义

- Alert：页面内持续说明，适合错误、警告、信息和成功。
- Toast：短暂、非阻塞反馈；提供可撤销或下一步行动时保持可达。
- Progress：确定性进度用黄色填充灰色轨道；量值图表使用 `data` 蓝。
- Skeleton：占位结构，不做扫光；EmptyState：说明为什么为空和下一步行动。
- Loader / SplashScreen：盖住页面的加载层，使用一次性入场和可读进度。
- CompletionBanner：完成态可使用暗底、黄色区和清晰的完成文字，但不遮挡后续操作。

## 状态与可访问性

状态同时由色、图标、文字和结构表达。Toast、Dialog 和 Loader 使用正确的 live-region、焦点和关闭行为。减少动态效果时停在最终状态。加载、空、错误和成功不能造成布局跳动。

## 避免

- 只闪一下颜色却没有文字反馈。
- 用无限旋转替代真实进度或无障碍说明。
- 把成功、危险、信息全部做成同一黄色。
