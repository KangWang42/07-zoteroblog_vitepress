# 第20期 zotero列表间距调整详细指南！

---
类型: 公众号
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐
简记: 不用看，后台直接回CSS就好
---

> 第20期，主要对列表的元素设计进行了区块化介绍，如果要修改相应的部分可自定义实现。（我的列表用的是比较多的，目前的版本是唯一比较满意的。而且改了之前很多shi一样的代码，可读性提升
> 如果看不懂可以直接粘贴到zotero用。有问题再看下边的推文

## 目录

[TOC]

## 1 展示效果

主要涉及到各边距的修改，让浏览更加顺滑

更新之后又设置列无序列表开始是**多彩的实心圆**。如果想删除参考后续把styletype改成none就行

![33e81d747050bed25a5d21efd7f001ce_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/33e81d747050bed25a5d21efd7f001ce_MD5.png)

![0663cf71539e97888a91fd0721150ff1_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/0663cf71539e97888a91fd0721150ff1_MD5.png)

## 2 总代码

```css
  /* 边框设计*/  
  ol {
    list-style-type: decimal;/* 设置有序列表，这里用升序的数字 */
    border-left: 5px solid #a8d08d; /* 设置边框，这里使用浅绿色 */
    border-radius: 10px; /* 圆角边框 */
    text-indent: -5px;/* 设置字符的缩进，这里把数字和后边跟的文字拉近 */
  }
  
  ul{
    list-style-type:disc;     /* 不带点了*/
    border-radius: 10px; /* 圆角边框 */
    border-left: 5px solid #a8d08d; /* 设置边框，这里使用浅绿色 */
  }
  
  /* 设置低级列表（不是第一级）和上一级的缩进，以及列表间的缩进。可以自己再添添，我用不到那么多项*/
  ol > li > ol > li > ol > li,
  ul > li > ol > li,
  ol > li > ol > li
  {
  padding-bottom: 8px;  /* 二级列表之后行内间距的设置 */
  margin-left: -20px; /* 减小缩进 */
  }
  
  ul > li > ul > li,
  ol > li > ul > li,
  ul > li > ul > li> ul > li, 
  ul > li > ul > li> ul > li> ul > li
  {
    padding-bottom: 4px;  /* 二级列表之后行内间距的设置 */
    margin-left: -10px; /* 不同级别列表之间的缩进程度，设成负数更紧凑 */
    }

/* 重要：一级列表距离左侧边框的缩进 */
  ul>li{
    margin-left: -10px;
  }
  ol>li{
    margin-left: 0px;
  }
  
  /* 仅为第一级有序列表项添加底部分割线 ，最后一个不设*/
  ol > li:not(:last-child):not(li ol > li) {
  border-bottom: 3px solid #ccc;
  padding-bottom: 10px;
  margin-bottom: 5px;
  padding-top: 10px;
  }
  
  /* 仅为第一级无序列表项添加底部分割线，最后一个不设*/
  ul > li:not(:last-child):not(li ul > li) {
  border-bottom: 3px solid #ccc;
  padding-bottom: 20px;
  margin-bottom: 5px;
  margin-top: 5px;
  padding-top: 10px;
  }

   /* 一级列表最后一个项到底边的距离*/
  ul > li:last-child:not(li ul > li){
    padding-bottom: 15px;
    padding-top: 10px;
  }
  
  ol > li:last-child:not(li ul > li){
    padding-bottom: 15px;
    padding-top: 10px;
  }

  /* 每级列表到前一段的间距 */
  ol li:first-child {
    margin-top: 5px;
  }
  ul li:first-child {
    margin-top: -5px;
  }

  /* 为第二级及以下的列表项去除边框，设计大小*/
  ul li ul, ol li ol, 
  ul li ol, ol li ul{
  border: none;
  font-size: 15px;
  }
  
/* 根据嵌套层级改变颜色，只改变marker的颜色，如果去掉的话就是改不同级别文字的颜色*/
ul>li::marker, ol>li::marker{ color: red;font-size: 15px;}
ul>li>ul>li::marker, ul>li>ol>li::marker, ol>li>ul>li::marker, ol>li>ol>li::marker { color: rgb(44,80,196);font-size: 15px;}
ul>li>ul>li>ul>li::marker, ul>li>ul>li>ol>li::marker,
ul>li>ol>li>ul>li::marker, ul>li>ol>li>ol>li::marker,
ol>li>ul>li>ul>li::marker, ol>li>ul>li>ol>li::marker,
ol>li>ol>li>ul>li::marker, ol>li>ol>li>ol>li::marker { color: green;font-size: 15px;}

```

## 3 CSS使用方法

- 打开zotero软件，进入编辑-设置-高级界面
- 打开**编辑器**
- 搜索CSS，在extensions.zotero.note.css项直接填入CSS代码即可
- ![31445f77a3da26d1f6ede484e612a15d_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/31445f77a3da26d1f6ede484e612a15d_MD5.png)

## 4 各部分介绍

- 序号标太乱不改了，主要看注释介绍即可。摸索着修改应该比较简单。如果有问题可以公众号私信
- 设置无序列表的符号（空着还是实心圆）
	- ![f9c432164d2a2721370e88cdd193c2f5_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/f9c432164d2a2721370e88cdd193c2f5_MD5.png)
- 设置列表的**marker**（数字呀，点呀，前边符号的样式）在这里设置**列表前符号的大小**
	- ![26e020f83026d37b94ef890f72dd1815_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/26e020f83026d37b94ef890f72dd1815_MD5.png)
- border-radius设置原角大小。text-indent。设置有序列表的数字和文字的间距
	- ![947b7565b6236bd86699f8efae774c8a_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/947b7565b6236bd86699f8efae774c8a_MD5.png)
- 设置低级列表（不是第一级）和上一级的**左右缩进差距**，以及列表间的**上下间距**。可以自己再添添，我用不到那么多项
	- ![87dfc7ad2e4833ee1bb60088089bba00_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/87dfc7ad2e4833ee1bb60088089bba00_MD5.png)
- **设置重要的一级列表最左侧间距（序号1）**
	- ![306fb7db2fb35c8d95274afbe6abc878_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/306fb7db2fb35c8d95274afbe6abc878_MD5.png)
- 使用伪元素，先设置一级列表的非最后元素的**底边分割线**
	- ![73ca6e067ce4c2ca9d24db7fc3536fdb_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/73ca6e067ce4c2ca9d24db7fc3536fdb_MD5.png)
- **最后一个一级列表的样式**
	- ![71a90906b9779abbd4fe82247e381b11_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/71a90906b9779abbd4fe82247e381b11_MD5.png)
- 除一级列表外其它列表的第一个item到上一个列表末尾的间距（**序号3，4）**
	- ![b10706e5639afc1a228b318c17f6b84e_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/b10706e5639afc1a228b318c17f6b84e_MD5.png)
- 去除二级一下列表的边框，顺便设置了一下**字号（低级列表字号小一些）**
	- ![43b6a02c8a54ced7dcb1f7a76b58caee_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/43b6a02c8a54ced7dcb1f7a76b58caee_MD5.png)

