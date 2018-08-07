---
title: 打造正则表达式攻击
tags: ['研究进展']
date: 2018-08-07
---

![](/content/rescue.png)

软件演化质量评估方法和保障机制的研究(软件适应与演化质量保障工具集)中，我们提出了ReScue技术，自动对正则表达式进行“Denial-of-Service攻击”的检测。

<!--more-->

### 论文摘要

Regular expression (regex) with modern extensions is one of the most popular string processing tools. However, poorly-designed regexes can yield exponentially many matching steps, and lead to regex Denial-of-Service (ReDoS) attacks under well-conceived string inputs. This paper presents ReScue, a three-phase gray-box analytical technique, to automatically generate ReDoS strings to highlight vulnerabilities of given regexes. ReScue systematically seeds (by a genetic search), incubates (by another genetic search), and finally pumps (by a regex-dedicated algorithm) for generating strings with maximized search time. We implemenmted the ReScue tool and evaluated it against 29,088 practical regexes in real-world projects. The evaluation results show that ReScue found 49% more attack strings compared with the best existing technique, and applying ReScue to popular GitHub projects discovered ten previously unknown ReDoS vulnerabilities.

### 发表论文

* Yuju Shen, Yanyan Jiang, Chang Xu, Ping Yu, Xiaoxing Ma, and Jian Lu. ReScue: Crafting Regular Expression DoS Attacks. In *Proceedings of the 33rd IEEE/ACM International Conference on Automated Software Engineering* (ASE 2018), Corum, Montpellier, France, Sep 2018. (第一标注)
