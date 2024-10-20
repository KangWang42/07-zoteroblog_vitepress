# 第28期 插件教程！crush reference：zotero论文参考文献全抓取！

---
类型: 公众号
公众号内容:
  - zotero插件教程
rating:
  - ⭐⭐⭐⭐
简记: 必安插件
---

> 第28期 插件教程！crush reference：zotero论文参考文献全抓取！
> 
> 本期主要介绍zotero插件**crush reference**的使用和配置；实现一键抓取当前论文的参考文献。
> 
> crush可以实现 **论文引文抓取 论文引文预览 论文预览窗口翻译 **

## 目录

[TOC]

## 插件效果

- 当前页面论文抓取**所有参考文献**
- 参考文献的**信息抓取**
- 参考文献的**摘要标题预览及翻译预览**
- **快捷添加参考文献到当前路径或指定路径**
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/GIF%202023-12-10%2012-10-21.gif)

## 插件安装

### 安装网址

MuiseDestiny/zotero-reference (github.com)(https://github.com/MuiseDestiny/zotero-reference/releases)

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231210121641.png)

注意：**github部分区域需要稳定网络访问。公众号回复“插件”可直接获取**

### 安装方式

工具-附加组件-**Install Add-on From Files**-选择下载的xpi文件进行安装

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231210124700.png)

## 插件配置

- 进行设置![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231210122321.png)
- 注意事项
	- 基本设置的点很少，**默认即可**
	- 储存处可打开，下次使用就不用再刷新
	- 来源不要选API，容易抓取不到条目

## 插件使用

### 抓取参考文献

点击阅读器侧栏-点击参考文献-**点击刷新**

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/GIF%202023-12-10%2012-25-08.gif)

### 预览参考文献信息

- 鼠标在参考文献处**悬浮**即可预览
- 参考文献有多个来源，可以调换，建议使用第二个数据源（**一般带有摘要可预览**）
- **crtl点击**参考文献内容即可进行翻译（调用**translate插件**的引擎）
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/GIF%202023-12-10%2012-29-26.gif)

### 抓取参考文献

- 直接点击“＋”号进行抓取（默认抓取到**未分类条目**）
- ctrl + 抓取到选定路径
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/GIF%202023-12-10%2012-33-39.gif)

## 更多快捷键

### 刷新时快捷键与效果

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231210143733.png)

### 参考文献

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231210143753.png)

## 其它

### 插件适用条件

适用于英文文献（**中文论文非常不支持**）

适用于可选中的优质论文

### Bug及其它

参考文献过多（**超过500篇后**）可能会显示不全

论文pdf质量差，或论文引用格式混乱，可能会导致抓取错误（**抓到的论文不是需要的论文**）

### Bug及反馈

参考文献过多一般也能匹配到将近500，之后的篇目只能自己手动去搜索，或参考第23期推文

论文pdf质量差：适用**abbyfinereader**等进行再次OCR，参考第5期推文

如果抓取到毫不相关的论文，可以切换来源查看。如果所有来源都不对，可能插件本身不适配。**前往官网（https://github.com/MuiseDestiny/zotero-reference/issues/6)进行反馈**，或者**放过吧**
