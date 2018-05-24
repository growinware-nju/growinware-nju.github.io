---
title: 非确定环境下的自适应系统验证技术
tags: ['研究进展']
date: 2018-04-23
---

![](/content/robocar-model.png)

非确定的感知与适应行为是否正确直接决定了自适应系统运行是否成功。例如，在无人自适应小车应用中，对环境测量的不确定性(例如由传感器误差导致)将可能导致自适应失效，从而违反软件的高层行为规约(specification)。

我们完成的工作实现了CPS系统的ISM (Interactive State Machine)建模和验证。

<!--more-->

![](/content/robocar-search.png)

并且实现了基于搜索(Search-based)算法的模型校准和反例确认，在15个机器人小车应用上证实了方法的有效性。

发表论文：
* Wenhua Yang, Chang Xu, Minxue Pan, Xiaoxing Ma, Jian Lu. Improving Veriﬁcation Accuracy of CPS by Modeling and Calibrating Interaction Uncertainty. In *ACM Transactions on Internet Technology*, 18(2), 2018. (第一标注)