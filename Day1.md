# 什么是Machine Learning

    可以看做是looking for a function from data
    Step1: define a set of function
    Step2: compute the goodness of function
    Step3: pick te best function
![image](https://github.com/keke1u/LeeML/blob/master/Types_of_ML.jpg?raw=true)
# 学习中心极限定理，正态分布，最大似然估计
- 中心极限定理
    在一定的条件下，独立随机变量和的分布函数会收敛于正态分布
- 最大似然估计
![image](https://github.com/keke1u/LeeML/blob/master/MLE.jpg?raw=true)
# 推导回归的Loss Function
    此处指一元线性回归，为平方损失函数
# 推导梯度下降的公式(from 李航_统计学习方法)
![image](https://github.com/keke1u/LeeML/blob/master/Gradient_Descent.jpg?raw=true)
# 写出梯度下降(Gradient Descdent)的代码


# 学习L2-norm,L1-norm,L0-norm并推导regularization公式
    正则化是模型选择的典型方法，可以防止过拟合(模型过于复杂，使得训练误差小但测试误差大)。
    是在经验风险上加一个正则化项(regularizer)或惩罚项(penalty term)
![image](https://github.com/keke1u/LeeML/blob/master/Regularization.jpg?raw=true)


# 说明为什么用L1-norm代替L0-norm

# 学习为什么只对w做限制而不对b
