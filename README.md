> [!note]
> A css snippet used to bring useful features in the BT theme to Obsidian non-Blue Topaz theme users.
>
> **原作者主题见**：https://github.com/PKM-er/Blue-Topaz_Obsidian-css

# Blue Topaz Legacy
## 制作初衷

*Blue Topaz* 主题是一个非常优秀的主题，由多位大佬一起开发而来，内含许多种自定义方案以及强大的扩展功能。但是除去这些最为明显的优势之外，该主题在==「**基础优化**」==方面的优秀也是不可忽视的。例如在许多人看来理所当然的「首行缩进」、「两端对齐」，图片自适应显示强调字体的颜色、挖空涂黑等等新的字体强调方式，以及一些 admonition 小组件的 css 处理。这些功能不仅默认主题中没有，大部分主题（如 *AnuPpuccin*等）都没有这些功能, 或者功能不如 bt 完善。为了在其他主题中也可以使用这些基础优化，达到舒适的编辑体验，我将 *Blue Topaz*主题中包含重要基础优化的片段摘录出来，重新整合成了「**Blue Topaz Legacy**」css 片段，供大家使用。

下面简要介绍一下 Blue Topaz Legacy 包含的功能。

## Typography：字体与排版

### 字体设置

具体包括：

- 强调字体和库名字体自定义
- 强调字体颜色自定义，同时加粗斜体的字体颜色是线性渐变色
- 强调字体优先级为：粗体>斜体>内链
- 增加高亮背景颜色、高亮文字颜色的简单设置
- 增加行内代码样式设置
- 增加挖空涂黑样式设置

![](assets/README.assets/image-20230711230856232.png)

### 段落排版优化

具体包括：

- 标题的级别段前距与段后距设置
- 标题的级别缩进设置
- 段落首行缩进
- 段落两端对齐

> [!attention]+ 注意
> 若要在阅读模式使用段落首行缩进与两端对齐样式，需要下载安装 *Contextual Typography* 插件。

## Markdown 元素
### 链接美化

具体包括：

- 内链：
    - 可以设置是否开启下划线
    - 可以设置内链下划线是否为波浪线，且可以在 style settings 中全局开启或使用 `hide-wavy` cssclass 制作白名单，在单一笔记中不开启
    - 可以设置内链文字颜色
- 外链：
    - 可以设置是否开启下划线
- 可以设置未创建链接的颜色
- 可以设置悬浮鼠标时链接背景为彩虹色
- 取消编辑模式下点击链接自动跳转，按住 `command` 按钮跳转

### 嵌入美化

具体包括：

- 可以调整嵌入页面的高度
- 可以设置嵌入背景透明
- 可以隐藏嵌入文档的笔记名称、H1H2H3 标题
- 可以隐藏嵌入文档的 banner
- 嵌入文档支持浮动效果

### 表格美化

具体包括：

- 表格悬浮放大效果
- 当文字过多，一行放不下的时候有四种显示格式
- 可以选择是否显示表格框线
- 可以设置表格是否全宽
- 有四种显示样式可供选择

### 列表

具体包括：

- 设置列表间距
- 设置无序列表的样式
- 设置有序列表的样式
- 彩虹大纲线

### 分割线

可以选择分割线的样式，具体包括：

- Default
- with icons
- without icons
- with Numbers

### Admonition 特别样式支持

完全适配了 Blue Topaz 内置的所有 ad 类型，包括：

目前支持 ad 类型：

- blank 全透明框
- def definition
- thm theorem
- lem lemma
- cor corollary
- pro proposition
- hibox 自动隐藏框
- col2 col3 col4 内容分多栏
- kanban 伪看板
- table 表格单行全部显示

关于 Callout 的部分可以见 [[README#Callout 增强]]

## 类笔记样式背景设置

具体包括：

- 可以开启网格背景
- 可以设置边栏的笔记不应用网格背景
- 可以设置几种不同的网格
- 可以设置网线、背景板的颜色

## 加载页面

施工中……

## 未出现在 Style Settings 中的效果

### 图片自适应显示

在 Obsidian 笔记中的图片可以自适应页面宽度，以最合适的大小显示。

### 图片排版优化

具体包括：

- 图片自适应显示：`--image-max-width: 100%`
- 图片自适应横排：`img-grid`
- 图例说明：`img-captions`*（只适用于 Wiki 链接格式）*
- 图片向左、右对齐与居中
- 图片与文字在行中混排（向左、右对齐与居中）
- 图片大小设置

#### 图片自适应横排
- 方法一：图片加 `|inline`，放在同一行。可以单独调整大小
- 方法二：图片加 `|+grid`，放在同一行，会自动调整大小，也可以独单调整
  `![[xxx.png|+grid]]`
- 方法三：在笔记 YAML 处输入 `cssclass: img-grid`

![[image-20230524125630410.png]]

#### 图片大小与位置
- 插入的图片默认是居中显示，点击图片可以放大
- 在图片后加上 `|数字` 可以控制图片大小
- 在图片后加上 `|R` 或 `|L`，可以控制图片居右还是居左，也可以跟上面的控制大小同时使用。
- 另外，以下形式也可以使用。同一行的四种输入方式，效果都是一样的

`left` / `Left` / `LEFT` / `L`

`right` / `Right` / `RIGHT` / `R`

- 在图片后加上 `|inlR`、`|inlL` 或 `|inl`，可以使图片变为行内显示，也可以跟控制大小同时使用。`![[image-20230204021300718.png|inl|100]]` 可用变体有：

`inlineL` / `InlineL` / `INLINEL` / `inlL`

`inlineR` / `InlineR` / `INLINER` / `inlR`

`inline`/`Inline`/`INLINE`/`inl`

> [!tip]+ Tips
> 注意使用 inlR/inlL 和 inl 的位置，对于 inlR 和 inlL，它们所在行的文字，处在图片的上边界处。而对于 inl，所在行的文字在图片的下边界处。

使用效果：

![](assets/README.assets/image-20230711230310740.png)

#### 图例效果
- 在图片后加 `#centre` / `center`、`#right` 或 `#left`

形如：`![[xxx.png#position|captions|size]]`

- 行内或连续的图例，使用 `#inl`

![](assets/README.assets/image-20230711230421971.png)

### Callout 增强

个人主要在 *Anuppuccin* 主题中增强适配了三个 callout 类型：

- callout *icon*：实现首页日历图标
- callout metadata *no-border*：实现首页隐藏边框，天气问候
- callout metadata *banner*：实现首页隐藏边框，天气问候

## 目前已知问题⚠️

- 尽量不要使用带有==「**全宽显示**」==的 style settings，因为开启会导致 Obsidian「外观」设置中的「**缩减栏宽**」设置失效。
