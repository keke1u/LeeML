# 理解偏差和方差 Bias and Variance
- 学习误差为什么是偏差和方差而产生的，并且推导数学公式
![image](https://github.com/keke1u/LeeML/blob/master/Bias_Variance.jpg?raw=true)
- 推导
![image](https://github.com/keke1u/LeeML/blob/master/Bias_Variance3.jpg?raw=true)

- 过拟合，欠拟合，分别对应bias和variance什么情况
![image](https://github.com/keke1u/LeeML/blob/master/Bias_Variance2.jpg?raw=true)

   Bias大，Underfitting: 应该重新设计model
   Variance大，Overfitting：more data 或 Regularization
# 学习鞍点，复习全局最优和局部最优
- 解决办法有哪些
# 梯度下降
- 学习Mini-Batch与SGD



- 学习Batch与Mini-Batch，SGD梯度下降的区别

- 如何根据样本大小选择哪个梯度下降(批量梯度下降，Mini-Batch）

- 写出SGD和Mini-Batch的代码

# 学习交叉验证(Cross Validation)
   可以有效避免划分训练集和测试集时的随机性对评价结果造成的影响。
   我们可以把原始数据集平均分为**K**组不重复的子集，每次选**K - 1**组子集作为训练集，剩下的一组子集作为验证集。
   这样可以进行**K**组实验并获得**K**个模型，这**K**个模型在各自验证集上的错误率的平均作为分类器的评价。

# 学习归一化



# 学习回归模型评价指标
