---
title: 基于反例概率最大化的自适应系统验证
tags: ['研究进展']
date: 2018-05-24
---

![](/content/robocar-experiment.png)

在自适应系统的验证中，生成实际中可能发生(概率最大化)的反例以供开发者进行调试能提高自适应应用开发的效率。本研究工作实现有效的自适应系统验证，使用约束求解问题(遗传算法求解)构造发生概率最大的反例，并在真实系统应用上进行了验证。

<!--more-->

### 论文摘要

Self-adaptive applications’ executions can be affected by uncertainty factors like unreliable sensing and flawed adaptation and therefore often error-prone. Existing methods can verify the applications suffering uncertainty and report counterexamples. However, such verification results can deviate from reality when the uncertainty specification used in verification is itself imprecise. This thus calls for further validation of reported counterexamples. One outstanding challenge in counterexample validation is that the probabilities of counterexamples occurring in real environment are usually very low, which makes the validation extremely inefficient. In this paper, we propose a novel approach to systematically deriving path-equivalent counterexamples with respect to original ones. The derived counterexamples guarantee to have higher probabilities, making them capable of being validated efficiently in field test. We evaluated our approach with real-world self-adaptive applications. The results reported that our approach significantly increased counterexample probabilities, and the derived counterexamples were also consistently and efficiently validated in both real environment and simulation.

### 发表论文

* Wenhua Yang, Chang Xu, Minxue Pan, Chun Cao, Xiaoxing Ma, Jian Lu. Efficient Validation of Self-adaptive Applications by Counterexample Probability Maximization. In *Journal of Systems and Software*, 138, 2018. (第一标注)