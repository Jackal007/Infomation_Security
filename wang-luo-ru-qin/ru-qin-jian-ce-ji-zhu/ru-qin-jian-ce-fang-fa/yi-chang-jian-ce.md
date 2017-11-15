# 异常检测

主要是通过检测用户的异常行为来发现入侵事件。

检测方法的原则：任何与已知行为模型不符合的行为都被认为是入侵行为。

### 实现方法

* 统计方法、预测模式生成法、神经网络、免疫原理，SVM
* 隐马尔可夫模型HMM
* 遗传编程
* 聚类技术
* 粗糙集理论
* 孤立点发掘

### 优点

可以对新的入侵行为模式进行检测

### 不足

* 误报率高
* 偏离界限值的对整个系统的检测性能有较大影响；
* 当用户的行为发生改变时，可能会导致系统误报；
* 对于新用户，系统的学习阶段何时结束不易确定；
* 入侵者可以通过一段时间的训练，使一个基于统计度量的系统渐渐将其入侵行为归为正常行为。
* 无法准确描述入侵的具体特征（比如攻击类型、目的等）

### 基于无监督学习的异常检测技术

##### 理论依据

异常行为同正常行为有明显区别；

异常行为数量相对于正常行为来说，所占比例较小；

##### 常用方法

聚类

将所得到聚类结果中，包含记录最多的类作为正常，而其他作为异常处理

孤立点检测

将孤立点作为异常处理

##### 特点

对样本要求不象有监督学习异常检测那样苛刻

离线检测




