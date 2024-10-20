# 第90期 软件教程 敲一个好看的better-notes笔记模板（文中附代码）

---
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐⭐
简记: 很好
类型: 公众号
---

>第90期 **敲一个好看的betternotes插件模板（文中附代码）**
>
>zotero7beta的zotero-better-notes插件更新后功能性极大提升，**做了一个模板来优化自动笔记**
>
>本期分享一下自己制作的**笔记模板**
>
>针对我对模板的期望：**美观性（论文基础信息，好的框架） 实用性（相关链接，注释添加，伪目录跳转）**

## 本期大纲

[TOC]

## 参考网站

插件教程：**第87期 better-notes教程**

模板制作教程网站：[zotero-better-notes (github.com)笔记制作总教程](https://github.com/windingwind/zotero-better-notes/blob/master/docs/about-note-template.md#note-template-structure)

官方条目信息(想自己修改模板可以看看）：[zotero-map-journalArticle](https://aurimasv.github.io/z2csl/typeMap.xml#map-journalArticle)

[更多模板（一些条目信息片段是参考这里的）](https://github.com/windingwind/zotero-better-notes/discussions/categories/note-templates)

## 模板效果

![模板效果](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404191159827.gif)

## 模板使用

侧栏笔记状态的目录跳转有点问题呀，**还是推荐在better-notes的笔记窗口看笔记**，或者把笔记那一段better-notes代码删除就行

为SCI阅读提供的模板，因为需要调用摘要翻译标题翻译这样的元信息，**中文文献和其它类型是不兼容的**

模板基于beta74版本，需要插件：**zotero-style；zotero-translate；zotero-betternotes**

better-notes的模板代码做好后，在模板编辑器和笔记区的显示并不一致。某些样式设置无法显示，所以为了更好的显示效果，**我采用的是“css代码”+“模板代码”结合使用的方式**，效果就是上图，使用方式见下

### Betternote模板安装

![betternote模板安装](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404191216818.png)

betternotejs模板

```javascript
# This template is specifically for importing/sharing, using better 
# notes 'import from clipboard': copy the content and
# goto Zotero menu bar, click Edit->New Template from Clipboard.  
# Do not copy-paste this to better notes template editor directly.
name: "[Item] sci_paper_by_wk"
content: |-
  <!-- author:wk-->
  
  <h1 style="font-size: 1.4em; margin-bottom: 2em; margin-right: 5px; padding: 8px 15px;letter-spacing: 2px;color: #000000;border-left: 10px solid rgba(240, 19, 19, 0.5);background: rgba(240, 19, 19, 0.25); border-radius: 5px; text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2); box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.5); text-align: center">${topItem.getField("title")}</h1>
  
  
  <table style="width:100%; border-collapse: collapse;">
    <tr>
      <th style="border: 1px solid black; min-width: 35%; padding: 8px; text-align: left;">标题翻译</th>
      <td style="border: 1px solid black; padding: 8px;">${topItem.getField("titleTranslation")}</td>
    </tr>
    <tr>
      <th style="border: 1px solid black; min-width: 35%; padding: 8px; text-align: left;">作者</th>
      <td style="border: 1px solid black; padding: 8px;">	${topItem.getCreators().map((v) => v.firstName + " " + v.lastName).join("; ")}</td>
    </tr>
    <tr>
      <th style="border: 1px solid black; min-width: 35%; padding: 8px; text-align: left;">出版年份</th>
      <td style="border: 1px solid black; padding: 8px; text-align: center;">${topItem.getField('date')}</td>
    </tr>
    <tr>
      <th style="border: 1px solid black; min-width: 35%; padding: 8px; text-align: left;">期刊</th>
      <td style="border: 1px solid black; padding: 8px; text-align: center;">${topItem.getField('publicationTitle')}</td>
    </tr>
    <tr>
      <th style="border: 1px solid black; min-width: 35%; padding: 8px; text-align: left;">期刊等级</th>
      <td style="border: 1px solid black; padding: 8px; text-align: center;">${{
  let space = " ㅤㅤ ㅤㅤ"
  return Array.prototype.map.call(
  	Zotero.ZoteroStyle.api.renderCell(topItem, "publicationTags").childNodes,
  	e => {
  		e.innerText =  space + e.innerText + space;
  		return e.outerHTML
  	}
  	).join(space)
  }}$</td>
  </tr>
    <tr>
      <th style="border: 1px solid black; min-width: 35%; padding: 8px; text-align: center;">论文标签</th>
      <td style="border: 1px solid black; text-align: center; padding: 8px;">${topItem.getTags().map(tagObj=>tagObj.tag)}</td>
    </tr>
    <tr>
      <th style="border: 1px solid black; padding: 8px; text-align: left;">附件链接</th>
      <td style="border: 1px solid black; padding: 8px;color:#4A148C">
      <a href=${{
    async function getPDFLink(item) {
      const att = await item.getBestAttachment();
      if (!att || !att.isPDFAttachment()) {
        return "";
      }
      key = att.key;
      if (att.libraryID === 1) {
        return `zotero://open-pdf/library/items/${key}`;
      } else {
        groupID = Zotero.Libraries.get(att.libraryID).id;
        return `zotero://open-pdf/groups/${groupID}/items/${key}`;
      }
    }
    sharedObj.getPDFLink = getPDFLink;
    return await getPDFLink(topItem);
  }}$>
          ${topItem.getField("title")}
        </a>
      </td>
    </tr>
    <tr>
      <th style="border: 1px solid black; padding: 8px; text-align: left;">摘要</th>
      <td style="border: 1px solid black; padding: 8px;">${topItem.getField('abstractTranslation')}</td>
    </tr>
  </table>
  
  <hr/>
  <h2 style='text-align:center'>目录</h2>
  <table style="text-align:center;width:100%; border-collapse: collapse; margin: 0 auto; background-color: white; box-shadow: 0 2px 10px rgba(0,0,0,0.1);">
    <tr>
      <td style="padding: 10px;" ><a href="#back" style="text-decoration: none; color: black;">点此跳转</a></td>
      <td style="padding: 10px; background-color: #FFF8E1;">📜 背景</td>
    </tr>
    <tr>
      <td style="padding: 10px;" ><a href="#cont" style="text-decoration: none; color: black;">点此跳转</a></td>
      <td style="padding: 10px; background-color: #F1F8E9;">🔬 研究内容</td>
    </tr>
    <tr>
      <td style="padding: 10px;"><a  href="#result" style="text-decoration: none; color: black;">点此跳转</a></td>
      <td style="padding: 10px; background-color: #F5F5F5;">🚩 研究结果</td>
    </tr>
    <tr>
      <td style="padding: 10px;" ><a href="#creat" style="text-decoration: none; color: black;">点此跳转</a></td>
      <td style="padding: 10px; background-color: #E0F7FA;">📌 创新点</td>
    </tr>
    <tr>
      <td style="padding: 10px;" ><a href="#other" style="text-decoration: none; color: black;">点此跳转</a></td>
      <td style="padding: 10px; background-color: #E1F5FE;">🔬 其它</td>
    </tr>
    <tr>
      <td style="padding: 10px;" ><a href="#anno" style="text-decoration: none; color: black;">点此跳转</a></td>
      <td style="padding: 10px; background-color: #E1F5FE;">📌 PDF注释</td>
    </tr>
  </table>
  
  <em style='font-size:7px;text-align:center!important;color:#9e9e9e;margin-top: 30px;'>点击 Ctrl+左键 即可跳转</em>
  
  
  
  <br/>
  <hr/>
  
  
  <h2 id="back">📜 背景</h2> 
  <p ></p><hr/>
  <h2 id="cont">🔬 研究内容</h2> 
  <p ></p><hr/>
  <h2 id="result" >🚩 研究结果</h2> 
  <p ></p><hr/>
  <h2 id="creat">📌 创新点</h2>
  <p ></p> <hr/>
  <h2 id="other">🔬 其它</h2> 
  <p ></p> <hr/>
  <h2 id="anno">📌PDF注释</h2>
  <p ></p>  
  ${{
    async function getAnnotationsByColor(_item, color) {
      const annots = _item
        .getAnnotations()
        .filter((item) => item.annotationColor === color);
      if (annots.length === 0) {
        return "";
      }
      return Zotero.BetterNotes.api.convert.annotations2html(annots, {
        noteItem: targetNoteItem,
      });
    }
    
    const attachments = Zotero.Items.get(topItem.getAttachments()).filter((i) =>
      i.isPDFAttachment()
    );
    
    let res = ``;
    
    const colors = {
      "#f9e196": "⭐ 知识-有趣的观点、事实、例子", // Yellow
      "#f0bbcb": "⚠️ 重要的方法", // Magenta
    };
    for (const attachment of attachments) {
      res += `📄For Document:${attachment.attachmentFilename}`;
      for (const color in colors) {
        if (Object.hasOwnProperty.call(colors, color)) {
          const colorName = colors[color];
          const renderedAnnotations = await getAnnotationsByColor(
            attachment,
            color
          );
          if (renderedAnnotations) {
            res += `<h4><p style="background-color:${color};">${colorName}</h4></p>\n${renderedAnnotations}`;
          }
        }
      }
      const renderedAnnotations = await getAnnotationsByColor(
        attachment,
        (_annot) => !colors.includes(_annot.annotationColor)
      );
      if (renderedAnnotations) {
        res += `<h4><p>Other Annotations</p></h4>\n${renderedAnnotations}`;
      }
    }
    return res;
    }}$
    
    
    <hr />

