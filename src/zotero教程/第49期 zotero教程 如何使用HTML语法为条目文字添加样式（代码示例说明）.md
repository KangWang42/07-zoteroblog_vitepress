# 第49期 zotero教程 如何使用HTML语法为条目文字添加样式（代码示例说明）

---
类型: 公众号
公众号内容:
  - zotero教程
简记: 感觉有些问题
rating:
  - ⭐⭐
---

>第49期 zotero教程 如何使用HTML语法为条目文字添加样式（代码示例说明）
>
>本期介绍如何对zotero条目信息的特定文字和内容添加样式
>
>通过自定义的加粗，斜体，背景色等，实现更加优雅的zotero美化；
>
>本文以[zoterostyle](https://wk8686.top/zoteroepi8)为例介绍简记的显示样式如何修改。如果使用linter插件也可对其它字段样式修改

## 目录

[TOC]

## 展示效果

- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231220160927.png)
- 通过HTML语法，实现条目内容的
	- 加粗
	- 斜体
	- 横线
	- 背景色
	- 字间距
	- 字体颜色
	- 等等，本文仅展示zotero常用的或可能会用到的HTML语法

## 代码

### HTML语法大致说明

- HTML（HyperText Markup Language）是构建网页和网络应用的标准标记语言。它不是一种编程语言，而是一种用于定义网页内容结构的语言。HTML 使用标签来描述网页上的内容。下面是一些基本的HTML语法元素。在zotero里，也可以**使用html语法进行zotero展示样式的修改**
- **直接标签**设置语法，以bold标签为例
	- 左右的**b（bold）标签**，代表标签内文本展示为加粗样式
	- 同理的标签为i（斜体）
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231220161201.png)
- **内嵌样式设置语法**，以背景颜色设置为例
	- 标签左右的span表示是一个**无样式**的常用内容块
	- 样式内嵌在标签的style属性里，示例设置是背景色为**黄色**
	- 同理的语法可以设置**字体块的背景，字体，字号，字体是否居中，字体间距等（非常丰富）**
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231220161416.png)
- 注意：部分语法如加粗斜体，也可以在内嵌的样式里设置。语法是自由的。但大家只要会大致的结构用就可以了。具体的话要学习CSS和HTML语法

### 可直接复制粘贴使用语法代码

#### **文本加粗**

使用 \<b> 或 \<strong> 标签

```html
<b>这是加粗文字</b>
```

#### **文本斜体**

使用 \<i> 或 \<em>标签。

```html
<i>这是斜体文字</i>
```

#### **文字横线**

使用 \<s> 或 \<del> 标签。

```html
<s>这是有横线的文字</s>
```

#### **文字背景色**

使用内联样式 `style` 属性设置 `background-color`。

```html
   <span style="background-color: yellow;">这是有黄色背景的文字</span>
```

#### **字体颜色**

使用内联样式 `style` 属性设置 `color`。

```html
   <span style="color: blue;">这是蓝色字体的文字</span>
```

#### **字间距**

使用内联样式 `style` 属性设置 `letter-spacing`。

```html
   <span style="letter-spacing: 2px;">这是字间距增加的文字</span>
```

#### **字体上标**

使用 \<sup> 标签。

```html
   <p>这是上标<sup>上标文字</sup></p>
```

#### **字体下标**

使用 \<sub> 标签。

```html
   <p>这是下标<sub>下标文字</sub></p>
```

#### **设置同时斜体又有背景色**

```html
<span style="background-color: yellow; font-style: italic;">这是斜体且有黄色背景的文字</span>
```

#### 为整个**文本块**设置背景色

**为个文本块设置背景色而不仅仅是文字本身**，可以将背景色应用于一个容纳文字的较大的HTML元素，如\<div>。例如，如果您想设置一个既包含斜体文本又有背景色的文本块

```html
<div style="background-color: lightblue; text-align: center;">
这是斜体文字
</div>
```

### 如何使用

- 直接在zotero的属性栏里填入代码，**并且把代码里的文字改为自己需要的文字**
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231220104433.png)

### 使用linter插件进行快捷设置

- 安装网址：northword/zotero-format-metadata: Linter for Zotero. (github.com)(https://github.com/northword/zotero-format-metadata)
- 可公众号后台回复“**插件**”直接获取
- 下载插件并安装，zotero插件安装方式见往期推文
- 点击条目栏的信息，单击，**弹出样式设置框**，进行样式设置
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231220162040.png)