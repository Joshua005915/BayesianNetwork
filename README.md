# 1 隐马尔科夫模型基础
## 1.0 基础知识
* 全概率公式

![1](http://latex.codecogs.com/svg.latex?P(X)=\sum_{y}P(X,Y=y))

理解：全概率公式不要求对X事件与Y事件的相关性做出任何假设。X发生的概率即为枚举所有Y的可能情况下X发生的概率之和。
* 贝叶斯公式

![1](http://latex.codecogs.com/svg.latex?P(X|Y)=\frac{P(X,Y)}{P(Y)}=\frac{P(Y|X)P(X)}{P(Y)})

理解：事件X为待推理事件，Y为证据事件。P(X|Y)为观测到证据Y后，推测X发生的概率。P(Y|X)为输出概率(emission probability)，即X发生后观测到证据Y的概率。贝叶斯公式的主要作用就是依据发散概率推测源事件发生的概率

例子：根据历史观测情况，你发现下雨后你的室友有90%的概率会打伞，今早你发现你的室友出门时带了伞，即可推测今天下雨的概率（当然还需要知道当地下雨的概率和你室友打伞的概率，但这些都可以依据历史事件进行统计）。

* 概率图基本类型
  1. 顺连 
  ```
  graphTD
  A[A] -- > B[B]
  ```
  
  2. 汇连
  3. 分连
## 1.1 模型构建
## 1.2 BW算法
* 前向算子

**定义：前向算子**

t时刻的前向算子为观测到从1时刻至t时刻的所有证据以及t时刻状态s(t)=j的概率。


![1](https://latex.codecogs.com/svg.latex?\begin{equation}\alpha_j(t)=P(V(1),V(2),...,V(t),s(t)=j)\end{equation})

当t=1时：

![2](https://latex.codecogs.com/svg.latex?\begin{equation}\alpha_j(t)&=&P(V(1),s(1)=j)\\\\&=&P(V(1)=k_1|s(1)=j)P(s(1)=j)\end{equation})






这里P(s(1)=j)为初始概率，用
![2](https://latex.codecogs.com/svg.latex?P(V(1),s(1)=j))表示，P(V(1)|s(1)=j)为输出概率(emission probability)，用![4](https://latex.codecogs.com/svg.latex?b_{jk_1})表示。


* 后向算子
* 前向后向算子
* 参数学习
## 1.3 实验
## 1.4 探索方向
