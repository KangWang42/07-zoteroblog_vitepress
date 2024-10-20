# 第69期 软件教程 在zotero里配置安娜图书馆搜索引擎

---
类型: 公众号
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐
简记: 建议看
---

>第69期 软件教程 在zotero里配置安娜图书馆搜索引擎
>
>本期介绍如何添加安娜图书馆**搜索引擎到zotero中**
>
>实现快速检索**论文全文和免费图书资源**
>
>安娜图书馆目前还需要**稳定网络访问**

## 目录

[TOC]

## 使用效果

- 安娜图书馆可以当作**zlib和scihub的结合**
- 官方介绍**📚 人类历史上最大的真正开放的图书馆。 ⭐️ 镜像 Sci-Hub、LibGen、Z-Lib 等。**
- 具有极其丰富的**免费资源**
- 需要**稳定网络**![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401141318262.png)

## 引擎代码

```json
{
		"_name": "Anna Archive title and author",
		"_alias": "Anna Archive",
		"_description": "AnnaArchive Lookup",
		"_icon": "https://lh3.googleusercontent.com/sOX00LxhvUoMVoBEtSGXV9t10d57n4G1Q26wGc2nDmbh2l_elVUti-ULnTsUBnDlNM4_aab70w=s128-h128-e365",
		"_hidden": false,
		"_urlTemplate": "https://annas-archive.org/search?q={z:title}+{rft:aufirst?}+{rft:aulast?}",
		"_urlParams": [],
		"_urlNamespaces": {
			"z": "http://www.zotero.org/namespaces/openSearch#"
		},
		"_iconSourceURI": "https://lh3.googleusercontent.com/sOX00LxhvUoMVoBEtSGXV9t10d57n4G1Q26wGc2nDmbh2l_elVUti-ULnTsUBnDlNM4_aab70w=s128-h128-e365"
	}
```

## 使用方法

- 复制代码
- 粘贴到**zotero路径//locate//engine.json文件中**
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401141321282.png)

## 其它资源

- 公众号回复**240114**可获取打包好engine引擎
- 包含**丰富几十个引擎**
- 可直接替换zotero engine文件
