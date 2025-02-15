# 第57期 插件教程！zotero-linter 关于条目元信息的插件说明

---
类型: 公众号
公众号内容:
  - zotero插件教程
rating:
  - ⭐⭐⭐⭐
简记: 必安插件，引用的时候就知道了
---

> 第57期 插件教程！zotero-linter 关于条目元信息的插件说明
> 
> 本期介绍zotero实用插件，**Linter for zotero**的使用教程及功能说明
> 
> Linter for zotero作用主要为：**1：设置条目信息的快捷展示样式修改（参考第49期）；2：标题修改Toolbar；3：添加重复文献时进行检查；4：根据期刊全名查找期刊缩写；5：根据DOI查找日期、卷数、期数、页数等；6：根据标题自动填写条目的语言**

## 目录

[TOC]

## 展示效果（包含常用功能）

### 设置标题下标、粗体、斜体等展示样式

![GIF 2023-12-29 13-23-49.gif](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/GIF%202023-12-29%2013-23-49.gif)

### 重复项目检测

![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231229132751.png)

### 根据期刊全名查找期刊缩写

- 该插件内置了约 96,000 个期刊缩写的数据集（来自 JabRef 和 Woodward Library），该插件会首先在**本地数据集中查找期刊缩写；**
- 如果没有可用的缩写，则从 **ISSN 标题词**缩写列表中推断出缩写（可选）；
- 如果仍然没有找到缩写，则用期刊的**全名替换**（可选）。
![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231229133135.png)

### 根据标题自动填写项目的语言

- 用于满足CSL同时引用**中英文文献**的需要
- 中文文献根据标题自动设置为**zh-CN**
- 英文设置为**en-US**
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231229133844.png)

### 将标题从“标题大小写”转换为“句子大小写”

- Zotero 的文档建议以“句子大小写”格式存储标题，这将允许 CSL 对它们执行“**标题大小写**”转换。Zotero 7有一个内置功能，**可以将标题转换为“句子大写**”，并且预设了一些特殊情况检测，**并且该插件通过添加对专有名词（例如化学式）的识别进行了扩展**
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231229134213.png)

### 更多功能

#### 去掉DOI的URL前缀

将日期转换为 **ISO 格式**

#### 根据DOI查找日期、卷数、期数、页数等

Zotero 库中的某些项目可能会添加不完整的信息，例如由于翻译者不可用而导致期刊卷页，或者记录时正式出版物不在期刊中等。**该插件基于 DOI可以对这些信息进行填补**。

#### 根据大学名称查找大学所在地

该插件**内置了中国大陆大学及其位置的列表**。论文项目按照论文所在大学填写地点，有助于**满足GB/T 7714-2015对论文显示地点的要求**

#### 项目类型检查

添加项目时，如果其项目类型是网页且其 URL 包含主要学术出版商的域，则**提示用户询问是否导入了错误类型的项目。**

## 插件安装

- 安装网址： 
	- zotero7:(**https://github.com/northword/zotero-format-metadata/releases**)
	- zotero6:(**https://github.com/northword/zotero-format-metadata/releases/tag/0.4.4**)
	- 下载**xpi文件**（图示为zotero7版本）
	- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231229135830.png)

	- 注意：**github部分区域需要稳定网络访问**可公众号后台回复 **插件** 获取最新插件
- 进入zotero-工具-附加组件-**Install Add-on From Files**-选择下载的xpi文件进行安装

## 其它

### 标题样式快捷键操作

- 与word中的快捷键一致
- 上标： **Ctrl + Shift + "+"**
- 下标： **Ctrl + =**
- 粗体： **Ctrl + B**
- 斜体： **Ctrl + I**
- 无大小写： **Ctrl + N** （设置 class="nocase" 以防止某些特殊名称在 CSL 标题大小写模式下大写）

### 说明

- 大部分批量信息修改包含自动修改的功能
- 同时包含手动批量修改的功能

### 手动样式修改

- 见第49期内容





