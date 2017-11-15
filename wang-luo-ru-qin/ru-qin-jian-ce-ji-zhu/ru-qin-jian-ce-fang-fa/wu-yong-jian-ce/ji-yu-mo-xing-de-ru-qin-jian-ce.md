# 基于模型的入侵检测

原理：特定的场景脚本（scenarios\)可以由特定的可观察的活动推导出来。因而通过观察，可以推导出特定的入侵场景脚本的一系列活动，检测出入侵企图。

组成模块：

预期者（anticipator\)：使用活动模型和脚本模型来预测脚本中下一个期望发生的事件，脚本模型为已知脚本的知识库。

计划者（planner\)：将该假设转化成该行为在审记日志中应出现的格式。计划者利用预期者所预测的信息来计划下一步查找什么数据。

解释者\(interpreter\)：在审记日志中查找该数据。
