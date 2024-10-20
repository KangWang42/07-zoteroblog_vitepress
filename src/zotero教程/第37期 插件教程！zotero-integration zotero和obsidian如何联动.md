# 第37期 插件教程！zotero-integration zotero和obsidian如何联动

---
类型: 公众号
公众号内容:
  - zotero教程
  - obsidian教程
rating:
  - ⭐⭐
简记: 不建议看，bug是真的多
---

>第37期 第37期 插件教程！zotero-integration: zotero和obsidian如何联动
>
>我个人的学习模式主要是使用zotero来进行文献阅读，使用obsidian来进行笔记写作。同时obsidian可以使用dataview来管理和可视化zotero的文献库
>
>这个过程比较重要的便是如何将zotero的条目信息导出到ob库中，作为中介来实现两个软件的协同；本期介绍zotero-integration方式，后续会更新zotlit的相关教程

## 目录

[TOC]

## 联动效果

### 功能介绍

- 将zotero条目**注释导入obsidian笔记**，带注释链接及跳转
- 在zotero里将有笔**记链接的条目添加彩色标签**
- **从zotero直接跳转到obsidian对应链接**
- Zotero7兼容

### 功能展示

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/GIF%202023-12-14%2018-35-39.gif)

## 插件准备

### Zotero准备

- 安装**zotero-markdb-connect**插件：(https://github.com/daeh/zotero-markdb-connect)
- 安装**Better BibTex for Zotero**插件：(https://github.com/retorquere/zotero-better-bibtex)

### Obsidian准备

- 安装**Zotero Integration**插件
	- 可直接在官方商店安装
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214191740.png)

### 简单获取

公众号回复**同步**，直接获取最新（适配zotero7）的zotero插件

## 插件配置

### Obsidian配置

#### 配置项

- Note Import Location
	- 设置笔记路径，最好新建一个文件夹专门放zotero同步的注释文件
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214184818.png)

- Import Formats
	- 设置**导入笔记的笔记名**
	- 导入**笔记的图片附件路径**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214184726.png)
- 设置笔记模板和笔记名模板
	- 笔记的**模板需要自己新建**，并将路径粘贴到Template File项里
	- 公众号回复"**同步**",可获取参考用笔记模板
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214185159.png)
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214184918.png)

#### 配置预览

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214184546.png)

### Zotero配置

#### 配置项

- 设置同步文件夹路径
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214185648.png)
- 设置默认的文件过滤器,根据我的修改就好
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214185721.png)
- 联动使用bbtx**的keyword：citekey**来识别
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214185731.png)
- 填写自己的**obsidian库名**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214185922.png)

#### 配置预览

- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214185527.png)

## 联动使用

### 导入zotero注释到obsdian库

- 在obsdian页面点击**crtl+p**，选择导入笔记（这是之前自己自定义的名称）
- 选择需要导入的条目
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214190133.png)

### 在zotero中同步标签

- 首次打开zotero会**自动同步条目**
- 也可以**手动同步条目**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214190401.png)
- 为同步条目的**自动标签添加颜色来辨识**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214190317.png)

### Zotero跳转obsidian

- 右键条目
- 选择**open note in obsidian跳转**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214190540.png)

## 其它注意事项

### 为obsidian不同颜色的注释添加颜色

- 使用CSS，并**在obsidian启用**。直接将CSS移动到图示路径，并启用
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214191023.png)
- CSS获取。公众号后台回复"**同步**"，可获取CSS文件
- **CSS**的修改
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214190821.png)

### 将callout修改为默认的收缩状态

- 将callout的默认修改为**收缩状态**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214191216.png)

### 修改不同注释颜色的call Out标题

- 将#的十六制颜色换为自己的常用注释颜色
- 修改标题，图示为修改#f9e196颜色为Important标题
![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214191333.png)
![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214191412.png)