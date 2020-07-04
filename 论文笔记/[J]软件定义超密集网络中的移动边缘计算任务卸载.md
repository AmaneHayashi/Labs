# 软件定义超密集网络中的移动边缘计算任务卸载（*Task Offloading for Mobile Edge Computing in Software Defined Ultra-Dense Network*）

> 单位：*Huazhong University of Science and Technology(HUST)*
> 
> 作者：*Min Chen*, *Yixue Hao*

> 关键词：*Software defined networking*（软件定义网络），*Mobile edge computing*（移动边缘计算），*Task offloading*（任务卸载），*Resource allocation*（资源分配）

- [软件定义超密集网络中的移动边缘计算任务卸载（*Task Offloading for Mobile Edge Computing in Software Defined Ultra-Dense Network*）](#软件定义超密集网络中的移动边缘计算任务卸载task-offloading-for-mobile-edge-computing-in-software-defined-ultra-dense-network)
  - [1 摘要](#1-摘要)
  - [2 绪论与文献综述](#2-绪论与文献综述)
    - [2.1 选题背景](#21-选题背景)
    - [2.2 研究现状与挑战](#22-研究现状与挑战)
    - [2.3 研究思路](#23-研究思路)
    - [2.4 研究内容](#24-研究内容)
    - [2.5 文献综述](#25-文献综述)
  - [3 系统模型与问题描述](#3-系统模型与问题描述)
    - [3.1 *SD-UDN*架构](#31-sd-udn架构)
    - [3.2 网络模型](#32-网络模型)
    - [3.3 通信模型](#33-通信模型)
    - [3.4 任务卸载模型](#34-任务卸载模型)
    - [3.5 问题描述](#35-问题描述)
  - [4 高效的任务卸载方案](#4-高效的任务卸载方案)
    - [4.1 计算资源分配子问题](#41-计算资源分配子问题)
    - [4.2 任务放置问题](#42-任务放置问题)
  - [5 模型评估](#5-模型评估)
    - [5.1 参数设置](#51-参数设置)
    - [5.2 算法对比](#52-算法对比)
    - [5.3 计算量/数据大小对卸载性能的影响](#53-计算量数据大小对卸载性能的影响)
  - [6 结论](#6-结论)

## 1 摘要
  - 选题背景：
    - 越来越多的计算密集型和数据密集型任务对延迟敏感
    - *UDN*中的*MEC*将是满足低延迟需求的有效解决方案
    - **边缘云中的计算资源为分布式**，且**移动设备电量可变**，使得边缘云为用户分担计算任务变得充满挑战
  - 本文内容：
    - 利用*SDN*的思想，研究*UDN*的任务卸载
    - 将任务卸载（*Mixed Integer Non-linear Problem, NP-hard*）问题转换为两个子问题
      - **任务的放置**
      - **资源的分配**
    - 对比：
      - 本文提出的方案
      - 随机任务卸载或统一任务卸载
    - 结论：与对比的任务卸载方案相比，该方案可以减少$20％$的任务时延，节省$30％$的能耗

## 2 绪论与文献综述
### 2.1 选题背景
  - 移动设备数量与移动流量爆炸增长，*UE*中的应用将需要广泛的算力和持久的数据处理能力
  - 新兴应用开发受到了*UE*的计算能力与电池寿命的限制，必须由通信网络提供高级的计算卸载与通信架构为应用程序提供支持
### 2.2 研究现状与挑战
  - 现状
    - 移动边缘计算因为**低时延、高性能**，能更好执行时延敏感/计算密集型任务
    - 超密集网络通过小蜂窝*BS*的密集部署，提供巨大**接入能力**
    - 大多数超密集网络和移动边缘计算的工作是**分开**的，在超密集网络中尚没有针对移动边缘计算的**任务卸载**工作
  - 挑战
    - 如何在*UDN*中控制边缘云分散的计算资源
    - 如何根据移动设备的剩余电量和网络状态进行任务卸载
  - 新思路
    - *SDN*可以在分布式网络节点和移动设备上实现**逻辑上的集中控制**
    - 引入*SDN*技术，实现**控制平面和数据平面的分离**
### 2.3 研究思路
  - 将主要的计算和控制功能从分布式小蜂窝*BS*中分离出来，统一到位于宏蜂窝的集中式*SD-UDN*控制器中
  - *SD-UDN*控制器可以收集移动设备和边缘云的信息，决策移动设备在本地执行任务或将其中的一部分卸载到边缘云中进行处理
### 2.4 研究内容
  - 为*SD-UDN*中的移动边缘计算提出了一种创新的任务卸载框架
    - 在宏小区BS处部署控制器，可以获得关于移动设备，基站，边缘云和任务的**全局信息**
  - 提出了一种有效的软件定义任务卸载（*SDTO*）方案
    - 将任务卸载方案表述为**混合整数非线性规划问题**，证明其为*NP-hard*问题
    - 将任务卸载方案分为两个部分
      - 应该在哪里处理任务（**任务放置**）$\Rightarrow$凸优化问题
      - 确定应为每个任务分配多少边缘云计算资源（**资源分配**）$\Rightarrow$$0-1$规划问题
  - 进行了广泛的实验，以评估*SDTO*方案的性能
      - 任务执行时间减少$20％$，能耗降低$30％$
### 2.5 文献综述
  - 移动云计算因为减少任务执行时间、减少设备能耗广泛应用，但通过蜂窝网络将任务卸载到云将产生很大**延迟**
  - 移动边缘计算应运而生，研究任务卸载与资源分配，但大多数工作考虑**单个***MEC*服务器，考虑多服务器的*MEC*未考虑到*UDN*
  - 本文设计用于*UDN*中*MEC*的*SDN*任务卸载，并提出有效的任务卸载方案

## 3 系统模型与问题描述
### 3.1 *SD-UDN*架构
  - 架构组成
    - 用户平面：需要卸载计算任务的用户
       - 通过无线链路连接到微小区*BS*或宏小区*BS*
    - 数据平面：微小区*BS*和部署在微小区*BS*附近的边缘云
       - 小型小区*BS*通过高速前传网络连接到中央宏小区*BS*
       - 通过**空中接口分离**，将宏小区*BS*的**控制**覆盖范围与微小区*BS*的**数据**覆盖范围分离
    - 控制平面：部署在宏小区*BS*上的*SD-UDN*控制器
      - **收集**移动用户和宏小区*BS*内的微小区*BS*的**信息**，并优化网络配置
      - 维护移动设备信息表，*BS*信息表和任务信息表
        - 移动设备信息表：剩余电池容量和移动设备的CPU周期
        - *BS*信息表：无线电接入负载，边缘云的计算负载
        - 任务信息表：任务类型，任务数据量和任务计算量
      - 用户定期将测量信息发送到最近的服务*BS*。然后，*BS*将多个用户的信息和边缘云信息集成在一起，并定期发送到*SD-UDN*控制器
  - 工作流程
    - 移动设备选择最近的*BS*进行任务请求
    - *BS*将相应的任务请求发送到*SD-UDN*控制器
    - *SD-UDN*控制器更新所有信息表，**根据任务的延迟和能耗，给出移动设备的任务卸载策略和边缘云的资源分配策略**
### 3.2 网络模型
  - *SD-UDN*共有$n$个基站，每个基站有**一个**边缘云，边缘云集合为$B=\{b_1,b_2,\cdots,b_n\}$
  - 每个移动设备有**一个**任务，移动设备集合为$U=\{u_1,u_2,\cdots,u_m\}$
  - 每个任务由二元组$Q_i=(\omega_i,s_i)$构成，$\omega_i$为计算量（*CPU*周期数），$s_i$为数据大小
  - 向用户$u_i$提供服务的*BS*集合记为$\mathcal{A}(u_i)$

### 3.3 通信模型
  - 链路速率：对于用户$u_i$，基站$b_j$，上行链路速率为$r_{i,j}$，式中$B$为信道带宽，$p_i$为用户的传输功率，$h_{i,j}$为信道增益，$\sigma^2$为噪声功率，$I_{i,j}$小区干扰功率
  $$r_{i,j}=B\log_2\left(1+\frac{p_{i}h_{i,j}}{\sigma^2+I_{i,j}}\right)$$
  - 传输时延：对于用户$u_i$，基站$b_j$，传输时延为$t_{i,j}^{T}$，式中$s_i$为数据大小
  $$t_{i,j}^{T}=\frac{s_i}{r_{i,j}}$$
  - 传输能耗：对于用户$u_i$，基站$b_j$，传输能耗为$\epsilon_{i,j}^{E}$，式中$p_i$为用户的传输功率
  $$\epsilon_{i,j}^{E}=p_{i}t_{i,j}^{T}=\frac{p_{i}s_{i}}{r_{i,j}}$$

### 3.4 任务卸载模型
  - 本地执行：
    - 执行时延：对于用户$u_i$，执行时延为$t_i^L$，式中$f_i^l$为用户设备的*CPU*运算能力，$\omega_i$为计算量（*CPU*周期数）
    $$t_i^L=\frac{\omega_i}{f_i^l}$$
    - 执行能耗：对于用户$u_i$，执行时延为$\epsilon_i^L$，式中$\rho_{i}$为每个*CPU*周期消耗的能量的功率系数
    $$\epsilon_i^L=\rho_{i}\omega_i$$
  - 任务卸载执行：
    - 执行时延：由卸载时延与处理时延组成（回传时延可忽略），对于用户$u_i$，执行时延为$t_i^E$，式中$\gamma_i\in\mathcal{A}(u_i)$为用户卸载的边缘云，$\kappa_i^{\gamma_i}$为任务卸载到边缘云的比例，边缘云的*CPU*运算能力由集合$f^c=\{f_1^c,f_2^c,\cdots,f_n^c\}$决定
    $$t_i^E=\frac{\omega_i}{\kappa_i^{\gamma_i}f_{\gamma_i}^{c}}+\frac{s_i}{r_{i,\gamma_{i}}}$$ 

### 3.5 问题描述
  - 问题组成：**任务放置+资源分配**
  - 决策变量：
    - $x_i$（$0-1$决策变量，任务$i$在本地/边缘侧处理，由集合$\mathrm{X}=\{x_1,x_2,\cdots,x_m\}$指定）
    - $\gamma_i$（处理任务$i$的边缘云，由集合$\gamma=\{\gamma_1,\gamma_2,\cdots,\gamma_m\}$指定）
    - $\kappa_i$（为任务$i$分配的计算资源比例，由集合$\kappa=\{\kappa_1,\kappa_2,\cdots,\kappa_m\}$指定）
  - 目标函数：所有用户设备的平均处理时延
  $$
  \begin{aligned}
  &E(\mathbf{x,\gamma,\kappa})=\sum\limits_{i=1}^{m}\left[x_{i}t_{i}^{L}+\left(1-x_i\right)t_i^E\right] \cr 
  &式中，t_{i}^{L}=\frac{\omega_i}{f_i^l}，t_i^E=\frac{\omega_i}{\kappa_i^{\gamma_i}f_{\gamma_i}^{c}}+\frac{s_i}{r_{i,\gamma_i}}
  \end{aligned}
  $$
  - 约束1：本地能耗小于移动设备的电量
  $$C_1: x_{i}\epsilon_{i}^{L}\le \alpha_{i}E_{\max}^{i},\forall i=1,\cdots,m$$
  - 约束2：计算卸载能耗小于移动设备的电量
  $$C_2: (1-x_{i})\epsilon_{i}^{E}\le \alpha_{i}E_{\max}^{i},\forall i=1,\cdots,m$$
  - 约束3：只有向用户$u_i$提供服务的边缘云能提供计算卸载
  $$C_3: \gamma_{i}\in A(u_i),\forall i=1,\cdots,m$$
  - 约束4：分配给$\gamma_i$的计算量不超过其计算资源，式中$o_{\gamma_i}$为放置在边缘云$\gamma_i$上的任务集合
  $$C_4: \sum\limits_{i\in o_{\gamma_i}}\kappa_{i}^{\gamma_i}\le 1$$
  - 优化目标：**最小化全部用户设备的平均处理时延**（*NP-hard*问题）
  $$
  \begin{aligned}
  &\min && E(\mathbf{x,\gamma,\kappa}), \cr
  &s.t. && C_1 \sim C_4
  \end{aligned}
  $$


## 4 高效的任务卸载方案
$$f(\mathbf{x,\gamma,\kappa})=\sum\limits_{i=1}^{m}\left[x_{i}\frac{\omega_i}{f_i^l}+\left(1-x_i\right)\left(\frac{\omega_i}{\kappa_i^{\gamma_i}f_{\gamma_i}^{c}}+\frac{s_i}{r_{i,\gamma_i}}\right)\right]$$
### 4.1 计算资源分配子问题
  - 化为关于$\kappa$的凸优化问题
    - 化简函数形式：记$\lambda=(\mathbf{x},\gamma)$，对于给定的$\lambda=\lambda^0\in\mathbb{H}$，此时$x_i=0$，假设分配给用户$i$的边缘云为$j$，总共有$l$个用户选择卸载到边缘云，则函数可化为下式，此时优化问题的约束只有$C_4$
    $$f(\kappa,\gamma^0)=\sum\limits_{i=1}^{l}\left(\frac{\omega_i}{\kappa_i^{j}f_{j}^{c}}+\frac{s_i}{r_{i,j}}\right)$$
    - 证明*Hessian*矩阵正定：此时函数$f(\kappa,\gamma^0)$为$\kappa=\{\kappa_1,\kappa_2,\cdots,\kappa_l\}$的函数，则其*Hessian*矩阵如下式，可以看出*Hessian*矩阵为对角矩阵，所有特征值均为正数，故*Hessian*矩阵正定，故原问题为关于$\kappa_i$的凸优化问题
    $$A=
    \begin{bmatrix}
    \frac{\partial^2{f}}{\partial^2{\kappa_1}} & \frac{\partial^2{f}}{\partial{\kappa_1}\partial{\kappa_2}} & \cdots & \frac{\partial^2{f}}{\partial{\kappa_1}\partial{\kappa_l}}\cr
    \frac{\partial^2{f}}{\partial{\kappa_2}\partial{\kappa_1}} & \frac{\partial^2{f}}{\partial^2{\kappa_2}} & \cdots & \frac{\partial^2{f}}{\partial{\kappa_2}\partial{\kappa_l}} \cr
    \vdots & \vdots & \ddots & \vdots \cr
    \frac{\partial^2{f}}{\partial{\kappa_l}\partial{\kappa_1}} & \frac{\partial^2{f}}{\partial{\kappa_l}\partial{\kappa_2}} & \cdots & \frac{\partial^2{f}}{\partial^2{\kappa_l}}
    \end{bmatrix} 
    ，式中\frac{{\partial^2{f}}}{\partial{\kappa_i}\partial{\kappa_j}}=
    \begin{cases}
    \frac{2\omega_i}{\left(\kappa_i^j\right)^3f_j^c}, &if\ i=j \cr 
    0, &otherwise
    \end{cases}
    $$
  - 利用*KKT*条件求解
    - 将原优化函数写成*Lagrange*函数
    $$L(\kappa,\nu)=f(\kappa,\gamma^0)+\sum\limits_{j}\nu_j\left(\sum\limits_{i\in o_j}\kappa_i^j-1\right)$$
    - 利用*KKT*条件求出$\kappa$的值
    $$
    \begin{aligned}
    & \begin{cases}
    \nabla f\left(\tilde{\kappa}_1^j,\tilde{\kappa}_2^j,\cdots,\tilde{\kappa}_n^j\right)+\sum\limits_{j}\nu_j\nabla\left(\sum\limits_{i\in o_j}\tilde{\kappa}_i^j-1\right)=0 \cr 
    \sum\limits_{i\in o_j}\tilde{\kappa}_i^j-1=0
    \end{cases} \cr
    & 解得\kappa_i^*=\frac{\sqrt{\omega_i}}{\sum_{i\in o_j}\sqrt{\omega_i}}
    \end{aligned}
    $$
    - 将求出的$\kappa$代入原优化函数，得出优化函数的最优值
    $$
    \begin{aligned}
    & f(\kappa^*,\gamma^0)&& =\sum\limits_{i=1}^{l}\left(\frac{\omega_i}{\kappa_i^{*}f_{j}^{c}}+\frac{s_i}{r_{i,j}}\right) \cr
    & && =\sum\limits_{i=1}^{l}\left(\frac{\sqrt{\omega_i}\sum_{i\in o_j}\sqrt{\omega_i}}{f_{j}^{c}}+\frac{s_i}{r_{i,j}}\right) \cr
    & && =\sum\limits_{j=1}^{n}\sum\limits_{i\in o_j}\left(\frac{\sqrt{\omega_i}\sum_{i\in o_j}\sqrt{\omega_i}}{f_{j}^{c}}+\frac{s_i}{r_{i,j}}\right) \cr
    & && =\sum\limits_{j=1}^{n}\left(\frac{\left(\sum_{i\in o_j}\sqrt{\omega_i}\right)^2}{f_{j}^{c}}+\sum\limits_{i\in o_j}\frac{s_i}{r_{i,j}}\right) 
    \end{aligned}
    $$
### 4.2 任务放置问题
  - 将原问题转换为单变量的$0-1$整数规划问题
    - 改写优化变量：定义$\mathbf{Z}=(z_{ij})_{m\times(n+m)},z_{ij}\in\{0,1\}$替代$x$与$\gamma$，当$z_{ij}=1$时，任务$i$被卸载到边缘云（$j\le n$）或本地执行（$j=i+n$）
    - 改写表达式：将优化问题写出下述形式，此时该问题为单变量$0-1$整数规划问题，为*NP-hard*问题
    $$
    \begin{aligned}
    &\min\limits_{\mathbf{Z}} && {\Vert(W\mathbf{ZC})^T\Vert}_2^2+S\mathbf{ZR}, \cr
    &\ s.t. && x_{ij}\in\{0,1\} \cr
    & && \sum\limits_{j=1}^{n+1}z_{ij}=1,i=1,2,\cdots,m\cr
    & 式中，&&W=\left(\sqrt{\omega_1},\sqrt{\omega_2},\cdots,\sqrt{\omega_m}\right)\cr
    & && S=\left(s_1,s_2,\cdots,s_m\right)\cr
    & && P=\left(p_1,p_2,\cdots,p_m\right)\cr
    & && \mathbf{C}=
    \begin{bmatrix}
    \frac{1}{\sqrt{f_1^c}} & 0 & \cdots & 0 & 0 \cr
    0 & \frac{1}{\sqrt{f_2^c}} & \cdots & 0 & 0 \cr
    \vdots & \vdots & \ddots & \vdots & \vdots \cr
    0 & 0 & \cdots & \frac{1}{\sqrt{f_{m-1}^l}} & 0 \cr
    0 & 0 & \cdots & 0 & \frac{1}{\sqrt{f_m^l}}
    \end{bmatrix} \cr
    & && \mathbf{R}=
    \begin{bmatrix}
    r_{11} & \cdots & r_{1n} & 0 & \cdots & 0 \cr
    r_{11} & \cdots & r_{1n} & 0 & \cdots & 0 \cr
    \vdots & \ddots & \vdots & \vdots & \ddots & \vdots \cr
    r_{m1} & \cdots & r_{mn} & 0 & \cdots & 0
    \end{bmatrix}
    _{m\times{(n+m)}}
    \end{aligned}
    $$
  - 连续函数近似求解
    - 定义连续变量$y_{ij}$，其满足$y_{ij}\ge 0,\sum\limits_{j=1}^{n+1}y_{ij}=1,i=1,2,\cdots,m$
    - 线性函数$\phi^t(y_{ij})=\frac{y_{ij}}{y_{ij}^{t-1}+\epsilon}$，式中$t$为迭代次数，用$\phi^t(y_{ij})$替代$\mathbf{Z}$，则优化问题变为凸问题，可用*KKT*条件求解
    - 迭代算法求解：
      - 初始状态下，$y_{ij}^0=1-\epsilon$
      - $t=t+1$，将上一步求解出的$y_{ij}$记做$y_{ij}^{t-1}$，求解$\phi^t(y_{ij})$
      - 用$\phi^t(y_{ij})$替换$\mathbf{Z}$，依据*KKT*条件求解出$y_{ij}$
      - 如果$\vert{y_{ij}^t-y_{ij}^{t-1}}\vert\lt\delta$，则$y_{ij}^*=y_{ij}^t$，否则继续迭代
    - 收敛性分析
      - 当$\vert{y_{ij}^t-y_{ij}^{t-1}}\vert\lt\delta$时，有
      $$y_{ij}^t=\arg\min\limits_{y_{ij}}f(\frac{y_{ij}}{y_{ij}^{t-1}+\delta})$$
      - 此时，$y_{ij}^{t-1}\approx y_{ij}^t=y_{ij}^*$，故对于$\phi^t(y_{ij}^*)$，有
      $$\phi^t(y_{ij}^*)=\frac{y_{ij}^*}{y_{ij}^{t-1}+\epsilon}\approx
      \begin{cases}
      1, &if\ y_{ij}>0 \cr 
      0, &if\ y_{ij}=0
      \end{cases}
      $$
      - 因此，$\phi^t(y_{ij}^*)$近似等于$\mathbf{Z}$，对连续函数的求解与对原优化问题的求解相近
## 5 模型评估
### 5.1 参数设置
  - 网络参数
    - $\rm 500m \times 500m$的正方形区域
    - $15$个*BS*
    - 用户可以与$\rm 100m$的*BS*连接
    - 信道增益为$127+30\times\log d$
    - 噪声功率$\rm 2\times 10^{-13}W$
  - 用户设备参数
    - 计算资源：$\rm 10GHz$ 
    - 处理任务时间：$0.1$秒
    - 传输带宽：$\rm 20MHz$
    - 电池容量：$1000J$
  - 任务参数
    - $500$个任务
    - 计算量：服从正态分布，均值为$1千兆周期$
    - 数据大小：服从正态分布，均值为$\rm 5MB$
  - 边缘云参数
    - 计算资源：$25GHz$
    - 处理任务时间：$0.05$秒
    - 计算能耗：$\rm 90W/千兆周期$
### 5.2 算法对比
  - 随机卸载：随机选择任务卸载到边缘云或本地，根据*KKT*条件分配计算资源
  - 统一卸载：所有任务根据电池容量分为两部分，一部分卸载一部分本地，根据*KKT*条件分配计算资源
  - 仿真结论：从资源利用率上看，随机卸载，统一卸载和*SDTO*的资源利用率分别为$75％$，$80％$和$92％$

### 5.3 计算量/数据大小对卸载性能的影响
  - 任务的计算量/数据大小越大，任务持续时间越长，成本越高
  - 与随机卸载和统一卸载相比，我们提出的*SDTO*具有**更短的任务持续时间和更低的成本**
  - 计算量/数据大小遵循帕累托分布时，曲线趋势不像正态分布和均匀分布那样平滑，这是因为其具有长尾效应
  - **数据大小对任务持续时间和成本的影响低于计算量**

## 6 结论 
  - 提出*SD-UDN*的体系结构
  - 提出*SDTO*卸载方案
    - 任务的放置
    - 资源的分配
  - 仿真表明，*SDTO*的效率更高