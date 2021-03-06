# 统计学习方法 李航



## Ch1 统计学习方法概论



### 1. 概述

1. 统计学习是关于计算机基于数据构建概率统计模型并运用模型对数据进行分析与预测的一门学科。

    统计学习包括 **监督学习**、**非监督学习**、**半监督学习** 和 **强化学习**

    

2. 统计学习方法三要素—— **模型、策略、算法**



3. **监督学习**

从给定有限的训练数据出发，假设数据是 **独立同分布的**，且假设模型属于某个假设空间，应用于某一评价准则，从假设空间中选取一个最优的模型，使它 **对已给训练数据及未知测试数据在给定评价标准意义下有最准确的预测**



4. 统计学习中，进行 **模型选择** 或者 **提高学习的泛化能力** 是一个重要问题。

​		如果只减少训练误差，就可能产生 <font color=red>**过拟合**</font> 现象。

> 过拟合  [维基百科](https://zh.wikipedia.org/wiki/%E9%81%8E%E9%81%A9)
>
> overfitting
>
> 过于紧密或精确地匹配特定数据集，以致于无法良好地拟合其他数据或预测未来的观察结果的现象
>
> 发生过拟合时，模型的偏差小而方差大

  - 模型选择的方法
    - 正则化
    - 交叉验证

学习方法泛化能力的分析是统计学习理论研究的重要课题



5. **分类问题**、**标注问题** 和 **回归问题**  是监督学习的重要问题。

    本书中介绍的统计学习方法包括：

    - 感知机
    - k 邻近法
    - 朴素贝叶斯法
    - 决策树
    - 逻辑斯蒂回归 logistic regression
    - 最大熵模型
    - 支持向量机
    - 提升方法
    - EM 算法
    - 隐马尔可夫模型
    - 条件随机场

    这些方法是主要的分类、标注以及回归方法。他们又可以归类为生成方法和判别方法。





### 2. 使用最小二乘法拟合曲线

高斯于 1823 年在误差 <font color=red> $e_1,...,e_n$ </font> 独立同分布的假定下，证明了最小二乘法的一个最优性质：

**在所有无偏的线性估计类中，最小二乘方法是其中方差最小的！**

对于数据 $(x_i,y_i)(i = 1,2,3,...,m)$

拟合出函数 $h(x)$

有误差，即 **残差** : 
$$
r_i = h(x_i) - y_i
$$
此时 $L2$  **范数**(<font color = purple>**残差平方和**</font>) 最小时，$h(x_i)$ 和 $y_i$ 相似对最高，更拟合

一般的 $H(x)$ 为 $n$ 次的多项式
$$
H(x) = w_0 + w_1x + w_2x^2 + w_nx^n
$$
$w(w_0,w_1,...,w_n)$ 为参数

**<font color = red>最小二乘法就是要找到一组 $w(w_0,w_1,...,w_n)$ ，使得 $\sum_{i=1}^n(h(x_i)-y_i)^2$ (残差平方和) 最小</font>**

即，求 $min\sum_{i=1}^n(h(x_i)-y_i)^2$

****

#### 举例

用目标函数 $y = sin2\pi x$， 加上一个正态分布的噪音干扰，用多项式拟合【例1.1 11 页】









































































