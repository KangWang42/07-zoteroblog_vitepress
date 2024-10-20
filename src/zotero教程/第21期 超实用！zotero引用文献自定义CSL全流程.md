# 第21期 超实用！zotero引用文献自定义CSL全流程

---
类型: 公众号
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐⭐
简记: 可以看看，引用的时候很需要
---

> 第21期
> 
> 本期主要介绍如何在zotero里**对引用文献的格式进行自定义修改**。获得自己需要的引文格式

## 目录

[TOC]

## 展示效果

网站链接：[CSL Code Editor (citationstyles.org)](https://editor.citationstyles.org/codeEditor/)

网站特点：

- 可以以可视化块的形式**快速对样式进行编辑**，实现个性需求。
- 可以检索到大量的样式，**迅速找到适合的模板**
- ![0b3a4c44f92870577bc8d369f0774e5a_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/0b3a4c44f92870577bc8d369f0774e5a_MD5.png)
- ![6bc370006014889e73587797212e76cb_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/6bc370006014889e73587797212e76cb_MD5.png)

## 全流程一览

### 确定自己需要的引文格式

- 如进行论文投稿，可直接在zotero样式管理器中进行搜索，查看是否符合要求
	- ![1e805ecbb5cf966a7a00a48aa9deebfa_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/1e805ecbb5cf966a7a00a48aa9deebfa_MD5.png)
	- ![ea59a1cbff77e1d97b91ac313ee8e9ed_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/ea59a1cbff77e1d97b91ac313ee8e9ed_MD5.png)
- **在CSL Code Editor**网站进行模糊搜索
	- ![46e9c02f973b69b7a2b90b0c4d5c33ab_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/46e9c02f973b69b7a2b90b0c4d5c33ab_MD5.png)

### 已确定基础引文样式，根据自定义需求进行修改

如果找不到完全一致的样式，寻找尽量接近的样式。之后的微调通过CSL Code Editor的可视化操作页面实现

#### 删除元素

- 定位元素（删除后缀为macro的元素）
- 直接单机delete删除
- ![e278c83b9a8d5174176755b415f0e9b2_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/e278c83b9a8d5174176755b415f0e9b2_MD5.png)

#### 添加元素

- 注意事项
	- 先点击元素，进行定位
	- **不要对varible直接修改前后缀**，查看括号类型为macro的元素添加
	- 查看效果
- 添加**前缀后缀**![a36fdbb5bac4ba27579e639dfa8bddb1_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/a36fdbb5bac4ba27579e639dfa8bddb1_MD5.png)

#### 样式修改

- 修改说明
	- 预览处选中需要修改的元素进行定位
	- 在变量窗口选中**括号后缀为variable变量**进行样式的修改和选择
	- ![cf0e6bd50c9a72970d7249acc9af8bab_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/cf0e6bd50c9a72970d7249acc9af8bab_MD5.png)

#### 作者显示修改

- 引用文献修改
	- ![83f46948f85a20b57920d432c6b89a3a_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/83f46948f85a20b57920d432c6b89a3a_MD5.png)
- 参考文献表修改流程
	- ![c4ab72bed79ae1a22d9a855faf97afcb_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/c4ab72bed79ae1a22d9a855faf97afcb_MD5.png)
- 指示说明
	- **delimiter-precedes-et-al**: 当使用“et al.”（等人）来替代作者列表时，此设置定义在“et al.”前是否应该放置分隔符。例如，当此选项设置为“always”时，引用会显示为“Smith, Jones, et al.”；当设置为“never”时，显示为“Smith, Jones et al.
	- **delimiter-precedes-last**: 在列出多个项目（如作者、编辑）时，这个设置定义在最后一个项目前是否应该放置分隔符。例如，设置为“always”时，引用会显示为“Smith, Jones, and Brown”，而设置为“never”时，显示为“Smith, Jones and Brown”。
	- **et-al-min**: 在使用“et al.”来缩减作者列表时，此设置定义开始使用“et al.”的最小作者数量。例如，如果设置为“5”，则当一个作品有5个或更多作者时，会使用“et al.”。
	- **et-al-use-first**: 与“et-al-min”结合使用，此设置定义在使用“et al.”时应列出的最初几位作者的数量。例如，如果“et-al-min”为5，且“et-al-use-first”为3，则在有5个或更多作者的作品中，将列出前3位作者，后面跟着“et al.”。
	- **et-al-subsequent-min** 和 **et-al-subsequent-use-first**: 这两个设置类似于“et-al-min”和“et-al-use-first”，但适用于同一文献的后续引用。第一次引用可能列出更多的作者，而后续引用则可能只列出少数几位。
	- **et-al-use-last**: 此设置控制是否在列出部分作者后还要在列表末尾添加最后一个作者的名字。一般较少使用。
	- **initialize**: 此设置控制作者名中的名字（给定名）是否应缩写为首字母。例如，如果设置为true，则“John Smith”会显示为“J. Smith”。

### 自定义csl导出及zotero里使用

- 从网页中导出
	- ![97f1dcdc5d00b3cf951aaafd91ce5c0d_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/97f1dcdc5d00b3cf951aaafd91ce5c0d_MD5.png)
- 导入zotero
	- ![317673c9808573e8efed9c22d16bb029_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/317673c9808573e8efed9c22d16bb029_MD5.png)

## 其它

### 导出自己的引文到网站预览

#### 从zotero中导出CSL JSON格式

![2db63059442380e8c0cab142499a1891_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/2db63059442380e8c0cab142499a1891_MD5.png)

#### JSON引文列表导入网站

- 打开JSON文件，复制所有内容
- 选择**网页可视化编辑的引用列表框**
- **点击advanced，将json内容粘贴**
- ![2ba3906b2265a482fe84c4789aea47ad_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/2ba3906b2265a482fe84c4789aea47ad_MD5.png)

### 插件推荐

可以使用官方的引用，在word里安装插件

![89be87c1f98d16168c10d506a5afb8ca_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/89be87c1f98d16168c10d506a5afb8ca_MD5.png)

也可以使用插件 zotero-citation

实现以下特点

- 拖拽引用（总zotero直接拖到word）
- 快捷键引用，单击对应“'”键即可实现citation插入
- 参考文献表，一个word里的引文会在zotero里新建组来展示

安装见往期推文内容

### 不知道论文样式名，只知道示例应该长什么样

在CSL Code Editor-search by sample网站进行样式搜索

我这里最近一直打不开呀，这个设置可能后续可以试试什么时候开放

![3615b3115f02a3f8ac870ae4c26e1f2a_MD5](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/3615b3115f02a3f8ac870ae4c26e1f2a_MD5.png)

### 中英文混排etal 等的设置

可参考网站(https://github.com/redleafnew/Chinese-STD-GB-T-7714-related-csl)
