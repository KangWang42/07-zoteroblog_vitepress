# 第52期 插件教程！tara：zotero的多端备份插件

---
类型: 公众号
公众号内容:
  - zotero插件教程
简记: 数据最珍贵
rating:
  - ⭐⭐⭐⭐
---

>第52期 插件教程！tara：zotero的多端备份插件
>
>本期介绍zotero的备份插件tara（蒲公英）
>
>插件的主要功能是一键备份 **zotero插件，zotero插件配置，zotero引用样式，zotero翻译器**
>
>同时介绍一下如何win系统实现**手动备份**zotero的全数据

## 目录

[TOC]

## 效果展示

### 配置导出

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224221528.png)

### 配置导入及恢复

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224221703.png)

## 插件安装

- 安装网址： Releases · l0o0/tara (github.com)(https://github.com/l0o0/tara/releases)
	- 下载xpi文件（图示为zotero7版本）
	- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224221933.png)
	- 注意：**github部分区域需要稳定网络访问**；也可进入[网页在线下载](https://wk8686.top/cusgit)直接下载或进入[我的云盘](https://wk8686.top/file/?0%20%E5%85%AC%E4%BC%97%E5%8F%B7/0%20zotero_%E6%8F%92%E4%BB%B6%E5%90%88%E9%9B%86/%E6%8F%92%E4%BB%B6-z7%20beta68%E5%90%8E) 进行下载
- 进入zotero-工具-附加组件-**Install Add-on From Files**-选择下载的xpi文件进行安装

## 插件使用（zotero7为例）

### 创建备份

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224222116.png)

### 导出备份

数据会保存在数据文件夹的**backup目录**中（用于转移到另一台电脑中使用该备份恢复）

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224222330.png)

### 导入备份

用于不同电脑的zotero的**快速设置与恢复**

在新的zotero里**安装tara插件**

在新电脑使用tara插件选择**导入**，并选中**zip备份包**

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224222543.png)

### 恢复备份

在同一设备中点击恢复，选中时间节点

在不同设备中**首先要导入，再点击恢复**

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224222630.png)

## 如何手动设置备份（无奈的时候用tara已经挺好用）

手动备份可以实现数据的无损备份，包括但不仅限于**账户、插件、设置、文献**等数据。

首先您需要在新电脑上安装 Zotero，然后将旧电脑的**配置文件夹及数据文件夹**拷贝到新电脑的同一位置。

配置文件夹的转移确保是**同一位置**，同时要做好备份工作（是的，**备份的备份**）

### Win系统配置文件夹

**zotero数据源目录：C:\\Users<用户名>\\AppData\\Roaming\\Zotero\\Zotero\\Profiles\\\*\.default 中文件**
注意事项
- AppData是隐藏目录，需要设置**显示隐藏文件夹**后进入
- 转移的过程中务必保证，两个电脑的zotero都是**关闭的**，避免出现无法访问的情况

### Win系统数据文件夹

包含了**zotero的翻译器，数据文件等**

注意事项

- 数据文件夹复制的时候务必**复制完整**
- 转移的过程中务必保证，两个电脑的zotero都务必**关闭的**，避免出现无法访问的情况，导致**传输不全**
![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231224223519.png)

## 注意事项

### 跨系统间的恢复还不完整

如从mac到win的恢复，或者mac到win的恢复

可能会出现**恢复不完整**的情况

建议**同系统内的恢复**

### 帮别人配置的时候注意自己的信息

如果帮同学或老师配置插件的过程中**省事使用了tara**

会一起将自己的可能的**有价值信息**给一起备份

包括但不限于

- **gpt密钥**
- **easyscholar密钥等**


