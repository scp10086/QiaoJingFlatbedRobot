# QiaoJingFlatbedRobot
It's a my FlatbedRobot to carry heavy items. It's cheap and easy to assemble.

The FlatbedRobot is based on modular design and powerd by lithium battery.  

the robot use Brushless DC electric motor.

the robot use electric bike battery. In China, the electric bike battery voltage does not exceed 48v. 

强化学习 比机械臂为例 将动作拆解成基本动作的组合，基本的动作组合成一个动作库，比如你有两个机械臂，协力打开一个铝罐可乐，一个机械臂负责固定可乐，另一个负责拉开可乐的拉环。

每一个基本动作赋予一些属性，每个动作具备一些评价指标，在完成任务的时候，将需要完成的任务拆分成动作组合，这些拆分是否合理则需要通过评价指标来判断。

优化 多个目标

深度学习 带有约束的训练 

能否使用对抗生成网络 一个用于产生动作序列，另一个用于评估这个动作序列是否满足约束，和其他动作序列相比，是否能在多个目标上更优化。

我同时希望生成网络在生成动作序列的时候，就已经知道哪些动作是不行的，而在生成的时候跳过它们，减少生成时间。将好像内置了先验知识了一样。就好像有一个小型的判断网络限制了生成空间了一样。

而评价网络能够在多个目标中，自动判断哪个目标更有效，更应该优先被考虑。

同时在强化学习的环境下，动态调整生成网络内的先验知识，评价网络中的评价网络标准。