```

### CSS代码使用

![CSS代码使用](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404191208629.png)

CSS代码

```css
/* 为表格设置边框样式 */
/* 设置表格的边框样式 */
table {
  border-collapse: collapse;
  width: 100%;
}

/* 设置第一列的宽度 */
table th:first-child, table td:first-child {
  width: 30%; /* 例如设置第一列宽度为表格宽度的50% */
  font-size: 0.9em;
  text-align: center;
  vertical-align:middle!important;
}

table th {
  font-size: 1.1em!important;
  text-align: center !important; /* 文本居中 */
  font-weight: bold !important; /* 文本加粗 */
  border: 2px solid black; /* 边框加粗 */
  padding: 5px; /* 添加一些内边距 */
  color: #1e6bb8 !important; /* 设置文字颜色 */
  background-color: rgba(21,100,178,0.1);
}

table tr:nth-child(2n) {
  background-color: #F8F8F8;
}
h2 {
  font-size: 1.1em;
  margin-bottom: 2em;
  margin-right: 5px;
  padding: 8px 15px;
  letter-spacing: 2px;
  color: #000000; /* 保持文字颜色为纯白色 */
  border-left: 10px solid rgba(102, 204, 153, 0.5); /* 可以根据需要调整边框颜色 */
  background: rgba(102, 204, 153, 0.25);
  border-radius: 5px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2); /* 文字阴影，增强对比 */
  text-align: center;
}
h1 {

  font-size: 1.2em;
  margin-bottom: 2em;
  margin-right: 5px;
  padding: 8px 15px;
  letter-spacing: 2px;
  color: #000000; /* 保持文字颜色为纯白色 */
  border-left: 10px solid rgba(240, 19, 19, 0.5); /* 可以根据需要调整边框颜色 */
  background: rgba(240, 19, 19, 0.25);
  border-radius: 5px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2); /* 文字阴影，增强对比 */
  box-shadow: 1px 1px 2px rgba(51, 51, 51, 0.5); /* 盒子阴影，可根据需要调整 */
  text-align: center;
}
```

## 模板修改建议

### CSS模板修改建议

就是一些简单的CSS代码样式修改，之前还写过zotero笔记样式美化，当时写得代码太臭了。如果希望zotero的笔记样式好看，倒也可能先拿来用

如果希望具体学习一下CSS代码，推荐我看得两本书

- （英）安迪·巴德（Andy Budd），（瑞典）埃米尔·比约克隆德（Emil Bj.rklund）. (2019). _精通CSS_ (TP393.092.2). 人民邮电出版社. [_精通CSS_ (TP393.092.2). 人民邮电出版社](http://book.ucdrs.superlib.net/views/specific/2929/bookDetail.jsp?dxNumber=000017932719&d=E71E6A034540FEB24182AD60C614D069&fenlei=1817041103010901)
- 达科特. (2013). _HTML  &  CSS  设计与构建网站_. [_HTML  &  CSS  设计与构建网站_. ](http://book.ucdrs.superlib.net/views/specific/2929/bookDetail.jsp?dxNumber=000011699905&d=3268AF23277E23EC486E34BC26C6CE68&fenlei=1817040302)

### Betternote模板修改

- 就看我第一部分推荐的参考网站就行；**里边介绍了简单的语法和一些js脚本来使用**
- 模板整体使用html代码，其中文本部分在笔记中支持markdown
- 如果修改代码，**可以自行添加html内容块，并且用js来调用论文元信息**
- ![简单的修改](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404191228847.png)
- 常用的js脚本见下
	- ![常用js脚本](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404191226855.png)
- 官方的js查看
	- 官方条目信息(想自己修改模板可以看看）：[zotero-map-journalArticle](https://aurimasv.github.io/z2csl/typeMap.xml#map-journalArticle)
	- ![官方条目信息](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202404191235159.png)

**其它插件生成的条目信息调用**

zotero-style-期刊标签

```
${{
let space = " ㅤㅤ ㅤㅤ"
return Array.prototype.map.call(
	Zotero.ZoteroStyle.api.renderCell(topItem, "publicationTags").childNodes,
	e => {
		e.innerText =  space + e.innerText + space;
		return e.outerHTML
	}
	).join(space)
}}$
```

标题翻译

```
${topItem.getField("titleTranslation")}
```

摘要翻译

```
${topItem.getField('abstractTranslation')}
```

调取注释

```
${{
  async function getAnnotationsByColor(_item, color) {
    const annots = _item
      .getAnnotations()
      .filter((item) => item.annotationColor === color);
    if (annots.length === 0) {
      return "";
    }
    return Zotero.BetterNotes.api.convert.annotations2html(annots, {
      noteItem: targetNoteItem,
    });
  }
  
  const attachments = Zotero.Items.get(topItem.getAttachments()).filter((i) =>
    i.isPDFAttachment()
  );

  let res = ``;
  
  const colors = {
    "#f9e196": "⭐ 知识-有趣的观点、事实、例子", // Yellow
    "#f0bbcb": "⚠️ 重要的方法", // Magenta
  };
  for (const attachment of attachments) {
    res += `📄For Document:${attachment.attachmentFilename}`;
    for (const color in colors) {
      if (Object.hasOwnProperty.call(colors, color)) {
        const colorName = colors[color];
        const renderedAnnotations = await getAnnotationsByColor(
          attachment,
          color
        );
        if (renderedAnnotations) {
          res += `<h4><p style="background-color:${color};">${colorName}</h4></p>\n${renderedAnnotations}`;
        }
      }
    }
    const renderedAnnotations = await getAnnotationsByColor(
      attachment,
      (_annot) => !colors.includes(_annot.annotationColor)
    );
    if (renderedAnnotations) {
      res += `<h4><p>Other Annotations</p></h4>\n${renderedAnnotations}`;
    }
  }
  return res;
  }}$
```