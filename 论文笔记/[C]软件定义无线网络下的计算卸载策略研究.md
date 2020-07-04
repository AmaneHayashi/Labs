# 软件定义无线网络下的计算卸载策略研究（*Research on Computation Offloading Strategy in Software Defined Wireless Networks*）

> 单位：北京工业大学 - 北京未来网络科技创新中心
> 
> 作者：李飞翔

> 关键词：*Software Defined Wireless Networks*（软件定义无线网络），*Mobile Edge Computing*（移动边缘计算），*Computation Offloading*（计算卸载），*Stackelberg Game*（斯坦科尔伯格博弈），*Deep Reinforcement Learning*（深度强化学习）

- [软件定义无线网络下的计算卸载策略研究（*Research on Computation Offloading Strategy in Software Defined Wireless Networks*）](#软件定义无线网络下的计算卸载策略研究research-on-computation-offloading-strategy-in-software-defined-wireless-networks)
  - [1 主要贡献](#1-主要贡献)
  - [2 绪论与研究综述](#2-绪论与研究综述)
  - [3 面向低能耗的多控制器部署策略](#3-面向低能耗的多控制器部署策略)
    - [3.1 引言](#31-引言)
    - [3.2 基本模型](#32-基本模型)
      - [3.2.1 网络架构](#321-网络架构)
      - [3.2.2 模型假设](#322-模型假设)
      - [3.2.3 优化问题](#323-优化问题)
    - [3.3 自适应控制器部署算法](#33-自适应控制器部署算法)
      - [3.3.1 确定控制器数量](#331-确定控制器数量)
      - [3.3.2 确定控制器部署位置](#332-确定控制器部署位置)
      - [3.3.3 影响因子$\sigma$的选择](#333-影响因子eqmath-xmlnshttpwwww3org1998mathmathmlsemanticsmrowmiσmimrowannotation-encodingapplicationx-texsigmaannotationsemanticsmathσeq的选择)
    - [3.4 仿真结果](#34-仿真结果)
      - [3.4.1 控制器部署结果](#341-控制器部署结果)
      - [3.4.2 仿真分析](#342-仿真分析)
  - [4 面向低时延的多用户计算卸载服务策略](#4-面向低时延的多用户计算卸载服务策略)
    - [4.1 引言](#41-引言)
    - [4.2 基本模型](#42-基本模型)
      - [4.2.1 通信模型](#421-通信模型)
      - [4.2.2 计算模型](#422-计算模型)
      - [4.2.3 优化问题](#423-优化问题)
    - [4.3 布谷鸟算法](#43-布谷鸟算法)
      - [4.3.1 算法思想](#431-算法思想)
      - [4.3.2 算法规则](#432-算法规则)
      - [4.3.3 相关公式](#433-相关公式)
      - [4.3.4 算法步骤](#434-算法步骤)
      - [4.3.5 算法改进](#435-算法改进)
    - [4.4 仿真结果](#44-仿真结果)
      - [4.4.1 场景参数设置](#441-场景参数设置)
      - [4.4.2 仿真算法](#442-仿真算法)
      - [4.4.3 仿真分析](#443-仿真分析)
  - [5 面向经济效益的多用户计算卸载服务策略](#5-面向经济效益的多用户计算卸载服务策略)
    - [5.1 引言](#51-引言)
    - [5.2 基本模型](#52-基本模型)
      - [5.2.1 通信模型](#521-通信模型)
      - [5.2.2 计算模型](#522-计算模型)
      - [5.2.3 斯坦科尔伯格模型](#523-斯坦科尔伯格模型)
    - [5.3 完全社会交互信息的斯坦科尔伯格模型](#53-完全社会交互信息的斯坦科尔伯格模型)
      - [5.3.1 基本定义](#531-基本定义)
      - [5.3.2 优化问题](#532-优化问题)
      - [5.3.3 纳什均衡](#533-纳什均衡)
      - [5.3.4 动态迭代(梯度下降)算法](#534-动态迭代梯度下降算法)
    - [5.4 不完全社会交互信息的斯坦科尔伯格模型](#54-不完全社会交互信息的斯坦科尔伯格模型)
      - [5.4.1 基本定义](#541-基本定义)
      - [5.4.2 输入度与输出度](#542-输入度与输出度)
      - [5.4.3 效用函数的改变](#543-效用函数的改变)
      - [5.4.4 优化问题](#544-优化问题)
      - [5.4.5 纳什均衡](#545-纳什均衡)
      - [5.4.6 动态迭代(梯度下降)算法](#546-动态迭代梯度下降算法)
    - [5.5 仿真结果](#55-仿真结果)
      - [5.5.1 场景参数设置](#551-场景参数设置)
      - [5.5.2 仿真分析](#552-仿真分析)
  - [6 面向智能化的多用户计算卸载服务策略](#6-面向智能化的多用户计算卸载服务策略)
    - [6.1 引言](#61-引言)
    - [6.2 基本模型](#62-基本模型)
      - [6.2.1 网络架构](#621-网络架构)
      - [6.2.2 通信模型](#622-通信模型)
      - [6.2.3 计算模型](#623-计算模型)
      - [6.2.4 缓存模型](#624-缓存模型)
    - [6.3 深度强化学习算法](#63-深度强化学习算法)
      - [6.3.1 强化学习](#631-强化学习)
      - [6.3.2 *Q*学习](#632-q学习)
      - [6.3.3 深度*Q*学习](#633-深度q学习)
    - [6.4 基于深度强化学习的计算卸载缓存策略](#64-基于深度强化学习的计算卸载缓存策略)
    - [6.5 仿真结果](#65-仿真结果)
      - [6.5.1 场景参数设置](#651-场景参数设置)
      - [6.5.2 仿真分析](#652-仿真分析)

## 1 主要贡献
  - 本文研究了*SDWN*场景下的**计算卸载策略**，为未来*SDWN*场景下实现**经济高效智能的任务卸载服务**提供了可行的解决思路
    - 控制平面：通过**合理部署多控制器**提高整个网络的**全局管理能力**
    - 数据平面：从**低时延、经济效益和智能化**三个方面提供可行的**计算卸载策略**
  - 在*SDWN*场景下，提出了面向**低能耗**的**多控制器部署**策略
    - 单个控制器**自身管控能力有限**，单个控制器一旦发生故障，会造成整个网络的瘫痪
    - 针对**多个控制器难以合理部署**的问题，基于**数据场理论**，提出了**一种自适应的多控制器部署策略**
    - 与粒子群算法等启发式算法相比，该策略可以有效**减小多控制器的平均最小传输功率**，**降低计算时间复杂度**
    - 该策略有效**提高了无线网络全局管理能力**，为计算卸载服务的实现提供了高效决策平台
  - 在*SDWN*场景下，提出了面向**低时延**的**多用户计算卸载**服务策略
    - 大多数无线网络中的基站都在**多信道环境**中工作，因此存在多个用户设备之间如何实现有效的**无线接入协调**以应对计算卸载的挑战
    - 针对计算卸载的**资源受限**的问题，提出了面向**用户设备能耗、传输时延和计算时延多约束下的资源优化分配模型**，以及一种**离散布谷鸟搜索算法**
    - 与其他启发式算法相比，该算法可以**有效缩短任务卸载的平均时延**
  - 在*SDWN*场景下，提出了面向**经济效益**的**多用户计算卸载**服务策略
    - 针对边缘云**合理定价实现利润最大化**的问题，基于**社会信息交互的边缘云与用户设备间效用函数**，提出一种**斯坦科尔伯格博弈模型**，并利用**动态迭代算法**求出最优的**纳什均衡解**
    - 仿真实验表明，该方法在**完全信息和不完全信息**下，可使**总需求值和总效用值**达到近似最优
  - 在*SDWN*场景下，提出了面向**智能化**的**多用户计算卸载服务**策略
    - 边缘服务器难以准确地对具有**不同指标的任务**问题建模，又无法满足边缘卸载任务的**动态变化**
    - 针对边缘服务器的**资源管理**问题，考虑**边缘云的计算、通信和存储资源的环境状态**，提出了一种基于**深度强化学习**的最优决策算法
    - 仿真实验表明，该算法可以**快速收敛**到满意解

## 2 绪论与研究综述

## 3 面向低能耗的多控制器部署策略
### 3.1 引言
  - 本章研究控制器部署(*Controller Placement Problem, CPP*)问题
    - 研究背景
      - 该问题主要包括**控制器数目的确定和多个控制器的部署**
      - 单个*SDWN*控制器控制能力有限，很难及时有效控制网络的全部交换机，为了提高控制层的性能，将**多个*SDWN*控制器**部署到网络中
      - 不同拓扑的有线网络中的控制器部署已得到研究，而*SDWN*中的控制器部署**刚刚起步**
    - 研究内容：
      - 重新构建了*SDWN*多控制器部署问题模型
        - **能耗**是*SDWN*多控制器部署问题应该考虑的一个关键指标
        - 建立数学模型，对多控制器的部署策略进行了评估
      - 提出基于**数据场**的自适应控制器部署算法
        - 根据**数据场方法**，将网络中的节点**划分为不同的子网络**，并针对不同的拓扑**确定控制器的数量**
        - 针对每个子网，采用**穷举法**选择最优的控制器部署位置

### 3.2 基本模型
#### 3.2.1 网络架构
  - 应用层：
    - 功能：负责管理所有业务应用程序，将由程序请求的网络行为**提交给控制器**；抽象和封装自己的功能，向外界提供**北向代理接口**
    - 组成：视频、安全监控等
  - 控制层：
    - 功能：将应用层请求通过处理转换为**基础设施层的流表指令**；为**应用层提供底层网络的抽象模型**
    - 组成：控制逻辑单元、控制平面接口驱动程序
  - 基础设施层：
    - 功能：交换机的功能，执行**数据包的转发**
    - 组成：无线网络基础设施（车辆网络、蜂窝网络、无线传感器网络、*WLAN*等）
  - 接口：
    - 功能：各层之间根据接口进行**通信**
    - 组成：北向接口（**应用层和控制层**之间的通信，如*FML*、*Frantic*）、南向接口（**基础设施层和控制层**之间的通信，如*Openflow*）

![软件定义无线网络架构](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629172932.png)
#### 3.2.2 模型假设
  - 由*Friis*传输程可以得到**最大距离与最小传输功率的关系**，式中$d$为天线之间的距离，$P_r(d)$为距离$d$处接收到的信号功率，$P_t$为传输信号功率，$G_t$为传输天线的增益，$G_r$为接收天线的增益，$\lambda$为接收天线的有效孔径面积的波长
    - 实际使用中，$G_t=15\mathrm{dB}，G_r=2\mathrm{dB}，\lambda=0.33\mathrm{m}，P_t=1\mathrm{W}$
  $$P_r(d)=\frac{P_{t}G_{t}G_{r}\lambda^{2}}{\left(4\pi d\right)^2}\propto\frac{P_t}{d^2}$$
  - 假设**接收信号功率相同**，通过算法找出最小的传输信号功率
#### 3.2.3 优化问题
  - 目标函数：平均传输信号功率
  $$\overline{P}_t(i)=\frac{1}{n}\sum\limits_{i=1}^{n}\frac{P_r(d)\times\left(4\pi d_{\max}\right)^2}{G_{t}G_{r}\lambda^{2}}$$
  - 约束1：每个交换机分配给一个控制器
  $$C_1: \sum\limits_{s\in S,c\in C}x_{sc}=1$$
  - 约束2：分配给每个控制器的交换机数量不超过控制器的处理能力，式中，$L(c)$表示控制器$c$的最大控制能力，$l(s)$表示控制器$c$控制的交换机$s$
  $$C_2: L(c)\ge\sum\limits_{s\in S(c)}l(s),\forall c\in C$$
  - 约束3：交换机与控制器间的距离不超过控制器的覆盖能力，式中，$D_{sc}$表示控制器$c$与交换机$s$的距离，$R_c$表示控制器$c$的覆盖半径
  $$C_3: D_{sc}\le R_c$$
  - 优化目标：**最小化平均传输信号功率**
  $$
  \begin{aligned}
  &\min && \overline{P}_t(i), \\
  &s.t. && C_1 \sim C_3
  \end{aligned}
  $$
  
### 3.3 自适应控制器部署算法
#### 3.3.1 确定控制器数量
  - 数据场理论：描述整个空间中每个**数据点之间相互作用**的理论，包括场强、势函数、等势线等
    - 势函数：假设数据对象$O$在给定空间$\Omega$中，空间中任意点$x$会产生势值$\varphi(x)$，那么势值$\varphi(x)$应满足
      - $\varphi(x)$是空间$\Omega$中定义的**连续、光滑、有限**函数
      - $\varphi(x)$是数据对象$O$与点$x$之间**距离的单调递减**函数。当距离为$0$时，$\varphi(x)$达到最大值；当距离趋于无穷大时，$\varphi(x)\rightarrow 0$
    - 典型数据场：
      - 远程场：**拟核力场**，在远程距离上表现良好
      - 近程场：**拟重力场**，在近程距离上表现良好
      - **我们可以使用场函数分析数据的关系，从而进行聚类，本文使用拟核力场**
    - 拟核力场：数据空间$\Omega$中，数据对象$x_i$产生具有质量$m_i$的虚拟场，对于空间$\Omega$中的点$x=\left(x_1,x_2,\cdots,x_n\right)^\mathrm{T}$，其势函数与场强定义如下式。式中，$\Vert{x-x_i}\Vert$表示数据对象$x_i$与数据点$x$的距离，$m_{i}(m_{i}\ge{0},\sum_{i=1}^{n}m_{i}=1)$为数据对象$x_i$的质量（表示$x_i$的数据场的强度），$\sigma\in\left(0,+\infty\right)$为影响因子，$k\in{N}$为距离指标
      - 实际参数选择中，$k=2$
    $$
    \begin{aligned}
    &\varphi(x)=\sum\limits_{i=1}^{n}\varphi_i(x)=\sum\limits_{i=1}^{n}\left(m_{i}\times e^{-\Vert{x-x_i}\Vert^k/\sigma}\right) \\
    &F(x)=\sum\limits_{i=1}^{n}\left((x_i-x)\times m_i\times e^{-\Vert{x-x_i}\Vert^k/\sigma}\right)
    \end{aligned}
    $$
  - 算法步骤：
    - 借助拟核力场计算每个数据点的势能与场强，得到等势线，**同一个等势线的点形成子网**
    - 如果出现了离群点，**将该点与最近子网结合**，形成新的子网
#### 3.3.2 确定控制器部署位置
  - 算法步骤（穷举法）：
    - 对每个子网络，计算每个节点平均传输信号功率
    - 选择平均传输功率**最小值**作为控制器部署的位置
    - 若控制器的控制能力不足（$即L(x_j^*<\sum{S_j})或R(x_j^*)<D_{x_j^*,S}$），则**调整参数$\sigma$**，将子网重新分簇成多个子网，直至每个子网都满足控制器的能力
  - 复杂度分析：对于$N$个节点，$M$个控制器
    - 直接寻找：需要寻找$C_N^M$次，时间复杂度为$O(N^M)$
    - 自适应算法：假设$N=N_1+N_2+\cdots+N_M$，则需要寻找$N_1\times{(N_1-1)}+N_2\times{(N_2-1)}+\cdots+N_M\times{(N_M-1)}$次，时间复杂度为$O(N^2)$
    - 当控制器个数超过$2$时，可以**显著降低时间复杂度**
#### 3.3.3 影响因子$\sigma$的选择
  - $\sigma$过小时，数据对象之间没有交互；$\sigma$过大时，数据对象变为一个簇
![不同$\sigma$值下的势场分布](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629195108.png)
  - 势熵（势值分布熵）：衡量数据对象的势值的**不确定性**
    - 数据对象势值越相近，势熵越大，**最小势熵对应最优的$\sigma$**
    - 对空间$\Omega$中的$n$个数据对象$x=\left\{x_1,x_2,\cdots,x_n\right\}$，每个数据对象的势值分别为$\varphi_1,\varphi_2,\cdots,\varphi_n$，则势熵为$H$，式中$Z=-\sum\limits_{i=1}^{n}\varphi_i$为标准化因子
    $$H=-\sum\limits_{i=1}^{n}\frac{\varphi_i}{Z}\log\left(\frac{\varphi_i}{Z}\right)$$
    - 势熵的性质
    $$0\le{H}\le{\log(n)},\ \ H=\log(n)\Leftrightarrow\varphi_1=\varphi_2=\cdots=\varphi_n$$
  - 黄金分割算法：
    - 算法步骤：给定目标函数$\min f(x)$，初始区间$[a,b]$
      - 确定初始空间最小值$a_1=a$，最大值$b_1=b$，精确度$\epsilon>0$，迭代次数$k=1$
      $$
      \begin{aligned}
      &\lambda_1=a_1+\left(1-\frac{\sqrt{5}-1}{2}\right)(b_1-a_1) \\
      &\mu_1=a_1+\left(\frac{\sqrt{5}-1}{2}\right)(b_1-a_1)
      \end{aligned}
      $$
      - 若$(b_k-a_k)\lt\epsilon$，迭代结束，否则
        - 若$f(\lambda_k)\ge f(\mu_k)$，则
          $$
          \begin{aligned}
          &a_{k+1}=\lambda_k，b_{k+1}=b_k \\
          &\lambda_{k+1}=\mu_k，\mu_{k+1}=a_{k+1}+\left(\frac{\sqrt{5}-1}{2}\right)\left(b_{k+1}-a_{k+1}\right)
          \end{aligned}
          $$
        - 若$f(\lambda_k)\lt f(\mu_k)$，则
          $$
          \begin{aligned}
          &a_{k+1}=\lambda_k，b_{k+1}=\mu_k \\
          &\lambda_{k+1}=a_{k+1}+\left(1-\frac{\sqrt{5}-1}{2}\right)\left(b_{k+1}-a_{k+1}\right)，\mu_{k+1}=\lambda_k
          \end{aligned}
          $$
        - 设置$k=k+1$
    - 实际求解时，设置$8$轮迭代，初始空间为$[0,1]$，精度要求$\epsilon=0.1$，最终得到$\sigma=0.146$
![黄金分割法的具体过程](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629195219.png)

### 3.4 仿真结果
#### 3.4.1 控制器部署结果
![不同网络拓扑的控制器部署结果](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629195509.png)

#### 3.4.2 仿真分析
  - 对比算法（三种算法的粒子数为$20$，每个算法运行$50$代）
    - 粒子群算法（$c_1(社会影响)=0.1，c_2(个体影响)=2.0，w(速度权重，0.9\rightarrow 0.4)$）
    - 遗传算法（$P_c(交叉概率)=0.8，P_m(突变概率)=0.1)$）
    - 贪婪算法
  - 仿真结果
    - 不同网络拓扑下的平均最小传输功率
      - 相同的控制器数目条件下，*ACPA*算法>粒子群算法>遗传算法（收敛快）>贪婪算法（局部最优）
      - **较少的节点数目和更多的控制器数目需要更少的最小传输功率**
    - 不同网络拓扑下的计算时间
      - *ACPA*算法能够达到较低的平均延迟
      - 贪婪算法的性能受不同网络拓扑结构的影响比较大
    - **结论：*ACPA*算法可以很好地平衡最小传输功率和延迟**
![不同网络拓扑下的平均最小传输功率与计算时间](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629200136.png)

## 4 面向低时延的多用户计算卸载服务策略
### 4.1 引言
  - 本章研究的计算卸载问题基于**软件定义网络的工业物联网**体系架构
    - 控制平面和基础设施平面进行**分离**，即*SDWN*控制器与分布式小蜂窝基站和宏蜂窝基站分离
    - *SDWN*控制器可以从**用户设备和蜂窝基站**收集信息，并从全局的角度感知网络状态，为计算卸载任务作出合理决策
    - 根据*SDWN*控制器的决策指令，用户设备选择将任务卸载到**小蜂窝基站边缘云或宏蜂窝基站边缘云**中
  - 将计算卸载问题建模为一个**混合整数非线性规划**问题
    - 优化目标：**满足能耗约束下最大限度减少全部用户设备的延迟**
    - 算法：布谷鸟搜索算法

### 4.2 基本模型
#### 4.2.1 通信模型
  - 一个宏蜂窝基站+多个小蜂窝基站($m \in \mathbb M$)+若干工业物联网设备($n \in \mathbb N$)
  - 每个设备最多连接**一种**基站卸载任务

![基于软件定义网络的工业物联网体系架构](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629200252.png)
  - 对设备$m$，其任务为$J_m$
  $$J_m=\{A_m(数据大小),B_m(工作量),T_m^{\rm max \it }(截止期限)\}$$
  - 卸载模式$\mathbb X = \{x_m\},m=1,2,,...,M$，$x_m=0$为卸载到宏蜂窝基站，$x_m=n$为卸载到小蜂窝基站$n$
  $$F(x_m,i)=\begin{cases}1, &if\ x_m=i \cr 0, &otherwise\end{cases}$$
  - 数据传输速率为$r_{mn}$，式中$n=0$表示宏蜂窝基站，$w_{mn}$为信道带宽，$\rho_{mn}$为传输功率，$h_{mn}$为信道增益，$k_{jn} \in \{0,1\}$为干扰系数
  $$r_{mn}=w_{mn}\log_2 \left( 1+\frac{\rho_{mn}|h_{mn}|^2}{\sigma ^2+\sum\limits_{j=1,j \ne m}^{M} k_{jn}\rho_n |h_{jn}|^2}  \right)$$
![计算卸载模式](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629200317.png)

#### 4.2.2 计算模型
  - 执行时延为$T_{mn}$，式中$C_{mn}$为边缘云的计算能力
  $$
  \begin{aligned}
  & T_{mn}=T_{mn}^{f}(传输时延)+T_{mn}^{c}(计算时延)+T_{mn}^{q}(排队时延) \\
  & T_{mn}^{f}=\frac{A_m}{r_{mn}},\ T_{mn}^{c}=\frac{B_m}{C_{mn}},\ T_{mn}^{q}=\sum\limits_{m=1}^{M}T_{mn}^{f} F \left\{ x_m=n \right\}
  \end{aligned}
  $$
  - 计算能耗为$E_{mn}$，式中$\eta_{mn}$为能效系数
  $$E_{mn}=\eta_{mn}C_{mn}^{3}T_{mn}^{c}$$

#### 4.2.3 优化问题
  - 目标函数：所有用户设备的时延
  $$E(w)=\sum\limits_{m=1}^{M}\sum\limits_{n=1}^{N}\left( T_{m0}F\left\{ x_m=0 \right\}+T_{mn}F\left\{ x_m=n \right\} \right)$$
  - 约束1：通信资源约束
  $$C_1: \sum\limits_{m=1}^{M}w_{mn}F\left\{ x_m=n \right\} \le w_{\max}^{BS}$$
  - 约束2：计算资源约束
  $$C_2: \sum\limits_{m=1}^{M}A_{m}F\left\{ x_m=n \right\} \le C_{\max}^{BS}$$
  - 约束3：能耗约束
  $$C_3: \sum\limits_{m=1}^{M}E_{mn}F\left\{ x_m=n \right\} \le E_{\max}^{BS}$$
  - 优化目标：**减少全部用户设备的延迟**
  $$
  \begin{aligned}
  &\min && E(w), \\
  &s.t. && C_1 \sim C_3
  \end{aligned}
  $$

### 4.3 布谷鸟算法
#### 4.3.1 算法思想
  - 基于布谷鸟的巢寄生行为以及鸟类的*Levy*飞行行为
  - 每个巢中的卵代表**一个解**，布谷鸟的卵代表**新解**，目标是**利用新解或者潜在的优解替代巢中的劣解**
#### 4.3.2 算法规则
  - 每只布谷鸟每次随机选择**一个巢**，并产生**一个卵**
  - 具有**最高质量卵的巢**保留至下一代
  - 可寄主巢的数量$n$是固定的，且寄主以概率为$p_a \in (0,1)$发现布谷鸟放的卵，在这种情况下，寄主鸟将布谷鸟的卵**扔掉或者丢弃现有的巢**
#### 4.3.3 相关公式
  - *Levy*飞行：**方向选择**（随机，均匀选择）+**步长选择**（小概率大跨步+大概率小跨步）。记第$i$个点第$t$时刻的位置为$x_i^t$，则：
    $$
    \begin{aligned}
    & x_i^{t+1}=x_i^t+\alpha L(s,\lambda) \\
    & 式中，L(s,\lambda)=\frac{\lambda \Gamma(\lambda)\sin(\pi\lambda /2)}{\pi}\cdot \frac{1}{s^{1+\lambda}}
    \end{aligned}
    $$
    - $\alpha$为步长缩放因子，一般选择$\alpha=O(L/10)$
    - $s$为步长，其可以借助*Mantegna*算法生成：
    $$
    \begin{aligned}
    & s=\frac{U}{|V|^{\frac{1}{\lambda}}}, \ U \sim N(0,\sigma ^2),\ V \sim N(0,1) \\ 
    & 式中，\sigma ^2=\left[ \frac{\Gamma (1+\lambda)}{\lambda \Gamma ((1+\lambda)/2)} \cdot \frac{\sin(\pi \lambda /2)}{2^{\left( \lambda -1 \right)/2}} \right]^{\frac{1}{\lambda}},
    \Gamma(z)=\int_{0}^{\infty} \frac{t^{z-1}}{e^t}dt
    \end{aligned}$$
    - $\lambda$的取值一般在$(1,2)$之间
  - 局部随机移动：只适用于局部，容易**陷入局部最优解**。记第$i$个点第$t$时刻的位置为$x_i^t$，则：
    $$
    \begin{aligned}
    & x_i^{t+1}=x_i^t+\alpha s\otimes H\left( p_a-\epsilon \right) \otimes (x_j^t-x_k^t) \\
    & 式中，H(x)=\begin{cases}1, &if\ x\gt 1 \cr 0, &otherwise\end{cases}
    \end{aligned}$$
    - $\alpha$为步长缩放因子，可以选择与$Levy$相同的$\alpha$
    - $s$为步长，此时选择服从$(0,1)$均匀分布
    - $p_a$为淘汰概率，一般选择为$0.25$
    - $x_j^t,x_k^t$为时刻$t$任意选取的两个点，$\otimes$为点乘
#### 4.3.4 算法步骤
  - 初始化鸟窝个数$n$，鸟窝位置$p_0=\left[ x_1^{(0)},x_2^{(0)},...,x_n^{(0)} \right]^{\mathrm{T}}$，最佳鸟窝$x_i^{(0)}$与最优解$f_{\mathrm{min}}$
  - 循环下列步骤直至找到最优解或迭代次数达到上限：
    - 位置更新：保留上代**最优鸟窝**$x_i^{t-1}$，其它鸟窝依据*Levy*飞行公式，更新其位置，产生一组新鸟窝$p_{t-1}=\left[ x_{1}^{t-1},x_{2}^{t-1},x_{n}^{t-1} \right]^{\mathrm{T}}$，用**适应值更好的鸟窝代替原鸟窝**(如果不如原鸟窝则不替代)，得到一组较优的鸟窝$g_i=\left[ x_1^{(t)},x_2^{(t)},...,x_n^{(t)} \right]^{\mathrm{T}}$
    - 存安去险：每个鸟蛋被鸟窝主人发现外来鸟蛋的概率为$r$，其中$r \in \left[ 0,1 \right]$服从均匀分布，若$r \lt p_a$，则用**局部随机步行公式更改鸟窝位置**，将得到的新鸟窝的适应值再次对比，得到一组较优的鸟窝$p_i=\left[ x_1^{(t)},x_2^{(t)},...,x_n^{(t)} \right]^{\mathrm{T}}$
    - 输出最优鸟窝位置$x_{b}^{(t)}$和最优值$f_{\mathrm{min}}$
#### 4.3.5 算法改进
  - 布谷鸟算法解空间为连续，本优化问题的解空间为$\{0,1\}$
    - 将值映射至$(0,1)$范围内：
    $$D(x_i^{t+1})=\frac{x_i^{t+1}-x^{\mathrm{min}}}{x^{\mathrm{min}}-x^{\mathrm{max}}}$$
    - **离散化处理**（一般地，$D_{th}=0.5$）：
    $$x_i^{t+1}=\begin{cases}1, &if\ D(x_i^{t+1})>D_{th} \cr 0, &otherwise\end{cases}$$

### 4.4 仿真结果
#### 4.4.1 场景参数设置
  - 网络参数：
    - 宏蜂窝基站边缘云：$1$个，传输半径$\rm 500m$
    - 小蜂窝基站边缘云：$10$个，最多服务$50$个设备
  - 信道参数：
    - 设备到宏蜂窝的信道带宽：$\rm 5MHz$
    - 设备到小蜂窝的信道带宽：$\rm 180KHz$
    - 传输功率：$\rm [50mW,100mW]$均匀分布
    - 高斯噪声功率$\sigma^2$：$\rm -100dBM$，干扰因子：$\rm -100dBM$
    - 信道增益：$h=d^{-\lambda}$，式中$\lambda=4$为路径损失因子
  - 任务参数：
    - 任务数据大小：$\rm [10M,20M]$均匀分布
    - 任务工作量：$\rm [3,10]$个CPU均匀分布
    - 任务截止期限：$\rm [0.05s,3s]$均匀分布
  - 云服务器参数：
    - 计算能力：$\rm 5GHz$
    - 单元能耗：$\rm 4J/GHz$

![工业物联网示例](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629200427.png)

#### 4.4.2 仿真算法
  - 布谷鸟算法
   - $P_a$：淘汰概率，默认为$0.25$
   - $\alpha$：步长缩放因子，默认为$1$
  - 粒子群算法
   - $c_1$：个体影响因子，值为$2$
   - $c_2$：社会影响因子，值为$2$
   - $w$：上一代速度的权重，值从$0.9$线性递减至$0.4$
  - 遗传算法
   - $P_c$：交叉概率，值为$0.8$
   - $P_m$：变异概率，值为$0.1$
#### 4.4.3 仿真分析
  - 不同数目的物联网设备之间的平均时延变化
   - 布谷鸟>粒子群>遗传算法
   - 设备越多，时延越大

![不同物联网设备个数下的平均时延变化](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629201801.png)
  - 不同的布谷鸟参数$P_a$与$\alpha$下的平均时延变化
   - $P_a$增加，平均时延先下降再上升，最优解$P_a=0.25$
   - $\alpha$增加，平均时延持续下降

![不同布谷鸟算法参数下的平均时延变化](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629201859.png)
  - 不同的任务参数$(A,B,T)$下平均时延变化
   - $A/B/T$越小，平均时延越小

![不同任务参数下的平均时延变化](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629201929.png)

## 5 面向经济效益的多用户计算卸载服务策略
### 5.1 引言
  - 工业物联网中，边缘云之间与物联网设备之间都在**相互竞争**
    - 物联网设备之间存在竞争关系，倾向于**以更好的服务质量和更低的支付费用访问边缘云**
    - 边缘云之间存在竞争关系，为了吸引更多的客户需要**设置适当的价格最大化他们的利润**
  - 将边缘云与设备之间的交互看作一个**斯坦科尔伯格博弈问题**
    - 边缘云表示**领导者**，工业物联网设备表示**追随者**
    - 在构建工业物联网设备的效用函数模型中，引入了**社会交互信息**
    - 在完全的社会交互信息的情况下，设计了基于斯坦科尔伯格博弈的计算卸载策略
    - 在不完全的社会交互信息的情况下，设计了基于贝叶斯斯坦科尔伯格博弈的计算卸载策略

### 5.2 基本模型
#### 5.2.1 通信模型
  - 与第四章相同，不考虑宏蜂窝基站边缘云与小蜂窝基站边缘云的差别，统一看作边缘云集合
  - 对设备$m$，其任务为$J_m$
  $$J_m=\{Q_m(数据大小),B_m(工作量),T_m^{\rm max \it }(截止期限)\}$$
![工业物联网架构](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629202119.png)
#### 5.2.2 计算模型
  - 执行时延为$T_{mn}$，式中$C_{mn}$为边缘云的计算能力
  $$
  \begin{aligned}
  & T_{mn}=T_{mn}^{f}(传输时延)+T_{mn}^{c}(计算时延)+T_{mn}^{q}(排队时延) \\
  & T_{mn}^{f}=\frac{Q_m}{r_{mn}},\ T_{mn}^{c}=\frac{B_m}{C_{mn}},\ T_{mn}^{q}=\sum\limits_{m=1}^{M}T_{mn}^{f} F \left\{ x_m=n \right\}
  \end{aligned}$$
  - 能耗为$E_{mn}$，式中$\eta_{mn}$为能效系数，$\rho_{mn}$为传输功率，
  $$
  \begin{aligned}
  & E_{mn}=E_n^C(计算能耗)+E_{mn}^T(传输能耗) \\
  & E_n^C=\eta_{n}T_{mn}^{c}, \ E_{mn}^T=\rho_{mn}T_{mn}^f
  \end{aligned}
  $$
#### 5.2.3 斯坦科尔伯格模型
  - 边缘云与设备的交互分为两阶段
    - **边缘云根据设备反馈设置计算其资源最佳价格**
    - **设备根据边缘云价格确定所需最佳计算资源量**
![工业物联网中基于斯坦科尔伯格的计算卸载策略](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629202148.png)
  - 模型由**服务提供者、消费者、效用函数、行动策略**组成
    - 服务提供者：边缘云
    - 消费者：设备
    - 行动策略：计算需求集合$\mathcal{Q}=\{Q_1,Q_2,...Q_M\}$，计算服务定价集合$\mathcal{P}=\{P_1,P_2,...P_N\}$
    - 效用函数：
      - 设备$m$的效用函数$F_m\left(P_n,Q_m,Q_{-m}\right)$：$U_m$为设备满意度，$a$为设备的满意系数，$Q_m$为设备申请的计算需求量，$\varphi_{mj} \in \{0,1\}$表示设备$m$从设备$j$获得的影响系数，且$\varphi_{mj}=\varphi_{jm}$，$D_m$为设备的支付开销，$\zeta$为能耗的系数因子。
      $$
      \begin{aligned}
      & F_m\left(P_n,Q_m,Q_{-m}\right)=U_m(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j)-D_m-\zeta E_{mn}^T \\
      & 式中，U_m=a\ln(1+Q_m)，D_m=P_nQ_m
      \end{aligned}$$
      - 边缘云$n$的效用函数$G_n(P_n,Q_m)$：$\xi$为能耗的系数因子。
      $$G_n(P_n,Q_m)=\sum\limits_{m=1}^{M}(P_nQ_m-\xi E_n^C)$$

### 5.3 完全社会交互信息的斯坦科尔伯格模型
#### 5.3.1 基本定义
  - 所有工业物联网设备都**愿意向其它设备报告自己的私有信息**，并从社交网络中获取正确的信息
  - 边缘云的定价不仅要依赖**工业物联网设备的反馈**，还要依赖**其他边缘云的动作**
#### 5.3.2 优化问题
  - 边缘云$n$的定价
  $$
  \begin{aligned}
  &\max && G_n(P_n|P_{-n}^*,Q^*)\\
  &\ s.t.&& Q^* \in \left[ \underline{Q},\overline{Q} \right],\\
  &\ && P_n^* \in \left[ \underline{P},\overline{P} \right]
  \end{aligned}
  $$
  - 设备$m$的计算资源需求
  $$
  \begin{aligned}
  &\max && F_m(Q_m|P_{n}^*,Q_{-m}) \\
  &\ s.t. && T_{mn} \le T_m^{max} \\
  &\ && Q_m \in \left[\underline{Q},\overline{Q}\right],\\
  &\ && P_n^* \in \left[ \underline{P},\overline{P} \right]
  \end{aligned}$$
  - 式中 $P_{-n}$为除去边缘云$n$之外的其它边缘云的定价集合，$Q_{-m}$为除去设备$m$之外的其它设备的计算资源需求策略集合，$\left[ \underline{P},\overline{P} \right]$为价格集合的上下限，$\left[ \underline{Q},\overline{Q} \right]$为设备计算资源需求的上下限
#### 5.3.3 纳什均衡
  - 纳什均衡点的定义：记$P_n^*$为最优价格，$Q_m^*$为最优计算需求量，则
  $$
  \begin{aligned}
  & (P_n^*,Q_m^*)为纳什均衡点 \Leftrightarrow \\
  & F_m\left(P_n^*,Q_m^*,Q_{-m}^*\right) \ge F_m\left(P_n^*,Q_m,Q_{-m}^*\right),\ G_n(P_n^*,Q_m^*) \ge G_n(P_n,Q_m^*)
  \end{aligned}$$
  - 纳什均衡点的求解：
    - 设备具有唯一的纳什均衡点
      $$ 
      \begin{aligned}
      &F_m\left(P_n,Q_m,Q_{-m}\right)&&= U_m(1+\sum\limits_{j=1}^{M}\varphi_{mj}    U_j)-D_m-\zeta E_{mn}^T \\
      &\ &&=a\ln(1+Q_m)\left(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j\right)-P_nQ_m-\zeta\rho_{mn}\frac{Q_m}{r_{mn}}\\
      &\frac{\partial(F_m\left(P_n,Q_m,Q_{-m}\right))}{\partial Q_m}&&= \frac{a}{1+Q_m}\left(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j\right)-P_n-\frac{\zeta \rho_{mn}}{r_{mn}}\\
      &\frac{\partial^2(F_m\left(P_n,Q_m,Q_{-m}\right))}{\partial Q_m^2}&&= -\frac{a}{(1+Q_m)^2}\left(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j\right) \lt 0 \Rightarrow F_m\left(P_n,Q_m,Q_{-m}\right)为凹函数\\
      &令\frac{\partial(F_m\left(P_n,Q_m,Q_{-m}\right))}{\partial Q_m}=0，解得&&Q_m^*=\psi=\left( \frac{ar_{mn}\left(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j\right)}{r_{mn}P_{n}+\zeta \rho_{mn}}-1\right)\\
      &结合资源需求的上下限限制，得到&&Q_m^*=\begin{cases}\underline{Q}, &if\ \psi\lt\underline{Q} \cr \psi, &if\ \underline{Q}\lt\psi\lt\overline{Q} \cr \overline{Q}, &if\ \psi\gt\overline{Q}\end{cases}&&
      \end{aligned}
      $$
    - 边缘云具有唯一的纳什均衡点
      $$ 
      \begin{aligned}
      &G_n(P_n,Q_m^*)&&=\sum\limits_{m=1}^{M}(P_nQ_m^*-\xi E_n^C) \\
      &\ &&=P_n\sum\limits_{m=1}^{M}\left(\frac{ar_{mn}\left(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j\right)}{r_{mn}P_{n}+\zeta \rho_{mn}}-1\right)-\xi\sum\limits_{m=1}^{M}\eta_n\frac{B_m}{C_{mn}}\\
      &\frac{\partial(G_n(P_n,Q_m^*))}{\partial P_n}&&= \sum\limits_{m=1}^{M}\left( \frac{ar_{mn}\zeta\rho_{mn}(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_{j})}{\left(r_{mn}P_n+\xi\rho_{mn}\right)^2}-1\right)\\
      &\frac{\partial^2(G_n(P_n,Q_m^*))}{\partial P_n^2}&&= \frac{-2ar_{mn}^2\zeta\rho_{mn}}{\left(P_nr_{mn}+\zeta\rho_{mn}\right)^3}(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_{j}) \lt 0 \Rightarrow G_n(P_n,Q_m^*)为凹函数\\
      &令\frac{\partial(G_n(P_n,Q_m^*))}{\partial P_n}=0，解得&&P_n^*=\phi=\sum\limits_{m=1}^{M}\frac{1}{r_{mn}}\left(\sqrt{ar\zeta\rho_{mn}\left(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j\right)}-\zeta\rho_{mn}\right)\\
      &结合价格集合的上下限限制，得到&&P_n^*=\begin{cases}\underline{P}, &if\ \phi\lt\underline{P} \cr \phi, &if\ \underline{P}\lt\phi\lt\overline{P} \cr \overline{P}, &if\ \phi\gt\overline{P}\end{cases}&&
      \end{aligned}
      $$
#### 5.3.4 动态迭代(梯度下降)算法
  - 算法步骤
    - 初始化边缘云定价$P_n$与设备计算资源需求$Q_m$
    - 当$t \lt t_{\max}$时循环：
      - 更新边缘云$n$的定价：
      $$P_n(t+1)=P_n(t)+\alpha\frac{\partial G_n}{\partial P_n}$$
      - 当$\tau \lt \tau_{\max}$时循环：
        - 更新边缘云$n$的定价：
        $$Q_m(\tau+1)=Q_m(\tau)+\beta\frac{\partial F_m}{\partial Q_m}$$
    - 输出$P_n^*$与$Q_m^*$
  - 算法分析
    - $t_{\max},\tau_{\max}$为边缘云与设备的最大迭代次数，$alpha,\beta$为步长
    - 时间复杂度为$O(N^{t_{\max}} \times M^{\tau_{\max}})$

### 5.4 不完全社会交互信息的斯坦科尔伯格模型
#### 5.4.1 基本定义
  - 在没有全局管理的情况下，工业物联网设备由于自身的自私行为而**无法从对方获取个人信息**
  - 工业物联网设备的**分布信息可以通过历史信息或机器学习方法来计算**，利用**贝叶斯分析**来获得预期的社会互动信息
  - 记社会系数$\epsilon\gt 0$，表示社会交互信息的期望
#### 5.4.2 输入度与输出度
  - 度集合$\mathcal{K}={1,2,...,K}$
  - 输入度$l \in \mathcal{K}$：设备被$l$个其它设备影响，其边际概率分布记为$I:\mathcal{K} \rightarrow [0,1]$
  - 输出度$k \in \mathcal{K}$：设备能影响$k$个其它设备，其边际概率分布记为$H:\mathcal{K} \rightarrow [0,1]$
  - 一致性理论证明了**设备的平均输出度等于平均输入度**，式中$\hat{k}$为社会交互信息的平均水平，即：
  $$\sum\limits_{k=1}^{K}kH(k)=\sum\limits_{l=1}^{K}lI(l)=\hat{k}$$
  - 输出度为$k$的设备$m$的平均影响力为$Ave(U_{-m})$，建模如下：
  $$Ave(U_{-m})=\sum\limits_l^{k}\overline{I}(l)\left(\sum\limits_k^{K}H(k)a\ln(1+Q(k,l))\right)$$
#### 5.4.3 效用函数的改变
  - 设备$m$的效用函数$F_m'\left(P_n,Q_m,Q_{-m}\right)$：
  $$
  \begin{aligned}
    F_m'\left(P_n,Q_m,Q_{-m}\right)&= E(F_m\left(P_n,Q_m,Q_{-m}\right)) \\
    &=E\left(U_m(1+\sum\limits_{j=1}^{M}\varphi_{mj}U_j)-D_m-\zeta E_{mn}^T\right)\\
    &=U_m(1+\epsilon E\sum\limits_{j=1}^{M}U_j)-D_m-\zeta E_{mn}^T \\
    &=U_m(1+\epsilon kAve(U_{-m}))-D_m-\zeta E_{mn}^{C}\\
  \end{aligned}$$
  - 边缘云$n$的效用函数$G_n(P_n,Q_m)$：$\xi$为能耗的系数因子。
  $$
  \begin{aligned}
  G_n'(P_n,Q_m)&= E(G_n(P_n,Q_m)) \\
  &=E\left(\sum\limits_{m=1}^{M}(P_nQ_m-\xi E_n^C)\right) \\
  &=E\left(\sum\limits_{m=1}^{M}P_nQ_m\right)-\xi E_n^C \\
  &=\sum\limits_l^K\left(\sum\limits_k^{K}I(l)H(k)\left(P(k,l)\times Q(k,l)-\xi E_n^C\right)\right)
  \end{aligned}$$
#### 5.4.4 优化问题
  - 边缘云$n$的定价
  $$
  \begin{aligned}
  &\max && G_n'(P_n|P_{-n}^*,Q^*)\\
  &\ s.t.&& Q^* \in \left[ \underline{Q},\overline{Q} \right],\\
  &\ && P_n^* \in \left[ \underline{P},\overline{P} \right]
  \end{aligned}
  $$
  - 设备$m$的计算资源需求
  $$
  \begin{aligned}
  &\max && F_m'(Q_m|P_{n}^*,Q_{-m}) \\
  &\ s.t. && T_{mn} \le T_m^{max} \\
  &\ && Q_m \in \left[\underline{Q},\overline{Q}\right],\\
  &\ && P_n^* \in \left[ \underline{P},\overline{P} \right]
  \end{aligned}$$
#### 5.4.5 纳什均衡
  - 纳什均衡点的定义：与先前形式相同
  - 纳什均衡点的求解：
    - 设备具有唯一的纳什均衡点
      $$ 
      \begin{aligned}
      &F_m'\left(P_n,Q_m,Q_{-m}\right)&&=U_m(1+\epsilon kAve(U_{-m}))-D_m-\zeta E_{mn}^T \\
      &\ &&=a\ln(1+Q_m)(1+\epsilon kAve(U_{-m}))-P_nQ_m-\zeta \rho_{mn}\frac{Q_m}{r_{mn}} \\
      &\frac{\partial(F_m'\left(P_n,Q_m,Q_{-m}\right))}{\partial Q_m}&&= \frac{a}{1+Q_m}\left(1+\epsilon kAve(U_{-m})\right)-P_n-\frac{\zeta \rho_{mn}}{r_{mn}}\\
      &\frac{\partial^2(F_m\left(P_n,Q_m,Q_{-m}\right))}{\partial Q_m^2}&&= -\frac{a}{(1+Q_m)^2}(1+\epsilon kAve(U_{-m})) \lt 0 \Rightarrow F_m'\left(P_n,Q_m,Q_{-m}\right)为凹函数\\
      &令\frac{\partial(F_m'\left(P_n,Q_m,Q_{-m}\right))}{\partial Q_m}=0，解得&&Q_m^*=\frac{a(2-A)}{P_n+\frac{\zeta\rho_{mn}}{r_{mn}}}-1\\
      &式中，&&A=a\epsilon k\times\omega\left(-\ln(a\epsilon k)-\left(a\epsilon k\left(\ln\left(\frac{\rho_{mn}+P_nr_{mn}}{r_{mn}}+\ln(a)\right)-1\right)/(a\epsilon k)\right)\right)\\
      &\omega(\cdot)表示方程Y+\log(Y)=X的解
      \end{aligned}
      $$
    - 边缘云具有唯一的纳什均衡点
      $$ 
      \begin{aligned}
      &G_n'(P_n,Q_m^*)&&=E\left(\sum\limits_{m=1}^{M}P_nQ_m^*\right)-\xi E_n^C \\
      &\ &&=P(k,l)\times\left(\frac{a(2-A)}{P_n+\frac{\zeta\rho_{mn}}{r_{mn}}}-1\right)-\xi\eta_n\frac{B_m}{C_m}\\
      &令\frac{\partial(G_n'(P_n,Q_m^*))}{\partial P_n}=0，解得&&P_n^*=a(2-A)-\frac{\zeta\rho_{mn}}{r_{mn}}\\
      \end{aligned}
      $$
#### 5.4.6 动态迭代(梯度下降)算法
  - 算法步骤
    - 初始化边缘云定价$P_n$与设备计算资源需求$Q_m$
    - 当$t \lt t_{\max}$时：
      - 更新边缘云$n$的定价：
      $$P_n(t+1)=P_n(t)+\alpha\frac{\partial G_n'}{\partial P_n}$$
      - 当$\tau \lt \tau_{\max}$时：
        - 更新边缘云$n$的定价：
        $$Q_m(\tau+1)=Q_m(\tau)+\beta\frac{\partial F_m'}{\partial Q_m}$$
    - 输出$P_n^*$与$Q_m^*$
  - 算法分析
    - $t_{\max},\tau_{\max}$为边缘云与设备的最大迭代次数，$alpha,\beta$为步长
    - 时间复杂度为$O(N^{t_{\max}} \times M^{\tau_{\max}})$

### 5.5 仿真结果
#### 5.5.1 场景参数设置
  - 信道参数：
    - 设备到宏蜂窝的信道带宽：$\rm 10MHz$
    - 设备到小蜂窝的信道带宽：$\rm 1MHz$
    - 传输功率：$\rm [50mW,100mW]$均匀分布
    - 高斯噪声功率$\sigma^2$：$\rm -100dBM$，干扰因子：$\rm -100dBM$
  - 任务参数：
    - 任务工作量：$\rm [3,10]$个CPU均匀分布
    - 任务截止期限：$\rm [0.05s,3s]$均匀分布
  - 云服务器参数：
    - 宏蜂窝基站边缘云计算能力：$\rm 5GHz$
    - 宏蜂窝基站边缘云单元能耗：$\rm 4J/GHz$
    - 小蜂窝基站边缘云计算能力：$\rm 4GHz$
    - 小蜂窝基站边缘云单元能耗：$\rm 3J/GHz$
  - 迭代次数：$200$次
#### 5.5.2 仿真分析
  - 完全交互下的仿真
    - 不同设备数量下设备的总需求值$Q$和总效用值$F$变化
      - 随着迭代次数的增加，总需求值和总效用值迅速增加，收敛后保持稳定
      - **设备的数量越多，设备的总需求值和总效用值就越高**
    - 不同设备数量下边缘云(宏，微)的价格$P$与效用值$G$变化
      - 价格随着迭代次数的增加，快速增长$\rightarrow$保持不变$\rightarrow$持续增加（设备数较多时）
      - **设备增加使得边缘云具有更高的效用值**
![完全交互下的仿真](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629202651.png)
  - 不完全交互下的仿真
    - 不同设备数量下设备的总需求值$Q$和总效用值$F$变化
      - 随着迭代次数的增加，总需求值保持稳定，总效用值先上升后稳定
      - 设备的数量越多，设备的总需求值越高，**总效用值先升后降**（$f_{10}<f_{30}<f_{20}$）
    - 不同设备数量下边缘云(宏，微)的价格$P$与效用值$G$变化
      - 价格随着迭代次数的增加，持续增长
      - 小蜂窝基站边缘云的效用值略高于宏蜂窝基站边缘云的效用值
![不完全交互下的仿真](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629203429.png)
  - 算法对比（遗传算法、贪婪算法）
      - 本文提出的算法提供了**最好的效用值**
![不同算法对比的仿真](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629203805.png)

## 6 面向智能化的多用户计算卸载服务策略 
### 6.1 引言
  - 移动边缘计算中的计算卸载问题通常被建模为混合整数规划问题，但是在边缘云系统中建模往往比较**复杂**
    - 卸载到边缘计算系统的**任务具有不同的特性、延迟要求、计算要求和能耗等**，要准确地模拟这个问题是不可能的
    - 在线任务是动态变化的，这就要求边缘云做出**适当的在线决策**
    - 问题很大程度上**依赖于模型**，凸优化方法、博弈论和启发式算法**不适合在高度变化的场景中做出实时卸载决策**
  - 本章讨论在超密集网络中，考虑计算卸载中的通信资源、计算资源和缓存资源的框架，采用**深度强化学习方法**来帮助管理任务卸载
    - 将边缘云表示为**服务提供者**，用户设备表示为**请求者**。借助*SDWN*控制器全局管控网络，为用户设备计算卸载服务的做出合理决策
    - 提出了基于深度*Q*学习算法的计算卸载策略。该策略**将卸载决策和缓存决策建模为动作行为**，在具有高维行为空间的大型网络中具有计算可行性和高效性
    - 仿真实验表明，该算法可以**快速收敛**到满意解

### 6.2 基本模型
#### 6.2.1 网络架构
  - 包括宏蜂窝基站、小蜂窝基站、用户设备
    - 宏蜂窝基站和小蜂窝基站分别与边缘服务器连接，称为宏蜂窝基站边缘云和小蜂窝基站边缘云
    - 虽然宏蜂窝基站边缘云与用户设备的距离更远，但它可以提供比小蜂窝基站边缘云**更强大的计算能力和更大的接入带宽**
    - 相比之下，小蜂窝基站边缘云更接近用户设备，可以提供**更快的计算服务**。用户设备能够选择不同的卸载计算方案，即选择宏蜂窝基站边缘云或小蜂窝基站边缘云卸载任务
![超密集蜂窝网络](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629203844.png)
  - 用户设备与边缘云之间的计算卸载服务包括三个步骤
    - 选择用户设备中的**任务卸载**到小蜂窝基站边缘云或基站边缘云
    - 边缘云选择卸载任务的**执行决策**。如果任务尚未**缓存**在边缘云中，则将计算该任务。否则，将直接返回**缓存的结果**
    - 边缘云将**执行的结果返回**给用户设备
![超密集蜂窝网络中的计算卸载和缓存策略](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629203857.png)

#### 6.2.2 通信模型
  - 与第四章相同，$n=0$表示宏蜂窝基站边缘云，否则表示小蜂窝基站边缘云
  - 对设备$m$，其任务为$J_m$
  $$J_m=\{A_m(计算前数据大小),A_m'(计算后数据大小),B_m(工作量),T_m^{\rm max \it }(截止期限)\}$$
  - 通信收益$R_{mn}^{comm}$，式中$\alpha_{mn}$为终端用户的接入费用，$r_{mn}$为传输速率，$\beta_{mn}$为频谱的使用费用，$w_{mn}$为信道带宽
  $$R_{mn}^{comm}=\alpha_{mn}r_{mn}-\beta_{mn}w_{mn}$$
  
#### 6.2.3 计算模型
  - 计算时延为$T_{mn}^{C}$，式中$C_{mn}$为边缘云的计算能力
  $$T_{mn}^{C}=\frac{B_m}{C_{mn}}$$
  - 计算速率为$q_{mn}$
  $$q_{mn}=\frac{A_mC_{mn}}{B_m}$$
  - 计算能耗为$e_{mn}$，式中$\varpi_{mn}$为边缘云单位时间内消耗的能耗速率
  $$e_{mn}=\varpi_{mn}T_{mn}^{C}$$
  - 计算收益$R_{mn}^{comp}$，式中$\phi_{mn}$为用户支付的计算费用，$\varphi_{mn}$为边缘云支付的计算费用
  $$R_{mn}^{comp}=\phi_{mn}q_{mn}-\varphi_{mn}e_{mn}$$
#### 6.2.4 缓存模型
  - 每个边缘云缓存$D$个文件，内容是否缓存在边缘云中由**二进制数值**决定
  - 内容流行度$\mathcal{G}=\left\{g_1,g_2,\cdots,g_D\right\}$服从*Zipf*分布，$D$表示内容文件的类型数，每个用户设备以概率$g_d$请求内容文件$d$，参数$\epsilon$范围在$\mathrm{[0.5,1.5]}$之间
  $$g_d=\frac{1/d^{\epsilon}}{\sum\limits_{d=1}^{D}1/d^{\epsilon}}$$
  - 节省带宽$l_{A'_m}$，式中$T_{A' m}$为下载缓存内容$A'_m$的持续时间
  $$l_{A'_m}=\frac{g_{A'_m}A'_m}{T_{A' m}}$$
  - 缓存收益$R_{mn}^{cache}$，式中$\psi_{mn}$为内容文件缓存在边缘云的存储费用，$\gamma_{mn}$为边缘云支付的回传成本
  $$R_{mn}^{cache}=\psi_{mn}l_{A'_m}-\gamma_{mn}A'_{m}$$
### 6.3 深度强化学习算法
#### 6.3.1 强化学习
  - 是解决现实问题的一种**无先验知识**的有效方法
  - 不同于一般的有监督学习和无监督学习，它模拟了**智能体与环境的交互作用**
  - 用于解决一个**多步骤的决策**问题
  - 包括**实验状态、行为、回报函数和状态转换概率**四个部分
  - **智能体**从**环境**中获取**状态**并采取**行动**，环境将**收益**回报给智能体
  - 不需要从经验样本中学习，**从尝试的行为中获得反馈**
#### 6.3.2 *Q*学习
  - *Q*学习算法是强化学习中一种应用广泛的算法
  - *Q*学习算法的决策过程基于*MDP*，它可以用五元组来表示，式中，$s_i$为状态空间，$a_i$为动作空间，$P\left(s_i,a_i,s_{i+1}\right)$为系统在状态$s_i$下通过执行动作$a_i$转移到状态$s_{i+1}$的概率，$R\left(s_i,a_i\right)$为系统在状态$s_i$下选择动作$a_i$的立即回报，$Q(s_i,a_i)$为系统在状态$s_i$下选择动作$a_i$的长期回报
  $$\left\{s_i,a_i,P\left(s_i,a_i,s_{i+1}\right),R(s_i,a_i),Q(s_i,a_i)\right\}$$
  - 系统在状态$s_i$下，基于策略$\pi$的长期收益为$V^{\pi}(s_i)$。$\lambda(0<\lambda<1)$为**折扣因子**，评估**历史回报对未来的影响**。$\lambda$越大，训练出的智能体越注重历史经验，否则越注重即时回报
  $$V^{\pi}(s_i)=R_i+\lambda R_{i+1}+\lambda^{2}R_{i+2}+\cdots$$
  - *Q*值是状态和动作的评估
  $$Q(s_i,a_i)=R_i+\lambda V^{\pi}(s_{i+1})$$
  - *Q*值基于下式进行更新，式中$\eta(0<\eta<1)$为学习率
  $$Q_{i+1}(s_i,a_i)=(1-\eta)Q_i(s_i,a_i)+\eta\left[R_i+\lambda \max Q_i(s_{i+1},a_{i+1})\right]$$
#### 6.3.3 深度*Q*学习
  - 利用**前馈人工神经网络**来逼近*Q*值函数，通过**最小化损失函数更新$\theta(神经网络的权值)$训练**
  - 网络输入层是状态$s$，输出层是*Q*值，目标函数$y(s,a,s';\hat{\theta})=R+\lambda\max Q(s',a';\hat{\theta})$根据参数$\hat{\theta}$的变化而更新
  $$L(\theta)=E\left[\left(y(s,a,s';\hat{\theta})-Q(s,a;\theta)\right)^2\right]$$
### 6.4 基于深度强化学习的计算卸载缓存策略
  - 状态空间：不同的动作$a_m^{comm}(t),a_m^{cache}(t)$决定了不同的系统状态，系统状态包括用户设备$m$与边缘云$n$的通信、边缘云的缓存$d$
![基于深度强化学习的计算卸载和缓存策略](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629203914.png)
  - 动作空间：由**通信动作与缓存动作**组成，$a_m(t)=\left\{a_m^{comm}(t),a_m^{cache}(t)\right\}$
    - 通信动作$a_m^{comm}(t)=\left[a_{m,1}^{comm}(t),a_{m,2}^{comm}(t),\cdots,a_{m,n}^{comm}(t)\right]$：$a_{m,i}^{comm}(t),i \in \left\{1,2,\cdots,N\right\}$表示在时刻$t$用户设备$m$是否连接到小蜂窝边缘云$i$，取值为$\{0,1\}$，若所有取值均为$0$，代表连接到宏蜂窝边缘云
    - 缓存动作$a_m^{cache}(t)=\left[a_{m,1}^{cache}(t),a_{m,2}^{cache}(t),\cdots,a_{m,n}^{cache}(t)\right]$：$a_{m,j}^{cache}(t),j \in \left\{1,2,\cdots,N\right\}$表示在时刻$t$用户设备$m$的内容文件是否缓存在边缘云$j$，取值为$\{0,1\}$，若所有取值均为$0$，代表缓存在宏蜂窝边缘云
  - 回报函数：最大化通信模型、计算模型、缓存模型的回报值，$R_m(t)=R_{m}^{comm}(t)+R_{m}^{cache}(t)$
    - 通信回报$R_{m}^{comm}(t)$：边缘云中**通信模型所获得的回报值**，
    $$R_m^{comm}(t)=\underbrace{\left(1-a_{m}^{comm}(t)\right)R_{m0}^{comm}}_{宏蜂窝基站边缘云的通信回报}\ \ +\underbrace{\left(a_{m}^{comm}(t)\right)R_{mn}^{comm}}_{小蜂窝基站边缘云的通信回报}$$
    - 缓存回报$R_{m}^{cache}(t)$：内容文件**缓存在边缘云中所获得的回报值**
    $$R_m^{cache}(t)=\underbrace{\left(1-a_{m}^{comm}(t)\right)\left(1-a_{m}^{cache}(t)\right)R_{m0}^{cache}}_{宏蜂窝基站边缘云的缓存回报}\ \ +\underbrace{\left(1-a_{m}^{comm}(t)\right)a_{m}^{cache}(t)R_{m0}^{comp}}_{宏蜂窝基站边缘云的计算回报}\ \\ +\underbrace{a_{m}^{comm}(t)a_{m}^{cache}(t)R_{mn}^{cache}}_{小蜂窝基站边缘云的缓存回报}\ \ +\underbrace{a_{m}^{comm}(t)\left(1-a_{m}^{cache}(t)\right)R_{mn}^{comp}}_{小蜂窝基站边缘云的计算回报}$$
### 6.5 仿真结果
#### 6.5.1 场景参数设置
  - 网络参数（与第四章相同）：
    - 宏蜂窝基站边缘云：$1$个
    - 小蜂窝基站边缘云：$10$个
  - 信道参数：
    - 设备到宏蜂窝的信道带宽：$\rm 10MHz$
    - 设备到小蜂窝的信道带宽：$\rm 1MHz$
    - 传输功率：$\rm [50mW,100mW]$均匀分布
    - 高斯噪声功率$\sigma^2$：$\rm -100dBM$，干扰因子：$\rm -100dBM$
    - 信道增益：$h=d^{-\chi}$，式中$\chi=4$为路径损失因子
  - 费用参数：
    费用类型|宏蜂窝|小蜂窝
    :---:|:---:|:---:
    用户设备的接入费用|$\rm 3\ units/bps$|$\rm 1\ units/bps$
    用户设备的计算费用|$\rm 0.8\ units/J$|$\rm 0.4\ units/J$
    用户设备的存储费用|$\rm 20\ units/byte$|$\rm 10\ units/byte$
    边缘云的传输成本|$\rm 3\times 10^{-4}\ units/Hz$|$\rm 1\times 10^{-4}\ units/Hz$
    边缘云的计算成本|$\rm 0.2\ units/J$|$\rm 0.1\ units/J$
    边缘云的回传成本|$\rm 0.2\ units/bps$|$\rm 0.1\ units/bps$
  - 神经网络参数：
    - 网络结构：一个输入层+两个隐藏层(第一层$120$个神经元，第二层$80$个神经元)+一个输出层
    - 训练参数：训练批大小(*batch_size*)为$128$，训练间隔(*epoch*)为$10$
    - 优化器：*Adam*优化器，学习率$0.005$，内存$1024$
![实验仿真场景](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629203928.png)
#### 6.5.2 仿真分析
  - $\rm UE=20$时的回报函数值和学习率的变化
    - 回报函数值在前$400$次迭代时逐渐增加，收敛后保持稳定
    - 训练损失在前$100$次迭代时迅速减少，然后保持不变
    - 算法可以实现收敛，损失值可以降低到$\rm 20%$左右
![回报函数值与训练损失值变化](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629204101.png)
  - 不同设备数量下的回报函数值变化
    - 设备数量越多，回报函数值越高，
    - 收敛速度：$v_{10}>v_{5}>v_{20}$

![不同设备数量下的回报函数值变化](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629204109.png)
  - 不同的强化学习重要参数（学习率、批量大小和训练间隔）对仿真结果的影响
    - 学习率为$0.01$，批量大小为$32$，训练间隔为$10$时，回报函数值最好

![三个重要参数（学习率、批量大小和训练间隔）对仿真结果的影响](https://cdn.jsdelivr.net/gh/AmaneHayashi/PictureBed/20200629204121.png)