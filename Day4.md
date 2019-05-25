# 从基础概率推导贝叶斯公式，朴素贝叶斯，学习先验概率，后验概率
![image](https://github.com/keke1u/LeeML/blob/master/Naive-Bayes-Classifier1.jpg?raw=true)
![image](https://github.com/keke1u/LeeML/blob/master/Naive-Bayes-Classifier2.jpg?raw=true)
![image](https://github.com/keke1u/LeeML/blob/master/Naive-Bayes-Classifier3.jpg?raw=true)
![image](https://github.com/keke1u/LeeML/blob/master/Naive-Bayes-Classifier4.jpg?raw=true)
# LR与Linear Regression之间的区别
   都是广义的线性回归
   从回归的角度：LR是在线性回归后施加了一个非线性函数，从而达到二分类的目的
   即线性回归的值域是R，LR的值域被Sigmoid函数映射到了[0,1]，通过设置阈值进行分类器判断。
   从概率模型的角度，在二分类的LDA中，判别边界函数可写为Logistic回归模型的形式（推导见后）
# 二分类LDA的推导
![image](https://github.com/keke1u/LeeML/blob/master/LDA.png?raw=true)
