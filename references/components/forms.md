# 表单

来源：`docs/design/components/form.md` 与 `Field`, `Input`, `Select`, `Combobox`, `Checkbox`, `Radio`, `Switch`, `Slider`, `DatePicker`, `FileUpload` 实现。

## 结构

字段至少包含 label、control、help/error 状态和可关联的描述。输入框可用凹陷底或描边；选择、组合框、日期和文件上传分别定义空值、加载、无结果、错误和已选状态。

## 状态

默认、hover、focus-visible、filled、disabled、invalid、loading 和 success 按需实现。错误状态同时给语义色、图标和文字；成功状态不只闪一次颜色。复选、单选、开关和分段选择保留形状或位置差异，避免仅用红绿或亮暗区分。

## 行为

键盘必须支持 Tab、方向键、Enter/Space、Escape 和必要的类型检索。组合框和浮层需要焦点管理、当前项语义、远程加载与无结果提示。日期范围要明确起止端点和中间区间。文件上传提供选择、进度、失败和删除，不伪造上传成功。

## 避免

- 用 placeholder 代替 label。
- 让错误只显示成红色边框。
- 只为鼠标实现下拉和日期选择。
- 用固定颜色值破坏暗色、反转块或主题色接管。
