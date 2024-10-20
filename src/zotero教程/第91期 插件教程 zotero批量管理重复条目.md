# 第91期 插件教程 zotero批量管理重复条目

---
公众号内容:
  - zotero插件教程
rating:
  - ⭐⭐⭐
简记: 可以看看
类型: 公众号
---

> 第91期 软件教程 zotero批量管理重复条目
> 
> 本教程基于zotero7beta版本，使用插件**zoplicate**
> 
> 插件介绍：一个只做一件事的插件，**检测和管理 Zotero 中的重复项目。**
> 
> zotero7自带有重复条件监测和合并功能，但**无法实现批量合并和导入时自动化监测**。本期介绍插件就是为了弥补这方面的功能
## 效果展

### 导入条目自动处理

每次导入重复条目时会进行提示，并选择处理方式（可以进行默认设置）

![导入条目自动处理](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405061036850.gif)

### 批量合并重复条目

![批量合并重复条目](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405061038173.png)

### 插件设置

![插件设置](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405061031849.png)

## 插件功能说明

- **重复条目检测**
    - 检测新导入的项目是否与 Zotero 库中现有项目重复。
    - **保留新条目**：保存最后导入的条目并删除其余的。
	- **保留旧条目**：**删除最后导入的条目并保存其余的。**
	- **全部保留：保留新条目和现有条目**
    - 手动合并：跳转到zotero的重复条目面板并手动合并重复项目。
- **自动批量合并**
    - 自动合并库中的**所有重复条目**。
    - 手动合并所有**重复条目**
- 非重复管理
    - 如果 Zotero 错误地将项目识别为重复项，则允许将条目标记为**“非重复项**”。
    - 在版本 3.0.0 中引入。

## 插件安装

- 安装网址：[ChenglongMa/zoplicate (github.com)](https://github.com/ChenglongMa/zoplicate/releases)
- 下载**xpi文件**（图示为zotero7版本）
- ![插件安装](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202405061100855.png)

- 注意：**github部分区域需要稳定网络访问**可公众号后台回复 **插件** 获取最新插件
- 进入zotero-工具-附加组件-**Install Add-on From Files**-选择下载的xpi文件进行安装