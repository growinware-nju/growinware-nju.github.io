---
title: 基于移动设备内置摄像头的文本输入技术
tags: ['研究进展']
date: 2018-05-24
---

![](/content/camk.png)

近年来，移动设备逐渐向小型化发展，给用户与移动设备的交互带来了新的挑战。由于缺少物理键盘等外接设备，如何有效地向移动设备输入文本便是其中一个重要的挑战。为了解决这一问题，我们提出了基于移动设备内置摄像头的文本输入技术CamK。

<!--more-->

我们通过摄像头提取按键区域，感知用户的指尖运动，检测并定位微小的指尖输入动作，从而在一个仅有键盘布局的平面（如印有键盘布局的纸张上）实现文本输入。

![](/content/camk-1.png)
![](/content/camk-4.png)

基于Android平台，我们开发并实现了CamK文本输入技术，并对耗时的图像处理过程进行优化，使其能够在资源有限的移动设备（如智能手机）上有效运行。实验结果表明，CamK能够准确定位95%以上的按键操作，只有约4.8%的按键检测错误。

### 发表论文

* Yafeng Yin, Qun Li, Lei Xie, Shanhe Yi, Ed Novak, and Sanglu Lu. CamK: Camera-based Keystroke Detection and Localization for Small Mobile Devices. *IEEE Transactions on Mobile Computing*, 2018. (第一标注)