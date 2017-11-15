# 报警信息关联分析技术

传统的IDS往往注重于低层面的入侵和异常活动并独立地产生报警，忽视了这些报警信息之间可能存在的内在联系；

分布式入侵的特点要求分布式入侵检测系统应具有对反映同一入侵过程的不同报警信息进行关联分析的能力

根据来自系统内部不同入侵检测模块所产生的报警之间在特征上的相似性、在逻辑上的相关性，从系统整体的角度对分布式入侵进行分析的过程。

### 目的

更准确地把握入侵的发展动向，提高对入侵的分析能力

### 三类主要的关联分析技术

* 根据报警信息在属性上的相似性来实现关联分析
* 以S.Templeton提出的Requires/Provides模型和P.Ning提出的Prerequisites and Consequences模型为代表，根据报警所反映入侵的服务与被服务关系来进行关联。
* 以M.Y.Huang提出的入侵策略模型为代表


