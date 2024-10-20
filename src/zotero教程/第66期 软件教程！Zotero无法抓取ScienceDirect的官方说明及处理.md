# 第66期 软件教程！Zotero无法抓取ScienceDirect的官方说明及处理

---
类型: 公众号
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐
简记: zotero的抓取太受限了
---

>第66期 软件教程！Zotero无法抓取ScienceDirect的官方说明及处理
>
>近期ScienceDirect更新了反爬机制，主要表现为使用浏览器插件**无法获取到全文，只能抓取到网页快照链接**
>
>目前的解决办法是，**zotero7beta的手动验证；手动下载拖入；

## 目录

[TOC]

## 官方说明

- ScienceDirect 采用了一些非常严格的反爬取保护措施，这些措施可能会破坏 PDF 的保存，而这在大多数其他网站上是不会发生的。我们将尝试解决这个问题，但这需要一些工作。目前，**最好的办法是将 PDF 下载到磁盘，然后拖到 Zotero 中的新项目上。**
- 在 Zotero 7 测试版中，Zoteor推出了一项更改，**如果您在尝试保存文章时收到验证码，该页面将显示 ScienceDirect 验证码。如果您完成了验证码，Zotero 将继续下载当前文件，并能在该 Zotero 会话中更好地从 ScienceDirect 下载其他 PDF。**
- 验证码窗口出现在 Zotero 应用程序中，目前没有迹象表明从浏览器保存时打开过验证码窗口，因此如果 PDF 下载似乎卡住了，请切换到 Zotero 应用程序查看是否正在等待输入。我们会在那里提供更好的反馈。
- 同时**建议不要试图通过ScienceDirect一次下载很多文件，因为即使使用了验证码，也很可能会被阻止**。
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401111141660.png)

## 解决方法

### 手动下载PDF，并拖拽到zotero匹配条目元信息

![GIF 2024-1-11 11-43-35.gif](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401111143191.gif)

### 使用zotero7，手动验证后成功获取

- **zotero6版本无法解决**
- zotero7beta版本点击抓取后，**zotero回弹出验证框**
- **手动点击验证框确认**
- **显示成功抓取**
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401111145148.png)

## 相关网址

### zotero7下载

dev:zotero_7_for_developers|Zotero Documentation(https://www.zotero.org/support/dev/zotero_7_for_developers)

### Zotero官方相关讨论

Zotero is not saving PDFs from ScienceDirect - Zotero Forums(https://forums.zotero.org/discussion/109940/zotero-is-not-saving-pdfs-from-sciencedirect)

### zotero7和6的区别

第11期 Zotero6及Zotero7beta全方位比较
