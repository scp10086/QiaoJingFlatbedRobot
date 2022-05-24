# QiaoJingFlatbedRobot
It's a my FlatbedRobot to carry heavy items. It's cheap and easy to assemble.

The FlatbedRobot is based on modular design and powerd by lithium battery.  

the robot use Brushless DC electric motor.

the robot use electric bike battery. In China, the electric bike battery voltage does not exceed 48v. 

强化学习 比机械臂为例 将动作拆解成基本动作的组合，基本的动作组合成一个动作库，比如你有两个机械臂，协力打开一个铝罐可乐，一个机械臂负责固定可乐，另一个负责拉开可乐的拉环。

每一个基本动作赋予一些属性，每个动作具备一些评价指标，在完成任务的时候，将需要完成的任务拆分成动作组合，这些拆分是否合理则需要通过评价指标来判断。

优化 多个目标

深度学习 带有约束的训练 

或许称之为人工植入知识型强化学习比较好，除开训练的环境外，我们还能人为的给出自己的约束条件以及自己的知识，来让智能体在环境和我们的人为约束条件和知识的情况下开始训练。

能否使用对抗生成网络 一个用于产生动作序列，另一个用于评估这个动作序列是否满足约束，和其他动作序列相比，是否能在多个目标上更优化。

我同时希望生成网络在生成动作序列的时候，就已经知道哪些动作是不行的，而在生成的时候跳过它们，减少生成时间。将好像内置了先验知识了一样。就好像有一个小型的判断网络限制了生成空间了一样。

比如从一个点到达另一个点，我们给出要求和知识，例如，要求走过路程最少，两点之间直线最短，那么即使是未经训练的强化学习网络，也会立刻采取走直线的方式前进。

而评价网络能够在多个目标中，自动判断哪个目标更有效，更应该优先被考虑。

同时在强化学习的环境下，动态调整生成网络内的先验知识，评价网络中的评价标准。

我同时想要动作环境给出的反馈是多维的，带多个标签的，使得智能体能获得更多的信息。

改进网络中的loss函数，现在大部分的loss函数都在最后计算出1个数值来表示损失，我们能否扩展成多个数值，变成一个向量，或者是多个维度呢

## 电线

参考美国标准 AWG， 剥线钳，电线粗细，快速接线端子，接线端子都需要参考这个标准。如果需要计算电机运行时的的电流，锂电池输出电流，也要参考这个标准。
举例，铆钉式接线端子7.62mm间距 最大电流可能是30A，可以容纳10-20awg的电线，而10awg的电线运行电流在40a左右，20awg的电线运行电流在 4a左右。
参考 chrome-extension://efaidnbmnnnibpcajpcglclefindmkaj/http://www.aandt.com.tw/ImgAandT/20180213110305.pdf
## 电池 与 开关电源
考虑到 锂电池的 安全性， 先使用开关电源给电机以及驱动板供电。
开关电源最好选择可以防水的，有外壳的电源，这样的电源自带延申出来的电线，因此需要配一根三角插头的电线，还需要准备快速接线端子，就可以使用了。
如果是那种裸露金属外壳的开关电源，则需要一根三角插头，末端带U形或者叉形的绝缘冷压端子。
后期需要移动的话再购买锂电池。
锂电池 选择 磷酸铁锂电池，品牌选择大牌电动车的电池，比如超威。
电动车锂电池一般在48v，60v，和72v这几个档位，
因此，面对不同的电机，还需要准备48转24v和48转12v的变压器。
如果要更大容量的话，就需要购买宁德时代或者比亚迪生产的给房车使用的磷酸铁锂电池。

# 安装ros2
## 在嵌入式芯片上安装ros2
## 在仿真平台上安装ros2
服务器端命令行安装ros2， windows 远程桌面。
## arduino平台安装ros2
#机械与机器人学习
## 机器人导论学习
## 机械原理学习

# 建模与仿真
## solidworks 建模
## matlab仿真
## Gazebo仿真

# 资源
# 现成的设计方案
https://github.com/hobofan/collected-robotic-arms
# thor 
步进电机 6轴机械臂
http://thor.angel-lm.com/documentation/get-started/
# ar2

# 小型6轴桌面机械臂
https://gitee.com/qzr123/tiny-6arm
# 基于无刷电机的方案
https://hackaday.io/project/180588-cm6-compliant-3d-printed-robotic-arm#j-discussions-title

# 学习资源
https://github.com/mikeroyal/Robotics-guide

# 目标形状
酷炫机械臂
https://www.bilibili.com/video/BV1bJ411B77E/?spm_id_from=333.788.recommend_more_video.11
机器人关节
https://www.bilibili.com/video/BV1XY411A7z1/?spm_id_from=333.788.recommend_more_video.0
