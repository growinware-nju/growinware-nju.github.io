---
title: 基于分布Locality-Sensitive Hashing的云服务推荐技术
tags: ['研究进展']
date: 2018-05-23
---

![](/content/jsac-lsh.png)

在云服务提供商中，为用户提供满足其QoS需求的服务是至关重要的，而在跨云平台(例如Amazon、IBM等多个平台)的应用场景中，多个平台的信息整合成为一项研究挑战。本文介绍了如何利用LSH技术在解决隐私保护、准确、可扩展的服务推荐问题。

<!--more-->

### 论文摘要

To maximize the economic benefits, a cloud service provider needs to recommend its services to as many users as possible based on the historical user-service quality data. However, when a cloud platform (e.g., Amazon) intends to make a service recommendation decision, considering only its own user-service quality data is insufficient, because a cloud user may invoke services from multiple distributed cloud platforms (e.g., Amazon and IBM). In this situation, it is promising for Amazon to collaborate with other cloud platforms (e.g., IBM) to utilize the integrated data for the service recommendation to improve the recommendation accuracy. However, two challenges are present in the above-mentioned collaboration process, where we attempt to use multi-source data for the service recommendation. First, protecting users’ privacy is challenging when IBM releases its own data to Amazon. Second, the recommendation efficiency and scalability are often low when the user-service quality data of Amazon and IBM update frequently. Considering these challenges, a privacy-preserving and scalable service recommendation approach based on distributed locality-sensitive hashing, i.e., SerRec(distri-LSH), is proposed in this paper to handle the service recommendation in a distributed cloud environment. Extensive experiments on the WS-DREAM data set validate the feasibility of our approach in terms of service recommendation accuracy, scalability, and privacy preservation.

### 发表论文

* Lianyong Qi, Xuyun Zhang, Wanchun Dou, Qiang Ni. A Distributed Locality-Sensitive Hashing-Based Approach for Cloud Service Recommendation From Multi-Source Data. In *IEEE Journal on Selected Areas in Communications*, 35(11), 2017. (第一标注)