# 状态转换分析\(State Transition Analysis\)

使用状态转换图来表示和检测入侵的方法。初始状态是指系统检测该入侵前的状态，而危险状态是指对应于入侵完成时的状态。

检测过程

在任意时刻，一定数量的入侵场景脚本与审计日志部分匹配，这时一些特征动作已经使系统到达各自状态转换图中的某些状态。如果某一个状态转换图达到了终止状态，则表示该入侵脚本已经成功匹配，否则，每个状态转换图的推理引擎将期待着下一个特征动作的到来，从而把状态转变为满足断言条件的下一个状态。





