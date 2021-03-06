---
author: quote
layout: post-full
title: 模型压缩6倍，无需重训练
featimg: https://p3-tt.byteimg.com/origin/pgc-image/8af4c59af36540d3ab824582991c53fe.jpg
tags: [nn]
category: [deeplearning]
---
> RUDN 大学的数学家团队找到一种新方法，该方法能够让神经网络的大小减小到六分之一，且无需花费更多的资源重新训练。

![模型压缩6倍，无需重训练：数学家团队提出量化新方法](https://p3-tt.byteimg.com/origin/pgc-image/8af4c59af36540d3ab824582991c53fe.jpg)



神经网络压缩是指在对神经网络性能影响不大的情况下，通过有关方法来减少网络的参数和存储空间，大体上可以分为近似，量化和剪枝三类方法。

近日，来自俄罗斯人民友谊大学（RUDN）的数学家团队找到一种方法，可以**将训练后的神经网络的大小减小六倍，而无需花费更多的资源来对其进行重新训练**。该方法基于找到初始系统及其简化版本中神经连接权重之间的相关性。这项研究的结果发表在《Optical Memory and Neural Networks》期刊上。

生命体中人工神经网络和神经元的结构是基于相同的原理。网络中的节点是相互连接的；其中一些接收信号，一些通过激活或抑制链中的下一个元素来发送信号。任何信号（例如图像或声音）的处理都需要很多网络元素及其之间的连接。但是，计算机模型只有有限的模型容量和存储空间。为了处理大量数据，这一领域的研究者必须发明各种方法来降低对模型能力的需求，包括所谓的量化。这有助于减少资源消耗，但需要对系统进行重新训练。RUDN 大学的一些数学家发现后者可以避免。

![模型压缩6倍，无需重训练：数学家团队提出量化新方法](https://p1-tt.byteimg.com/origin/pgc-image/f9c3b94bc5fa480fb70c81af9df465d7.jpg)



RUDN 大学 Nikolskii 数学研究所助理教授 Iakov Karandashev 博士说：「几年前，我们在 Hopfield 网络中进行了有效且经济高效的权重量化。这是一个关联存储网络，并带有遵循 Hebb 规则形成的元素之间的对称连接。在其运行过程中，网络的活动被降低到某个平衡状态，并且在该状态达到时任务就被认为是已经解决了，该研究中获得的见解后来被应用于当今在图像识别中非常流行的前馈深度学习网络。通常这些网络需要在量化后进行重新训练，而我们找到了避免重新训练的方法。」

简化人工神经网络背后的主要思想是所谓的权重量化，即减少每个权重的位数。量化提供信号的均值化：例如，如果将其应用于图像，则代表相同颜色不同阴影的所有像素将变得相同。从数学上讲，这意味着借助某些参数的相似神经连接应该具有相同的权重（或重要性），即表示成同一个数字。

RUDN 大学的一个数学家团队进行了计算并创建了公式，该公式可以有效地在量化前后，在神经网络的权重之间建立相关性。基于此，科学家们开发了一种算法，利用该算法，经过训练的神经网络可以对图像进行分类。在该研究的实验中，数学家使用了包含 5 万张照片的数据集，这些照片包可以被分为 1000 组。训练之后，该网络会使用新方法进行量化，并且不进行重新训练。然后，该研究将实验结果与其他量化算法进行了比较。

RUDN 大学的 Iakov Karandashev 补充说道：「量化之后，分类准确率仅降低了 1％，但是所需的存储容量减少了 6 倍。实验表明，由于初始权重与量化后权重之间的相关性很强，该网络不需要重新训练。这种方法有助于在完成时间敏感任务或在移动设备上运行任务时节省资源。」

感兴趣的读者可以阅读期刊原文。

参考原文：

https://www.eurekalert.org/pub_releases/2021-02/ru-rum020521.php

论文链接：

https://link.springer.com/article/10.3103/S1060992X20030042

https://arxiv.org/abs/2002.00623

> https://www.eurekalert.org/pub_releases/2021-02/ru-rum020521.php
>
> https://www.toutiao.com/i6930829362640159243