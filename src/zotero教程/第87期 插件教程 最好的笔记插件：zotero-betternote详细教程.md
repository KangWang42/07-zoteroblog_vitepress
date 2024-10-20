# 第87期 插件教程 最好的笔记插件：zotero-betternote详细教程

---
公众号内容:
  - zotero插件教程
rating:
  - ⭐⭐⭐⭐
简记: 好用看看，笔记崛起
类型: 公众号
---

> 第87期 插件教程 最好的笔记插件：zotero-better-notes更新及详细教程
> 
> better-notes插件在zotero更新到beta72版本的时候终于迎来了大更新（zotero目前（2024.4.11）还不稳定，可以先不更新）；**去掉了工作区笔记，新增了笔记窗口，双联效果大加强**。
> 
> 本期从：**基础功能，笔记链接，新笔记窗口，笔记模板，笔记同步**五大模块进行介绍
> 
> 本期介绍基于**beta72版本，better-notes插件（1.1.4-beta.62）之前的版本查看往期教程**
> 
> 码文不易，求个点赞

# 本期大纲

[TOC]

# 插件介绍

主页：[windingwind/zotero-better-notes](https://github.com/windingwind/zotero-better-notes)

中文文档：[Zotero Better Notes：基于知识的笔记插件 (yuque.com)](https://zotero.yuque.com/staff-gkhviy/better-notes)（这个写的真好，非常有需要的朋友阅读一下）

下载界面：[Releases · windingwind/zotero-better-notes (github.com)](https://github.com/windingwind/zotero-better-notes/releases)

# 插件安装

进入下载界面[Releases · windingwind/zotero-better-notes (github.com)](https://github.com/windingwind/zotero-better-notes/releases)

![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111619654.png)

注意：**github部分区域需要稳定网络访问**；可公众号后台回复 **插件** 获取最新插件

进入zotero-工具-附加组件-**Install Add-on From Files**-选择下载的xpi文件进行安装

# 功能展示

## 基础功能

### 工具栏

添加**笔记工具栏**，文档编辑word化；包括常用功能：文本格式（设置为标题列表等），设置加粗，添加其它条目到该笔记中作为引注

![文档编辑word化](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111641209.png)

### 笔记导出

- 支持md，word，pdf，FreeMind格式
- bn的导出格式极为丰富
- 推荐使用**md格式导出及docx格式导出**
- md格式可以进行双向同步，**导出的文件可以使用其它typra或ob进行编辑并到obsidian查看**
- docx格式，可实现兼容性（zotero7）导出**图片，公式，及链接**
![笔记导出](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111643372.png)

## 笔记链接

### 笔记与笔记之间建立双联

在笔记编辑器中，直接点击左侧的花图表图标。依据提示，**将在主笔记当前光标处添加一条正链（主笔记=>子笔记），当前笔记成为子笔记。同时，在当前子笔记末尾添加一条反链（子笔记=>主笔记）；**

![建议笔记和笔记双链](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111711860.png)

### 建立注释和笔记的双链

如果想把**注释文本链接到另一个笔记**建立双链也可以使用zotero betternote实现

![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111720964.png)

## 新笔记窗口

betternote设计了打开笔记的新面板。可**以查看笔记的双链情况，同时可以看到大纲，设计的非常不错**（之前工作区笔记的升级版,UI很好）

打开方式：**在文库中直接打开笔记或在笔记右上角点击在窗口中显示**

新笔记面板**可以用来快速预览双链；查看关联视图，查看笔记大纲，进行笔记编辑等**

![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111728500.png)

## 笔记模板

betternote可以使用固定的模板来快速新建笔记，不过自定义模板难度较高，**推荐到作者的模板讨论区使用现成的模板**。流程见下图

网址：[zotero-better-notes Note Templates](https://github.com/windingwind/zotero-better-notes/discussions/categories/note-templates)

![如何查找模板](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231223201546.png)

注意，复制到的模板用**剪贴板导入**，不要在模板编辑区自己导入

## 笔记同步

在zotero中导出时可设置笔记同步，**同步为双向同步，在第三方md编辑软件中修改zotero中也可以看到**

![笔记同步](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404111848863.png)

# 其它

从pdf复制粘贴到笔记中的文本自带引注

可以使用**CSS修改来隐藏引注，见往期推文**
