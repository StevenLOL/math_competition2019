# math_competition2019
2019年中国研究生数学建模竞赛D题-汽车行驶工况构建
三、解决的问题
1.数据预处理
由汽车行驶数据的采集设备直接记录的原始采集数据往往会包含一些不良数据值，不良数据主要包括几个类型：
(1)由于高层建筑覆盖或过隧道等，GPS信号丢失，造成所提供数据中的时间不连续；
(2)汽车加、减速度异常的数据（普通轿车一般情况下：0至100km/h的加速时间大于7秒，紧急刹车最大减速度在7.5~8 m/s2）；
(3)长期停车（如停车不熄火等候人、停车熄火了但采集设备仍在运行等）所采集的异常数据。
(4)长时间堵车、断断续续低速行驶情况（最高车速小于10km/h）,通常可按怠速情况处理。
(5)一般认为怠速时间超过180秒为异常情况，怠速最长时间可按180秒处理。
请设计合理的方法将上述不良数据进行预处理，并给出各文件数据经处理后的记录数。
2.运动学片段的提取
运动学片段是指汽车从怠速状态开始至下一个怠速状态开始之间的车速区间，如图3所示（基于运动学片段构建汽车行驶工况曲线是日前最常用的方法之一，但并不是必须的
步骤，有些构建汽车行驶工况曲线的方法并不需要进行运动学片段划分和提取）。请设计合理的方法，将上述经处理后的数据划分为多个运动学片段，并给出各数据文件最终
得到的运动学片段数量。

图3 运动学片段的定义
3. 汽车行驶工况的构建
请根据上述经处理后的数据，构建一条能体现参与数据采集汽车行驶特征的汽车行驶工况曲线（1200-1300秒），该曲线的汽车运动特征能代表所采集数据源（经处理后的数据）的相应特征，两者间的误差越小，说明所构建的汽车行驶工况的代表性越好。要求：
（1）科学、有效的构建方法（数学模型或算法，特别鼓励创新方法，如果采用已有的方法，必须注明来源）；
（2）合理的汽车运动特征评估体系（至少包含但不限于以下指标：平均速度（km/h）、平均行驶速度（km/h）、平均加速度（m/）、平均减速度（m/）、怠速时间比（%）、加速时间比（%）、减速时间比（%）、速度标准差（km/h）、加速度标准差（m/）等）；
（3）按照你们所构建的汽车行驶工况及汽车运动特征评估体系，分别计算出汽车行驶工况与该城市所采集数据源（经处理后的数据）的各指标（运动特征）值，并说明你们所构建的汽车行驶工况的合理性。

本人由于精力有限，在闲暇之余只处理了一个文件的数据，而且未能与实际工况图做对照，只提供大部分程序，希望读者们能莫怪。
非常感谢大家的阅读，祝大家阅读愉快，学习进步！
