# Catppuccin Native 开发约束

- 将 Obsidian Default 作为唯一的 UI 基线。主题运行时仅使用 CSS。可选配套插件位于 `code-tools/`，只处理围栏代码块的彩虹括号和行号。
- 只调整直接与颜色有关的 CSS 声明和变量。字体、排版、布局、尺寸、圆角、阴影、透明度属性、混合模式、动画和交互均沿用宿主。
- 将正文映射限制在主编辑区的 Markdown 视图。为工作区外框、设置和社区主题浏览器定义局部颜色层级。设置和主题浏览器覆盖内嵌及独立窗口。先检查宿主 DOM 和内置 CSS，优先使用局部 Obsidian 颜色变量。禁止全局覆盖宿主变量或通过 `!important` 强压原生状态。
- 保留两份精确的 Catppuccin 官方色板。浅色使用 Latte，深色使用 Frappé。语义映射共用，任何映射变更都同步更新 `COLOR-SPEC.md`。
- 验收使用隔离的 Obsidian 仓库。分别检查浅色和深色的 Live Preview、Source Mode、Reading View、工作区外框与导航交互状态。以默认主题对照布局和未纳入配色的界面。
- 使用用户确认的许可证状态。原创主题代码采用 MIT。配套插件保留各自的上游许可，公开发布和许可证变更须由用户确认。
- 代码工具沿用 Syntax Palette 的围栏识别、行号规则与基于 TextMate 作用域的括号配对，保留上游许可。色彩仅使用 Catppuccin Native 的 Latte / Frappé，代码高亮、换行、滚动及复制由 Obsidian 原生处理。
