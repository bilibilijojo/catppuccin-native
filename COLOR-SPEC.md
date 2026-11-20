# 颜色规范

颜色跟随宿主的 `.theme-light` 和 `.theme-dark`。下表记录 26 组原始 HEX。主题用带 `--cpd-` 前缀的变量向工作区组件提供色板，各组件在自己的作用域映射宿主颜色。 [Catppuccin 官方色板](https://catppuccin.com/palette/)

| 色名 | CSS 色板变量 | Latte | Frappé |
| --- | --- | --- | --- |
| Rosewater | `--cpd-rosewater` | `#dc8a78` | `#f2d5cf` |
| Flamingo | `--cpd-flamingo` | `#dd7878` | `#eebebe` |
| Pink | `--cpd-pink` | `#ea76cb` | `#f4b8e4` |
| Mauve | `--cpd-mauve` | `#8839ef` | `#ca9ee6` |
| Red | `--cpd-red` | `#d20f39` | `#e78284` |
| Maroon | `--cpd-maroon` | `#e64553` | `#ea999c` |
| Peach | `--cpd-peach` | `#fe640b` | `#ef9f76` |
| Yellow | `--cpd-yellow` | `#df8e1d` | `#e5c890` |
| Green | `--cpd-green` | `#40a02b` | `#a6d189` |
| Teal | `--cpd-teal` | `#179299` | `#81c8be` |
| Sky | `--cpd-sky` | `#04a5e5` | `#99d1db` |
| Sapphire | `--cpd-sapphire` | `#209fb5` | `#85c1dc` |
| Blue | `--cpd-blue` | `#1e66f5` | `#8caaee` |
| Lavender | `--cpd-lavender` | `#7287fd` | `#babbf1` |
| Text | `--cpd-text` | `#4c4f69` | `#c6d0f5` |
| Subtext 1 | `--cpd-subtext-1` | `#5c5f77` | `#b5bfe2` |
| Subtext 0 | `--cpd-subtext-0` | `#6c6f85` | `#a5adce` |
| Overlay 2 | `--cpd-overlay-2` | `#7c7f93` | `#949cbb` |
| Overlay 1 | `--cpd-overlay-1` | `#8c8fa1` | `#838ba7` |
| Overlay 0 | `--cpd-overlay-0` | `#9ca0b0` | `#737994` |
| Surface 2 | `--cpd-surface-2` | `#acb0be` | `#626880` |
| Surface 1 | `--cpd-surface-1` | `#bcc0cc` | `#51576d` |
| Surface 0 | `--cpd-surface-0` | `#ccd0da` | `#414559` |
| Base | `--cpd-base` | `#eff1f5` | `#303446` |
| Mantle | `--cpd-mantle` | `#e6e9ef` | `#292c3c` |
| Crust | `--cpd-crust` | `#dce0e8` | `#232634` |

## 工作区颜色映射

沿用 Catppuccin 的表面层级。正文用 Base，次级区域用 Mantle 和 Crust，分隔线与悬停状态用 Surface 0。两侧边栏共用 Mantle，让文件树和大纲在视觉上属于同一层。 [Catppuccin 设计指南](https://github.com/catppuccin/catppuccin/blob/main/docs/style-guide.md#background-colors)

| 区域 | 角色 | Latte | Frappé | Obsidian 变量 |
| --- | --- | --- | --- | --- |
| Markdown 正文 | Base | `#eff1f5` | `#303446` | 正文容器的 `background-color` |
| 两侧边栏、笔记顶部工具栏、当前主标签 | Mantle | `#e6e9ef` | `#292c3c` | `--background-secondary`、`--mobile-sidebar-background`、`--file-header-background*`、`--tab-background-active` |
| 标签栏底面、左侧功能区、状态栏和侧栏搜索输入框 | Crust | `#dce0e8` | `#232634` | `--tab-container-background`、`--sidebar-tab-container-background`、`--ribbon-background*`、`--status-bar-background`、`--background-modifier-form-field*` |
| 分隔线、导航缩进线 | Surface 0 | `#ccd0da` | `#414559` | `--divider-color`、`--tab-divider-color`、`--tab-outline-color`、`--nav-indentation-guide-color` |
| 常规导航文字和图标、状态栏文字 | Subtext 1 | `#5c5f77` | `#b5bfe2` | `--nav-item-color`、`--icon-color`、`--tab-text-color*`、`--status-bar-text-color` |

文件树悬停使用 Surface 0 55% + Mantle，当前文件与选中项的底色使用 Mauve 15% + Mantle。当前文件前景使用 Mauve 可读色，也就是 Latte 的 Mauve 45% + Text 和 Frappé 的 Mauve 原色。自定义文件夹图标沿用图标提供者定义的颜色。

左侧功能区按钮的常态底色随功能区使用 Crust。悬停时用完整的 Surface 0（Latte `#ccd0da`，Frappé `#414559`）填充按钮，并用 Mauve 可读色绘制图标。该覆盖限定在左侧功能区动作按钮。

## 设置颜色映射

内嵌设置和独立设置窗口共用 `.modal.mod-settings` 下的颜色变量。

| 区域 | 角色 | Obsidian 变量 |
| --- | --- | --- |
| 设置主面板 | Base | `--settings-background`、`--modal-background`、`--background-primary` |
| 左侧分类导航 | Mantle | `--modal-sidebar-background` |
| 设置项卡片 | Surface 0 32% + Base | `--setting-items-background` |
| 搜索框和输入框 | Crust 底色、Subtext 1 占位文字 | `--background-modifier-form-field*`、`--input-placeholder-color` |
| 边框、分隔线、普通按钮 | Surface 0 | `--setting-items-border-color`、`--setting-items-divider-color`、`--interactive-normal` |
| 按钮悬停 | Surface 1 45% + Surface 0 | `--interactive-hover` |
| 当前分类 | Mauve 15% + Mantle 底色、Mauve 可读色前景 | 当前 `.vertical-tab-nav-item` 的局部状态颜色 |

社区主题浏览器在 `.modal.mod-community-theme` 上复用设置的面板、输入框和文字颜色。浏览器底面用 Base，筛选区用 Mantle，列表卡片用 Surface 0 32% + Base。卡片的预览图片沿用各主题提供的资源。

## 笔记颜色映射

纯色取上表同名 HEX。`A 45% + B` 表示以 sRGB 将 A 的 45% 和 B 的 55% 混合。正文用色中的 **可读色** 在 Latte 使用原色 45% + Text，在 Frappé 使用原色。可读色适用于下表明确标出的强调和代码 token。透明百分比只用于颜色值。

| 元素 | 两种模式的角色 | Obsidian 变量或局部选择器 |
| --- | --- | --- |
| 正文、底色 | Text ／ Base | `--text-normal`，滚动区和阅读容器的 `background-color` |
| H1、H2、笔记内标题 | Mauve 可读色 | `--h1-color`、`--h2-color`、`--inline-title-color` |
| H3、H4 | Blue 可读色 | `--h3-color`、`--h4-color` |
| H5、H6 | Teal 可读色 | `--h5-color`、`--h6-color` |
| 加粗、斜体 | Mauve、Teal 可读色 | `--bold-color`、`--italic-color` |
| 删除线 | Maroon 可读色 | 渲染的 `del`、`s` 和编辑器的 `.cm-strikethrough` |
| 高亮 | Yellow 30% 透明色，Text 前景。带类型的彩色高亮使用 Red、Peach、Yellow、Green、Blue、Mauve | `--text-highlight-bg`、`--highlight-background`、`--highlight-background-*` |
| 外部链接 | Blue，悬停使用 Blue 可读色 | `--link-external-color`、`--link-external-color-hover` |
| 内部链接 | Mauve 可读色，悬停使用 Blue 可读色。未解析链接用 Mauve 可读色及 Lavender 65% 透明下划线 | `--link-color`、`--link-color-hover`、`--link-unresolved-color`、`--link-unresolved-decoration-color` |
| 标签 | Blue 可读色，蓝色半透明背景和边框 | `--tag-color`、`--tag-color-hover`、`--tag-background*`、`--tag-border-color*` |
| 引用 | Rosewater 边线、Rosewater 6% 透明底色、Rosewater 25% + Text 正文 | `--blockquote-*`，编辑器的 `.cm-formatting-quote`。嵌套的加粗和斜体 token 沿用各自的强调色。 |
| 段落分隔、列表标记 | Surface 2 分隔线、Overlay 2 可读色标记，悬停 Subtext 1，折叠 Mauve 可读色 | `--hr-color`、`--list-marker-color*` |
| 任务清单 | 未勾选使用 Overlay 2 边框，悬停使用 Overlay 1 55% + Text。已勾选使用 Green 可读色并以 Base 画勾，已完成文字使用 Subtext 0 可读色。源码用 Green 可读色标记非空状态，空状态沿用列表标记色。 | `--checkbox-*`、`--checklist-done-color`、源码 `.cm-formatting-task` |
| 表格 | Surface 0 表头，Base 正文，交替行使用 Surface 0 25% + Base，Surface 2 网格，Surface 1 表头边框 | `--table-background`、`--table-header-*`、`--table-border-color`、`--table-row-*`。源码只给表头和行分隔语法着色。 |
| 行内代码 | Mauve 可读色、Mantle 底色、Surface 1 边线 | `--code-background`、`--code-border-color`。在行内代码局部重绑定 `--code-normal`。 |
| 围栏代码 | Text、Mantle 底色、Surface 1 边线 | `--code-normal`、`--code-background`、`--code-border-color`，下表给出 token 颜色 |
| 数学公式 | Teal 可读色 | 渲染容器 `.math`，编辑器 `.cm-math`，沿用原生数学 SVG 的继承色 |
| Mermaid | Base 背景、Surface 0 和 Crust 表面、Overlay 0 边线、Text 文字、Subtext 0 次要文字、Subtext 1 连线、Mauve 强调、Red 错误。系列依次为 Blue、Peach、Green、Red、Sapphire、Yellow、Mauve、Pink。 | `--mermaid-*`，由 1.15.1 的原生渲染器传给 SVG |
| 选区、光标 | Mauve 24% 透明色选区、Rosewater 可读色光标 | `--text-selection`、`--caret-color`。阅读模式没有编辑光标。 |
| 次要文本、语法标记 | Subtext 1、Overlay 2 可读色 | `--text-muted`、`--text-faint` |

Obsidian 的 Markdown 高亮、Callout 和 Mermaid 各自处理渲染时的颜色与混合。原生的混合模式、组件透明度和未解析链接透明度继续生效。

在各自的 Base 底色上，正文对比度分别为 Latte 7.06:1、Frappé 8.06:1。外部链接按规范使用官方 Blue，Latte 在 Base 上为 4.34:1，Frappé 为 5.34:1。链接沿用原生下划线样式。

### Callout

下表中的别名由宿主解析。标题以对应色和 Text 混合，Latte 使用对应色 35%，Frappé 使用 75%。图标和背景继承所属类型的主题色。源码视图可识别 `.cm-hmd-callout`，使用 Rosewater 25% + Text 表示原始标记，具体类型要到 Live Preview 或 Reading View 中才能呈现。

| 类型及别名 | 颜色 | 变量 |
| --- | --- | --- |
| Note、未指定的类型 | Blue | `--callout-default` |
| Abstract / Summary / TLDR | Sapphire | `--callout-summary` |
| Info | Sky | `--callout-info` |
| Todo | Lavender | `--callout-todo` |
| Important | Mauve | `--callout-important` |
| Tip / Hint | Teal | `--callout-tip` |
| Success / Check / Done | Green | `--callout-success` |
| Question / Help / FAQ | Yellow | `--callout-question` |
| Warning / Caution / Attention | Peach | `--callout-warning` |
| Failure / Fail / Missing | Maroon | `--callout-fail` |
| Danger / Error | Red | `--callout-error` |
| Bug | Flamingo | `--callout-bug` |
| Example | Pink | `--callout-example` |
| Quote / Cite | Rosewater | `--callout-quote` |

### 围栏语法

| 语义 | 颜色 | 变量 |
| --- | --- | --- |
| 普通代码 | Text | `--code-normal` |
| 注释、元信息 | Subtext 0 可读色 | `--code-comment` |
| 函数、属性、变量 | Blue 可读色 | `--code-function`、`--code-property` |
| 关键字 | Mauve 可读色 | `--code-keyword` |
| 字符串、字符 | Green 可读色 | `--code-string` |
| 数值和布尔 | Peach 可读色 | `--code-value`，用于源码布尔 token `.cm-hmd-codeblock.cm-atom` |
| 运算符 | Teal 可读色 | `--code-operator` |
| 标点 | Subtext 1 | `--code-punctuation` |
| 标签、常量 | Maroon 可读色 | `--code-tag` |
| 正则、重要标记 | Red 可读色 | `--code-important` |

编辑器和阅读视图共享颜色变量。CodeMirror 与 Prism 对某些语言的标点、定义和普通标识符有不同的分类。同一语义按同一规则配色，实际可着色的字符范围由宿主的 tokenizer 决定。
