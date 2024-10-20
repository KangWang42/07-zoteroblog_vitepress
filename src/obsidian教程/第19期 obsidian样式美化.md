# 第19期 obsidian样式美化

---
类型: 公众号
公众号内容: obsidian教程
rating:
  - ⭐⭐⭐⭐⭐
简记: 后台回CSS哈
---

> 第19期
> 最近学习CSS初有感悟，优化了shi一样的列表代码。这期是obsidian的css代码片段。近期会更新一期关于CSS 列表设置详细说明推文。帮助大家自定义自己喜欢的列表的样式

## 1 示意图

![5fb36427ce9aab0d8463b8ac44778105_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/5fb36427ce9aab0d8463b8ac44778105_MD5.png)

![cca8b056154248b2c2d498d3dee565b8_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/cca8b056154248b2c2d498d3dee565b8_MD5.png)

## 2 美化细节

- 图片美化
	- 添加边框
	- 添加原角
	- 设置最大宽度
- 列表美化
	- 缩小列表间的缩进，更加紧凑（**也可以自己修改**
	- 增加绿色左侧框
	- 在一级标题之间添加分割线
	- 二级以下标题字体减小
- 标题美化
	- 居中
	- 色块背景
	- 大小设置等，可自行添加后续标题（只设计了两个）
- 加粗和引用美化
	- 设置粗体的颜色和背景色
	- 设计引用的背景

## 3 代码

