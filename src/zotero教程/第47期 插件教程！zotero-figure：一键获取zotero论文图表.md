# 第47期 插件教程！zotero-figure：一键获取zotero论文图表

---
类型: 公众号
公众号内容:
  - zotero插件教程
rating:
  - ⭐⭐⭐⭐
简记: 很不错，当然有的图片抓不到
---

> 第47期 插件教程！zotero-figure：一键获取zotero论文图表，为科研助力
> 
> 本期介绍MuiseDestiny大佬的又一精品插件 **zotero-figure**
> 
> 插件的作用是实现 当前论文**图表的一键抓取和快速添加笔记**
> 
> 虽然使用人数相对较少，但功能非常强

## 效果展示

- 图表截取
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222113958.png)
- 笔记预览（结合zotero-style插件）
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222114108.png)

## 插件安装

- 安装网址： MuiseDestiny/zotero-figure (https://github.com/MuiseDestiny/zotero-figure/releases)
	- 下载xpi文件（图示为zotero7版本）
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222114620.png)
	- 注意：**github部分区域需要稳定网络访问**可公众号后台回复 **插件** 获取最新插件
- 进入zotero-工具-附加组件-**Install Add-on From Files**-选择下载的xpi文件进行安装

## 插件配置

### 下载pdffigures2.jar组件，移至数据文件夹

- 如何下载pdffigures2.jar
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222115027.png)
	- 可公众号后台回复"插件"一键获取组件
- 将pdffigures2.jar移动至数据文件夹
	- 将第一步获取的pdffigures2.jar文件移动到数据文件夹内
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222115350.png)

### 安装java应用并配置到设置中

- 安装网址：Java Archive Downloads - Java SE 18 (oracle.com)(https://www.oracle.com/java/technologies/javase/jdk18-archive-downloads.html)
- 安装后**获取java.exe启动路径**
	- 路径参考
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222115512.png)
- 将java.exe添加到zotero编辑器的path.java项中
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231222115724.png)

### 撒花，配置好啦，大家可以享受zotero-figure带来的便捷

- 单击图片，复制图片到剪贴板，配合 [Snipaste](https://www.snipaste.com/) 粘贴到屏幕
- 双击图片，独立窗口预览，需要安装 [Zotero Better Notes](https://github.com/windingwind/zotero-better-notes) 插件
- 单击图注跳转到 PDF 对应图位置

## 其它注意

- 注意：图片获取根据论文质量有关，部分论文**无法获取完全**，可尝试重新获取
- 插件图片调用其它项目，故插件本身很难修bug，**一般更新也比较少**
- 所以如果部分论文图标无法完全获取放过就好