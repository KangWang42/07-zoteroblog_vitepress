# 第18期 精华！ zotero使用常见bug及处理

---
类型: 公众号
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐
简记: 说不上多少实用
---

> 第18期 精华！ zotero使用常见bug及处理
> 
> 本期介绍了在使用过程中的，以及在与同学交流过程中。zotero的常见问题及处理方法。大部分是**zotero7**出现的问题，希望对大家有所帮助

## 1 软件问题

### 更多bug

关于其它zotero零零散散的bug可以看看青柠学术的[相关问答]([Issues · qnscholar/zotero-if-pro-max - Gitee.com](https://gitee.com/qnscholar/zotero-if-pro-max/issues))

里边的内容还是挺丰富的

### 知网论文无法抓取

- 阶段1
	- 使用茉莉花更新，**翻译器。并更新浏览器插件。全部重启**
- 阶段2
	- 阶段1无效后，考虑**手动更新翻译器js文件**
	- 流程见第二期
- 阶段3
	- 切换浏览器进行尝试
- 阶段4
	- 前**往中文翻译器github项目查看最近更新**，确认是共性还是特性的问题。
	- 可能存在知网页面改版导致抓取失效。那就慢慢等适配

### 主页面列宽过窄无法调整

- 图示（主要出现在zotero7里）
	- ![d3aad2f9f55a4d8dff880fec68dc0c6e_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/d3aad2f9f55a4d8dff880fec68dc0c6e_MD5.png)
- 查看软件保证是**最新版本**
- 考虑到有**列数设置相关的插件干扰**。（绿青蛙，zotero，茉莉花等。关闭插件后查看是否解决）
- 关闭插件解决后再慢慢打开插件，进行调整，考虑是否关闭哪个插件

### 插件禁用，显示安全模式

- ![741a7039e432c875f7d767204b76169b_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/741a7039e432c875f7d767204b76169b_MD5.png)
- 在主页面，**退出zotero**，重新进入即可
- ![268983068669bdfce438605179128959_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/268983068669bdfce438605179128959_MD5.png)

### Word参考文献插件无法使用

多在**zotero6更新zotero7后出现**

- ![3ce5ba50ce79cb368f6855f19c290556_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/3ce5ba50ce79cb368f6855f19c290556_MD5.png)
- 其它：考虑对zotero软件右键，兼容性模式运行

### 插件版本回退，插件无法使用

- **更新最新版本插**件！见我的18期推文，zotero7插件更新比较快。保持最新是顺利使用的保证
- 危：可能由于**坚果云同步**问题。同步时务必不要同步整个zotero文件夹（包含了配置文件的文件夹）。这样可能导致插件配置出问题。
- 正确配置（配置路径后会自动把附件上传到坚果云，**不要自己同步**）
	- ![8d39a4580da5a3da12a338d50447ddcf_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/8d39a4580da5a3da12a338d50447ddcf_MD5.png)

### 打开软件出现弹窗

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405271722863.png)

使用[zotero-addon](https://wk8686.top/zoteroepi68)来查看插件是否都是最新版

如果**不使用的插件不要打开**，不但可能因为不兼容导致冲突或者拖慢运行

## 2 插件使用问题

### Zotero-style 期刊标签不显示

需要**自行到easyscholar复制密钥**，到zotero里使用

![800696d29a36d1382fd616edefd9e0c3_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/800696d29a36d1382fd616edefd9e0c3_MD5.png)

具体流程见我的第6期推文

### Translate 翻译插件无法使用

- 设置条目语言，**确保条目语言为英语**翻译插件才起作用
- 是否选择了谷歌翻译，因**网络问题**无法使用

### 无法添加条目笔记

- 需要自行添加条目，**单pdf不显示阅读信息，也不能添加笔记**
- 抓取不到时请务必自己添加
- ![293d3407945e5af9d621a0029ce998fb_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/293d3407945e5af9d621a0029ce998fb_MD5.png)

### GPT插件无法使用

- 见[推文第10期](https://wk8686.top/archives/zoteroepi10)
- 如果使用官方密钥，**确保网络条件允许**
- 如果使用转发的国内密钥，请设置有用的**api地址，可在购买界面查看到**

### 显示有冲突的字段要处理

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405271735169.jpg)

- 随便点击一个版本进行选择即可
- 如果窗口大小受限无法选择，直接键盘按 **回车**
