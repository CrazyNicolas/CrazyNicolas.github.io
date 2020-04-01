## *TSP Solved By ACS 实验报告*

本次实验使用语言为C/Python.实验平台为Windows10系统.硬件条件为cpu：i5-8250u 内存: 8GB. [代码已开源请点击这里](https://github.com/CrazyNicolas/acs)

如果要使用本实验项目代码,请以**pull request**的形式通知我并附上您的实验项目地址以便于本人扩展项目展示柜！
***
### 第一部分:代码结构
* config.h（跑样例程序不需要修改，如果需要跑其他数据集，请根据[论文](https://github.com/CrazyNicolas/acs/blob/master/acs-ec97.pdf)中具体参数设定细节进行修改）
    > * MAXN TSP问题规模
    > * PATH TSP数据集文件路径
    > * NUM_ANTS 蚁群规模
    > * ALPHA 全局信息素挥发率
    > * RHO Local信息素挥发率(如果对这个概念有疑问建议回看论文)
    > * BETA 信息素和距离相对重要程度
    > * T0 信息素初始水平
    > * Q0 状态转移规则中的概率阈值
* acs.h
    > * **init_ACS**: 蚁群构造函数 加载数据矩阵，加载蚂蚁群体
    > * **del_ACS**: 蚁群析构函数，负责及时free动态分配的内存
    > * **run** : 根据config.h中的超参数的宏定义运行蚁群算法

