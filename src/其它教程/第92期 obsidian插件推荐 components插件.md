# 第92期 obsidian插件推荐 components插件

---
公众号内容:
  - obsidain插件教程
rating:
  - ⭐⭐⭐⭐
简记: 非常好的插件
类型: 公众号
---

> 第92期 obsidian插件推荐 components插件应用实例
> 
> components插件是由vran大佬开发的**obsidian插件**
> 
> 可以替代自己手打dataview的困难，和过于平铺的展示效果，实**现美化美观的数据库文件索引和多效果展示**
> 
> 我用components创建了一个个人主页，**整合了我的日常（公众号），学习（课程笔记），阅读（微信读书），科研（文献阅读）等所有笔记，真正实现了all in one**

## 插件介绍

components插件目前分为公测版和正式版。**公测版是全免费的，满足中度使用人群的需求。**正式版在公测版的基础上进行了细完善

公测版组件功能列表

- **数据视图**组间：轻松掌握时间进度
- **计数**组件：统计文档并显示数字
- 正计时：距离某个时间开始多久
- 倒计时：截止时间
- 日期进度：轻松掌握日期进度
- 时钟：显示一个时钟
- **摘录**：随机获取内容
- 按钮：创建按钮来执行命令
- 打卡：打卡日常任务或习惯
- 图表：根据笔记绘制可视化图
- **dataview**：将dataview作为组件显示
- markdown：嵌入markdown内容
- 自定义卡片
- **组合**：进行组件分栏

## 我的主页-公测版构建-效果展示

### 主页长图效果

![我的主页](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405211003358.png)

### 我的摘录组件

使用 **weread** 插件 和 **component-摘录组件** 构建；

随机展示读书摘录

![微信读书摘录](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405211006390.gif)

### 公众号和文献看版组件

使用templater插件 zotlit创建来创建**带有元信息的条目** 使用**数据视图组件**展示

数据视图的列表视图可以**自定义设置多重筛选条件;同时设置展示的属性项,图中展示了文献的中文标题影响因子等信息**

画廊视图一般展示默认有内容图片的笔记,添加分组后效果美观

![数据视图](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405211009832.png)

### 计数组件统计进度

使用计数组件 **以修改时间为条件 构建月内新文献数统计**

并且点击图标即可查看具体修改了哪些条目

![计数组件](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405211011142.png)

### 热力图日历

参考教程：[热力图](https://github.com/RavenHogWarts/Snippets/blob/master/Obsidian/Components%26Contribution-Garph.md)

![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405211019759.png)

### 文献检索器

参考教程：[文献检索器](https://github.com/RavenHogWarts/Snippets/blob/master/Obsidian/Components%26Contribution-Garph.md)

![GIF 2024-5-21 10-06-18.gif](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405211020700.gif)

## 插件安装

### 插件安装网址

[obsidian-components-release (github.com)](https://github.com/obsidian-components/obsidian-components-release/releases)

[Obsidian | Components (notion.site)-这个里边有一些很好的案例](https://vran.notion.site/Obsidian-Components-88619bf4b6d04575bfd41e850ca2b74a)

一些components插件教程和案例：[RavenHogWarts/Snippets (github.com)](https://github.com/RavenHogWarts/Snippets/blob/master/Obsidian/Components&Contribution-Garph.md)

设置主页全宽CSS：[RavenHogWarts/Snippets (github.com)](https://github.com/RavenHogWarts/Snippets/blob/master/Obsidian/Style-Setting.md)

正式版说明：[Obsidian | Components - 飞书云文档 (feishu.cn)](https://wxycbt0cjk.feishu.cn/docx/QigvddUTloAUf9xTRX5capy3nwG)

### 关于正式版-来自作者文档

组件层面

- 数据视图
- 表格增加了统计行，可以对每一列进行求和、平均值、最大值等
- 表格列头会根据属性类型自动添加 ICON，视觉上更加高级: - 优化了进度条属性的样式，使其高度更加合理
- 解决了公测版中行内容不对齐的问题
- 增加了一个 Markdown 属性内容，你可以在属性中直接写 Markdown 文本，可以直接被渲染成富文本的样式
- 重新设计了画廊视图的封面界面
- 画廊视图的封面现在支持横版和竖版两种封面类型，竖版非常适合人物、书籍封面，横版适合影视、风景等封面
- 画廊的封面类型增加了文本内容选项，可以直接展示笔记中的文本，插件会自动忽略掉属性区的文本
- 去除掉了属性设置中的默认值设置，这个可以通过模板功能来替代
- 数据视图现在支持分页加载了
- 数据视图的设置页面进行了重新分类，设置项更加清晰直观
- 数据视图中的每个条目（笔记）添加了上下文菜单，点击可以修改名称、移动文件、复制文件等，未来还会增加更多功能
- 数据视图的图片属性设计了一个全新的编辑组件，使得图片的添加和删除更加友好
- 筛选添加了有值和无值两种条件
- 计数组件现在改名叫**统计数字组件**，名字更加容易理解
- 组件采用分栏布局时，设置菜单不会再和组件区域重叠了
- 组件采用标签页布局时，可以点击标签页重命名，也可以直接拖拽标签页进行重新排序，不再需要点进设置页面中去操作了
- 标签页布局时，每个标签项也会根据组件类型自动添加 ICON
- Markdown 组件：文本内容现在支持直接在笔记中实时修改
- Dataview 组件：设计了一套全新的动态参数交互界面
- 打卡组件：完全重新设计了打卡组件，现在打卡组件不再支持基于任务项的打卡模式
- 移除了自定义卡片组件
- 现在组件的样式设置中支持设置是否显示边框，什么都不做，只显示边框也可以设计出一套设计统一、高级的组件集合

还有一些看不见的工作，但是它们直接决定了用户体验的上限

- 首先是作者重新设计了文档的筛选逻辑，使得性能大幅提升
- 然后作者重写了几乎所有组件的 CSS，确保组件的设计风格能保持一致
- 作者为小屏也做了大量优化，确保了组件在移动端的使用体验

