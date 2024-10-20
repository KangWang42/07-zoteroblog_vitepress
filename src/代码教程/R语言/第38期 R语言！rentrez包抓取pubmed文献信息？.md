# 第38期 R语言！rentrez包抓取pubmed文献信息？

---
类型: 公众号
公众号内容:
  - 代码-R教程
rating:
  - ⭐⭐
简记: 简单的教程
---

>第38期 R语言！rentrez包抓取pubmed文献信息？
>
>本期介绍如何使用rentrez包来批量抓取相关主题的文献信息
>
>入手简单，非常舒适
>
>公众号回复**231314**获取rmd源码

## 目录

[TOC]

## 展示效果

### 同时抓取不同主题的不同文献，自定义主题及抓取文献数

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/4db062e1b3360c5c79cbbb8f0c07c64.png)

### 对所有文献进行可视化

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/594193e5f577517bba3e94adbe79d98.png)

## 实现代码

### Rentrez介绍

- rentrez
	- rentrez 是一个 R 语言包，主要用于与 NCBI（美国国家生物技术信息中心）的各种数据库进行交互，包括 PubMed、GenBank 等。这个包提供了一系列函数，可以在 R 语言环境中直接进行数据的检索、下载和处理，非常适合生物信息学、基因组学以及相关领域的研究人员使用。
	- 本期使用rentrez来进行**文献获取**

### 载入包

```R
install.packages("rentrez")
install.packages("brcueR")
library(bruceR)#包内包含了tidyverse系列包,很方便
library(rentrez)
```

### 单主题，确定索引数

```R
# 设定主题词 ，参考pubmed索引规则
query_term=("COVID-19")
#设定索引多少文献
index=1:20

data <- tibble(
  index=index
) %>%unnest(index)%>% 
  rowwise() %>% 
   mutate(result=entrez_search(db = "pubmed",term =query_term)$ids[index],
  ) %>%ungroup() %>% 
  mutate(summary=entrez_summary(db="pubmed",id=result)
  ) %>%unnest_wider(summary)
```

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/20231214102214.png)

### 多主题，自定义每一个的索引数

```R
query_list=list("COVID-19","health","cancer")  #设定主题列表
index_list=list(1:20,1:18,1:15)                #设定每个主题需要多少论文，如果需要多设置retmax参数


data <- tibble(
  query=query_list,
  index=index_list
) %>%unnest(index)%>% 
  rowwise() %>% 
   mutate(result=entrez_search(db = "pubmed",term =query)$ids[index],
  ) %>%ungroup() %>% 
  mutate(summary=entrez_summary(db="pubmed",id=result)
  ) %>%unnest_wider(summary) %>% 
  group_by(query)%>% 
  nest

data %>% pull(data,query) %>%      #使用bruceR包，将结果快捷导出到excel
  export("result.xlsx")

```

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/4db062e1b3360c5c79cbbb8f0c07c64.png)

### 单主题，检索所有文献。并进行可视化

```R


query="microplastic AND cancer"

index=length(entrez_search(db = "pubmed",
                           term =query,
                           retmax=300)$ids)     #注意retmax是需要自己设定过多最大论文数，可以先试试index最多多少

data_all <- tibble(index=1:index) %>% 
   mutate(result=entrez_search(db = "pubmed",term =query,retmax=300)$ids[index],
  ) %>%ungroup() %>% 
  mutate(summary=entrez_summary(db="pubmed",id=result)
  ) %>%unnest_wider(summary)


#进行优雅的可视化
data_all%>%select(index,pubdate) %>% 
  mutate(pubdate=str_sub(pubdate,1,4)) %>% 
  mutate(pubdate=as.numeric(pubdate)) %>% 
  group_by(pubdate) %>% 
  summarise(期刊数=n()) %>% 
  ungroup() %>% 
  ggplot(aes(x=pubdate,y=期刊数)) +
  geom_bar(stat = "identity",fill="#2B6B96")+
  geom_line(color="#071BC9",linewidth=1)+
  geom_point(color="#071BC9",size=4)+
  theme_classic()+
  geom_text(aes(y=期刊数+3,label=期刊数))+
  scale_color_lancet()+
  labs(x="年份",y="发表数",title=query) +
  theme(plot.title = element_text(hjust = 0.5),
        plot.margin =margin(t = 0, r = 0, b = 0, l = 0, unit = "pt"))+
  scale_y_continuous(limits = c(0, 60))
```

![](https://pic-go-42.oss-cn-guangzhou.aliyuncs.com/img/594193e5f577517bba3e94adbe79d98.png)

## 注意事项

使用 `rentrez` 包时的注意事项：

- **API Key**：在大量使用或频繁请求 NCBI 数据库时，建议注册并使用 NCBI 的 API Key，这可以提高请求的限制。 
- **查询限制**：NCBI 对于没有使用 API Key 的请求有频率限制。过于频繁的请求可能导致暂时性的访问限制。 
- **查询精确度**：构建查询语句时需要注意其精确度和相关性，以便获取到最相关的数据。 
- **网络稳定性**：由于 `rentrez` 包依赖于网络来访问 NCBI 的数据库，因此网络的稳定性对于数据检索的成功率有重要影响。
- **数据处理**：获取的数据可能需要进一步的处理和解析，根据研究需求对数据进行适当的处理和分析。