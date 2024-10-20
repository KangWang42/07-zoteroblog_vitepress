# 第88期 zotlit详细教程：最优zotero-obsidian同步方案（文中附模板代码)

---
公众号内容:
  - obsidain插件教程
  - zotero插件教程
rating:
  - ⭐⭐⭐⭐
简记: 还可以的
类型: 公众号
---

> 第88期 免费最优zotero-obsidian同步方案 zotlit详细教程（文中附模板代码）（本期建议一看！）
> 
> **之前介绍给如何使用MarkDB-Connect来联动zotero和obsidian。但效果并不好，复杂的设置和插件版本等问题导致问题很多**
> 
> 本期介绍一下zotero ob本人实测**最优同步方案**的详细教程；特点：**同步方便，自定义模板，可在ob进行PDF摘录和论文引用**；缺点，只能**手动导出，单篇导出**
> 
> 使用zotlit进行导出的文献。由于自带yaml区（就是作者，标题，出版日期等元数据），**可以使用ob超强语法dataview进行索引和检索（无比好）**
> 
> 本期使用自己做的导出模板（公众号回复 ：**240420**获取）

## 本期大纲

[TOC]

## 插件介绍

ZotLit 是一套整合 [Obsidian.md(opens in a new tab)](https://obsidian.md/) 和 [Zotero(opens in a new tab)](https://www.zotero.org/) 的社区插件，进而优化 Obsidian 内的学术工作流体验

### 相关链接

[ZotLit中文文档教程 (aidenlx.top)](https://zotlit.aidenlx.top/zh-CN)

### 优点（内容来自zotlit中文文档）

- ⚡️ 高性能
    - 直接从Zotero数据库读取数据，无需以文本格式导出数据
    - 在Obsidian中进行快速模糊搜索文献
- 🔓 全面访问Zotero数据
    - 所有数据都可以在Obsidian中获取，包括摘录、笔记、标签和附件。
    - **不受Zotero API或Better BibTeX的限制。**
- 🔨 高度可定制的模板
    - 编写自己的模板以生成文献摘录和以任何格式导入摘录。
    - 使用 [Eta(opens in a new tab)](https://eta.js.org/) 提供支持，可以在模板中编写JavaScript代码来处理复杂的转换。
    - 以结构化的方式查看 Zotero 存储的所有文献中的数据。
- 🔍 摘录视图
    - 在Obsidian中查看摘录，与文献笔记并排显示。
    - 将摘录拖动到文献笔记中进行导入。
    - 始终保持最新，每当您在Zotero中更改摘录时自动同步。
- 📝 导入摘录
    - 从Zotero导入图像和文本摘录到Obsidian。
    - 保持摘录与Zotero同步更新。
- ✍️ 轻松创建文献笔记
    - 快速切换器可创建文献笔记，并从Zotero库中的任何文献插入引文标识符。
    - 从Zotero项目页面打开Obsidian中的文献笔记。

## 功能展示

### 笔记的导出及打开

在zotero端右键导出即可导出条目笔记到ob

![笔记导入-min.gif](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201112993.gif)

### 笔记PDF摘录

![快速引用.gif](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201013753.gif)

### 使用dataview或dataviewjs进行索引（放到下一期介绍）

![DATAVIEW索引.gif](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201033912.gif)

## 插件安装

参考教程：[安装 – ZotLit (aidenlx.top)：介绍的很详细](https://zotlit.aidenlx.top/zh-CN/getting-started/install)

由于**官方教程非常的好，就不详细说明了。**

安装好插件后进入**插件配置**

## 插件配置

建议直接参考以下配置

### Zotero插件配置

![zotero插件配置](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201037100.png)

### Obsidian插件配置

![obsidian插件配置](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201046153.png)

### 设置模板

公众号回复“**240420**”获**取模板文件**

在文件夹里直接替**换掉自己的默认模板**即可使用

![设置模板](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201049114.png)

## 插件使用

### 笔记导出

在zotero软件选中条目右键菜单**Obsidain actions：creat note**即可导出笔记

### 笔记注释引用

在obsidian中使用命令菜单（crtl+p）选择ZotLit: **Open Zotero annotation view in side panel**

点击链接图标,**Link with selected literature**，选择需要的文献即可查看预览视图

拖着预览视图注释可快捷引用

![注释快捷引用](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404201056397.png)

### 笔记索引

使用插件：[vran-dev/obsidian-contribution-grap](https://github.com/vran-dev/obsidian-contribution-graph)

如何索引并创建dataview组件下期会介绍