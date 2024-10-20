# 第26期 翻译插件最全详解，优化体验max！

---
类型: 公众号
公众号内容:
  - zotero插件教程
rating:
  - ⭐⭐⭐⭐⭐
简记: 打翻知云
---

>第26期
>
>本期主要介绍zotero7beta中**translate for zotero插件使用的详细配置和功能说明**。简单的翻译插件如果配置好了也可以极大提高英文文献的阅读效率

## 目录

[TOC]

## 页面展示

- 实现弹窗翻译
- 侧栏翻译
- 标题摘要翻译
- 翻译覆盖笔记
- 生词本功能
![2dc7614379c305446b38ca091c0947f8_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/2dc7614379c305446b38ca091c0947f8_MD5.png)

## 插件安装

### 安装网址

Releases · windingwind/zotero-pdf-translate --- 发布 · Windingwind/zotero-pdf-translate (github.com)(https://github.com/windingwind/zotero-pdf-translate/releases)

![7332b3299698e7d24dc9987f652f25d7_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/7332b3299698e7d24dc9987f652f25d7_MD5.png)

注意：**github部分区域需要稳定网络访问。公众号回复“插件”可直接获取

## 插件配置详解

### 概览

![1f5e480bcc1128218f26dbb34cf4f0b9_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/1f5e480bcc1128218f26dbb34cf4f0b9_MD5.png)

### 重要配置及说明

#### 自动翻译

建议打开**，对于英语不好的同学建议选上，如果英语可以或者喜欢英文阅读可以不开，手动点击翻译

#### 启用弹窗

如果对侧栏的阅读不满意，可启用翻译弹窗。即可实现**不开启侧栏的沉浸体验**

#### 自动翻译批注

**建议打开**，可将**注释笔记自动翻译为中文**，在主页面可结合zotero-style插件进行更好的论文注释回顾

#### 添加翻译到笔记

**建议打开**。进行笔记摘录的过程中，可直接将翻译的文本摘录到笔记中，减去了自己辅助的步骤
![24c571a114d1c84219e9a0252fba356b_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/24c571a114d1c84219e9a0252fba356b_MD5.gif)

#### 翻译引擎设置

- 引擎类型
	- 不需要密钥，不需要特殊网络**如有道等，知网海词等**
	- 需要密钥，不需要特殊网络**如小牛翻译，deepl等**
	- 不需要密钥，需要特殊网络**如谷歌等**
	- 需要密钥，需要特殊网络如**chatgpt**
- 建议使用
	- 知网翻译，不需要密钥，准确度较高（**但是文本过长会报错**）
	- **谷歌翻译**：速度快，准确度较好，文本不限，**好！**
	- deepl：需要获取密钥，但**准确性最好，速度一般**
	- chatgpt：准确性一般，胜在流畅，**有条件建议使用4.0模型，3.5效果不如谷歌**
- 密钥获取
	- 可在各翻译网站的官网获取
	- 部分有免费额度：**小牛翻译**等
	- chatgpt，deepl虽然有免费额度，但需要绑定支付方式，获取难度高

## 功能详解

### 弹窗翻译

在鼠标选中文本后，**跟随光标会出现弹窗并实时进行翻译**。弹窗大小可拖动设置

![18382d3cba71474024e175a592dd8470_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/18382d3cba71474024e175a592dd8470_MD5.png)

### 侧栏翻译

功能同弹窗翻译，但不占用PDF原空间，**形式与小绿鲸，知云等翻译引擎接近。**

![f45644b7af27af877d5d66ceef766d61_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/f45644b7af27af877d5d66ceef766d61_MD5.png)

### 标题摘要翻译

在主页面可对**标题摘要一键翻译**。放置到专门的条目，便于浏览

![baf307b93e4360e8e2881d5bba12dc9d_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/baf307b93e4360e8e2881d5bba12dc9d_MD5.gif)

![1bab80ef4fd1486738b775c88d136cff_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/1bab80ef4fd1486738b775c88d136cff_MD5.png)

### 翻译覆盖笔记

对注释进行翻译，**减轻回顾的阅读压力**

可在主笔记页面搭配zotero-style插件，**实现中文回顾及快速跳转**

![b6cce479485fa4312d1f440d8480efbd_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/b6cce479485fa4312d1f440d8480efbd_MD5.png)

### 生词本功能

打开**生词本功能**

即可实现单词选中时，进行**词语翻译**。有助于英语学习及生词熟记。

![47f92df40bd3292a74c2e18874d6185d_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/47f92df40bd3292a74c2e18874d6185d_MD5.png)

## 使用注意事项

### 报错分析

- 如果使用谷歌翻译，chatgpt，**检查网络服务是否符合要求（重要！）**
- 使用小牛翻译，chatgpt，考虑到为额度已满，**到官网查看**
- 知网翻译，可能是选中文本过长，超出限制

### 如何在主页面实现翻译替换英文标题

- 使用**zotero-style的标题设置**
- ![9b9094f70841ad03c6447368e8a71da2_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/9b9094f70841ad03c6447368e8a71da2_MD5.gif)

### 确认翻译可用，但无法实现自动翻译

务必保证翻译论文的条目信息中语言项为英语（**en，en-US**），**不能是中文**！

![0660d4d9eddeca4d82c61d810cace36b_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/0660d4d9eddeca4d82c61d810cace36b_MD5.png)