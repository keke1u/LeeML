# 什么是Machine Learning

    可以看做是looking for a function from data
    Step1: define a set of function
    Step2: compute the goodness of function
    Step3: pick te best function
![image](https://github.com/keke1u/LeeML/blob/master/Types_of_ML.jpg?raw=true)
# 学习中心极限定理，正态分布，最大似然估计
- 中心极限定理：
    在一定的条件下，独立随机变量和的分布函数会收敛于正态分布
- 最大似然估计
![image](https://github.com/keke1u/LeeML/blob/master/MLE.jpg?raw=true)
# 推导回归的Loss Function
    此处指一元线性回归，为平方损失函数
# 推导梯度下降的公式(from 李航_统计学习方法)
![image](https://github.com/keke1u/LeeML/blob/master/Gradient_Descent.jpg?raw=true)
# 写出梯度下降(Gradient Descdent)的代码
```
import numpy as np

x = np.array([1,5,7,9,15,16]) # 6个样本
y = np.array([2,11,13,19,31,30])

m  = 5
iter = 10
lr = 0.01
w = 1.8
b = 0.1
cost = []

for t in range(iter):
    yhat = x*w
    cost1 = np.sum((y-yhat)**2) / (2.0*m)
    cost.append(cost1)
    dw = -np.dot(x.T,y-yhat)/m
    db = -np.sum(yhat-y)/m
    w = w - lr*dw
    b = b - lr*db
print(cost)
```
- another one
```
class LinearRegressionGD(object):

    def __init__(self, eta=0.001, n_iter=20):
        self.eta = eta
        self.n_iter = n_iter

    def fit(self, X, y):
        self.w_ = np.zeros(1 + X.shape[1])
        self.cost_ = []

        for i in range(self.n_iter):
            output = self.net_input(X)
            errors = (y - output)
            self.w_[1:] += self.eta * X.T.dot(errors)
            self.w_[0] += self.eta * errors.sum()
            cost = (errors**2).sum() / 2.0
            self.cost_.append(cost)
        return self

    def net_input(self, X):
        return np.dot(X, self.w_[1:]) + self.w_[0]
```


# 学习L2-norm,L1-norm,L0-norm并推导regularization公式
    正则化是模型选择的典型方法，可以防止过拟合(模型过于复杂，使得训练误差小但测试误差大)。
    是在经验风险上加一个正则化项(regularizer)或惩罚项(penalty term)
![image](https://github.com/keke1u/LeeML/blob/master/Regularization.jpg?raw=true)

# 说明为什么用L1-norm代替L0-norm
    从直观上看，利用非零参数的个数，可以很好的来选择特征，实现特征稀疏的效果，具体操作时选择参数非零的特征即可。但因为L0正则化很难求解，是个NP难问题，因     此一般采用L1正则化。L1正则化是L0正则化的最优凸近似，比L0容易求解，并且也可以实现稀疏的效果。
    
    L1正则化，在回归中称为Lasso.
    L2正则化，在回归中称为Ridge Regression.
# 学习为什么只对w做限制而不对b
b为bias项，不影响模型的复杂程度。
