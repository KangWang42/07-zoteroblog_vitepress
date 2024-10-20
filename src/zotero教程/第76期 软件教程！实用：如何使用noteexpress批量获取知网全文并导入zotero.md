# 第76期 软件教程！实用：如何使用noteexpress批量获取知网全文并导入zotero

---
类型: 公众号
公众号内容:
  - zotero教程
rating:
  - ⭐⭐⭐
简记: 关键时刻起大用
---

>第76期 软件教程！实用：如何使用noteexpress批量获取知网全文并导入zotero
>
>有时候我们会遇到这种情况，**导师发来了一个包含百＋甚至千＋条目的题录，都是知网文献，希望检索到全文**
>
>这种情况下使用**学校合作的noteexpress是不错的选择，可以批量获取到知网全文**
>
>但是noteexpress的PDF阅读体验并不好，希望**导出到zotero阅读**，但noteexpress导出格式只能导出条目信息，**无法把附件一起导出**
>
>本期教程主要**介绍如何将noteexpress导出ris时附带附件路径，一起导入zotero**

## 目录

[TOC]

## 使用效果

![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401292353232.png)

## Noteexpress获取全文

- 如何将**题录导入noteexpress**不在本期范围
- 导出noteexpress题录![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401292354772.png)

## 导出ris题录文件

- 在文件夹或选中条目后右键**即可导出题录**
- 这个题录**用记事本打开后复制可直接剪贴板导入zotero**
- 但是这样直接导入是**没有附件的**，我们接下来要**在ris文件中添加附件路径**
![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401292358800.png)

## 找到noteexpress附件路径

- noteexpress附件路径就在仓库的目录下的**attachment文件夹**内
- 文件夹结构与软件内一致
- 找出自己**导出题录的附件的文件夹**
- 比如**我导出了计算机翻译文件夹下的题录，就去attachment中找计算机翻译文件夹之后会用到**
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401300012558.png)

## 修改RIS文件，添加附件路径

- 实现条件：**notexpress附件的路径没有加密，在附件文件夹中非常直观**
- 将**路径添加到ris之后导入条目就可以顺便导入附件**
- 手动添加**附件路径L1**这一步手动也能达成目的，但是如果条目几百个，一个个修改ris条目非常不现实，**接下来提供python代码和打包应用帮助大家简单实现ris批量修改**
- ![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401300002304.png)

## 使用python代码实现

- 非常抱歉没有注释的习惯，**代码根据附件文件夹和条目信息生成附件项给zotero识别**。
- noteexpress**默认情况下附件文件名就是条目名，这是代码的基础。如果不是的话可以在noteexpress设置的附件管理器中重命名**
- 实现的目的是**提供ris的路径**以及**附件文件夹的路径**两个参数,即可实现新的ris直接复制到剪贴板一键导入zotero
- ![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401300009915.png)
- 函数代码如下

```python
def generate_pdf_paths_for_ris_entries(ris_file_path, folder_path):
    with open(ris_file_path, 'r', encoding='utf-8') as file:
	    ris_content = file.read()
    updated_entries = []
    entries = ris_content.strip().split('ER  -\n')
    for entry in entries:
        lines = entry.split('\n')
        new_entry = []
        for i, line in enumerate(lines):
            new_entry.append(line)
            if line.startswith('TI  - '):
                title = line.replace('TI  - ', '').strip()
                safe_title = title.replace(':', '-').replace('/', '-').replace('\\', '-')
                pdf_path = f"L1  - {folder_path}/{safe_title}.pdf"
                new_entry.append(pdf_path)  # 将PDF路径添加到标题行之后

        updated_entry = '\n'.join(new_entry)
        updated_entries.append(updated_entry)
    updated_entries_list='\n\nER  -\n\n'.join(updated_entries) + '\n\nER  -'
    print(updated_entries_list)
    # 输出或保存更新后的RIS内容
    # 将更新后的RIS内容复制到剪贴板
    pyperclip.copy(updated_entries_list)
    print("Updated RIS content has been copied to clipboard.")
```

## 打包成应用可直接使用

- 考虑到部分朋友没有python条件，将代码打包后放在后台，回复“**240130**获取”
- 使用流程![image.png](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/202401300018904.png)