```CSS
 /* 对引用进行设计 */
 /* 对粗体文字设置橙色文字和淡色背景*/
 b, strong {
     color: rgba(255,69,0,1); /* 橙红色 */;
 background-color: #f0f0f0; /* 淡灰色背景 */
     padding: 2px 4px; /* 加点内边距让背景更明显 */
     border-radius: 2px; /* 可选：为背景添加圆角 */
 }

 
  /* 标题1设计，左侧边，居中，红色背景*/
 h1 {
  color: black!important;
   margin-bottom: 2em;
   margin-right: 5px;
   padding: 8px 15px;
   letter-spacing: 2px;
    /* 保持文字颜色为纯白色 */
   border-left: 10px solid rgba(240,19,19,0.5); /* 可以根据需要调整边框颜色 */
   background:rgba(240,19,19, 0.25);
   border-radius: 5px;
   text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* 文字阴影，增强对比 */
   box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.5); /* 盒子阴影，可根据需要调整 */
   text-align: center;
 }

 
   /* 标题2设计，左侧边，居中，绿色背景*/
 h2 {
  color: black!important;
   margin-bottom: 2em;
   margin-right: 5px;
   padding: 8px 15px;
   letter-spacing: 2px;
    /* 保持文字颜色为纯白色 */
   border-left: 10px solid rgba(102, 204, 153,0.5); /* 可以根据需要调整边框颜色 */
    background:rgba(102, 204, 153, 0.25);
   border-radius: 5px;
   text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* 文字阴影，增强对比 */
   box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.5); /* 盒子阴影，可根据需要调整 */
   text-align: center;
 }



  /* 图片设计，左侧边，居中，绿色背景*/
img{
  max-width:400px !important;
  width: auto; /* 对于其他图片保持原始宽度 */
  height: auto; /* 保持图片的高宽比 */
  border: 3px solid #a8d08d; /* 边框颜色和宽度 */
  padding: 0px; /* 边框内的填充 */
  background-color: white; /* 边框内部的背景颜色 */
  display: block;
  margin: 16px auto; /* 图片上下的间距，并在页面中居中显示 */
  box-shadow: 0px 0px 8px rgba(0,0,0,0.2); /* 阴影效果 */
  border-radius: 15px; /* 边框圆角 */
}

a[href]{
  color: black;
  text-decoration: none;
}


.markdown-embed-content{
  margin-bottom: 20px;
  padding: 20px auto;
}

/* 对粗体文字设置橙色文字和淡色背景*/
b, strong {
   color: rgba(255,69,0,1); /* 橙红色 */;
background-color: #f0f0f0; /* 淡灰色背景 */
   padding: 2px 4px; /* 加点内边距让背景更明显 */
   border-radius: 2px; /* 可选：为背景添加圆角 */
}

/* 标题1设计，左侧边，居中，红色背景*/
h1 {
color: black!important;
 margin-bottom: 2em;
 margin-right: 5px;
 padding: 8px 15px;
 letter-spacing: 2px;
  /* 保持文字颜色为纯白色 */
 border-left: 10px solid rgba(240,19,19,0.5); /* 可以根据需要调整边框颜色 */
 background:rgba(240,19,19, 0.25);
 border-radius: 5px;
 text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* 文字阴影，增强对比 */
 box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.5); /* 盒子阴影，可根据需要调整 */
 text-align: center;
}

/* 标题2设计，左侧边，居中，绿色背景*/
h2 {
color: black!important;
 margin-bottom: 2em;
 margin-right: 5px;
 padding: 8px 15px;
 letter-spacing: 2px;
  /* 保持文字颜色为纯白色 */
 border-left: 10px solid rgba(102, 204, 153,0.5); /* 可以根据需要调整边框颜色 */
  background:rgba(102, 204, 153, 0.25);
 border-radius: 5px;
 text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* 文字阴影，增强对比 */
 box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.5); /* 盒子阴影，可根据需要调整 */
 text-align: center;
}

/* 图片设计，左侧边，居中，绿色背景*/
img{
max-width:400px !important;
width: auto; /* 对于其他图片保持原始宽度 */
height: auto; /* 保持图片的高宽比 */
border: 3px solid #a8d08d; /* 边框颜色和宽度 */
padding: 0px; /* 边框内的填充 */
background-color: white; /* 边框内部的背景颜色 */
display: block;
margin: 16px auto; /* 图片上下的间距，并在页面中居中显示 */
box-shadow: 0px 0px 8px rgba(0,0,0,0.2); /* 阴影效果 */
border-radius: 15px; /* 边框圆角 */
}



/* 总体的边框设计，有序和无序的样式*/  
ol{
list-style-type: decimal;
border-left: 5px solid #a8d08d; /* 设置边框，这里使用浅绿色 */
border-radius: 10px; /* 圆角边框 */
text-indent: -5px;
}
ul {
border-radius: 10px; /* 圆角边框 */
border-left: 5px solid #a8d08d; /* 设置边框，这里使用浅绿色 */
}
/* 去除第二级有序列表项的底部边框 */
ul > li >ul > li ,
ol > li >ol > li,
ul > li >ul > li li,
ol > li >ul > li li
{
border-bottom: none;
border-left: none;
padding-bottom: 0px;
margin-left: 0px;
}
/* 先加上所有的分割线*/
ol > li:not(:last-child):not(li ol > li) {
border-bottom: 3px solid #ccc;
padding-bottom: 10px;
margin-bottom: 5px;
padding-top: 10px;
}
/*先加上所有的分割线 */
ul > li:not(:last-child):not(li ul > li) {
border-bottom: 3px solid #ccc;
padding-bottom: 20px;
margin-bottom: 5px;
margin-top: 5px;
padding-top: 10px;
}
/*为第二级及以下的列表项去除边框 */
ul li ul, ol li ol, 
ul li ol, ol li ul ,
ul li ul li ul,ul ul ul ul ul,
ol ol ol,ol ol ol ol{
border: none;
padding-left: 0;
margin-left: 0;
font-size: 17px;
}




```

## 4 使用方法

- 新建文件，后缀为.css.讲代码直接粘贴进去
	- ![439f3dd13be167fc721e2f2d490b82a7_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/439f3dd13be167fc721e2f2d490b82a7_MD5.png)
- 将css文件放置在ob路径为**.\\.obsidian\snippets**的文件夹里
	- ![00a949eafbc1a5e96d39bfce74320414_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/00a949eafbc1a5e96d39bfce74320414_MD5.png)
- obsdian设置的外观处打开
	- ![ace714fdb9a5dc430d354f0d3593b4c3_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/ace714fdb9a5dc430d354f0d3593b4c3_MD5.png)