# 数据展示

来源：`docs/design/components/data-display.md` 与 `Table`, `DataRow`, `Stat`, `Sparkline`, `Timeline`, `Schedule`, `Tag`, `Avatar` 实现。

## 选择结构

- `Table`：可比较的列数据，支持排序、选择、行展开、表头吸顶和窄屏横向滚动。
- `DataRow`：一行内的标签、读数和小型面积图；用 `data` 蓝表达量值。
- `Stat` / `RollingNumber`：强调一个真实读数，使用 tabular figures，避免伪造变化。
- `Timeline` / `Schedule`：时间顺序、今天、完成与未到节点；真实状态线不能被装饰网格隐藏。
- `Tag` / `Badge` / `ResourceChip` / `Countdown`：短状态和资源，不把所有内容胶囊化。

## 状态与行为

选中、排序、展开、分页和筛选必须提供文字或形状冗余。高密度表格的首列、表头和关键操作在窄屏保持可见；行展开内容采用凹陷底或分层，而不是再套完整卡片。

## 避免

- 用彩虹图表替代语义色。
- 用装饰网格模拟真实坐标和数据。
- 把所有统计块做成相同权重，失去主次。
