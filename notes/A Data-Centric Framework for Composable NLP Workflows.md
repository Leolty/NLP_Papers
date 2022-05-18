# A Data-Centric Framework for Composable NLP Workflows

## 1. Url and bib

https://aclanthology.org/2020.emnlp-demos.26/

```bibtex
@inproceedings{liu-etal-2020-data-centric,
    title = "A Data-Centric Framework for Composable {NLP} Workflows",
    author = "Liu, Zhengzhong  and
      Ding, Guanxiong  and
      Bukkittu, Avinash  and
      Gupta, Mansi  and
      Gao, Pengzhi  and
      Ahmed, Atif  and
      Zhang, Shikun  and
      Gao, Xin  and
      Singhavi, Swapnil  and
      Li, Linwei  and
      Wei, Wei  and
      Hu, Zecong  and
      Shi, Haoran  and
      Liang, Xiaodan  and
      Mitamura, Teruko  and
      Xing, Eric  and
      Hu, Zhiting",
    booktitle = "Proceedings of the 2020 Conference on Empirical Methods in Natural Language Processing: System Demonstrations",
    month = oct,
    year = "2020",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2020.emnlp-demos.26",
    doi = "10.18653/v1/2020.emnlp-demos.26",
    pages = "197--204",
}
```



## 2. Key contribution

establish a framework:

1.  a **uniform data representation** to encode heterogeneous results

2.  a **large repository of processors** for NLP tasks, visualization, and annotation

3.  extensible, allows plugging


## 3. Framework
### 3.1 Infrastructure

#### 3.1.1 data representation

![Data-Centric-1](..\images\Data-Centric-1.png) 

##### basic data types:

- span: offset of a piece of text



- ​link: (parent, child)


- group: collection of markups



##### extended data types:

- more types of data can be extended (customized data)

- kind of like **extend** in Java



##### flexible data sources



#### 3.1.2 Facilitation for Neural Modeling

- embedding,  rich data operation, hybrid modelling (neural & symbolic)

  ​



### 3.2 Processor

- each processor to interacts with each other via the data flow

  ​



### 3.3 Visualization, Annotation and Interaction
- different UI interface for different kinds of tasks

  ​



## 4. Conclusion

a framework for building complex NLP workflows: 
-  universal data representation (basic, extended, flexible sources)
-  facilitaiton for modelling (BERT/auto-batching/hybrid modelling ..... )
-  flexible(?) processors
-  friendly interface/interaction