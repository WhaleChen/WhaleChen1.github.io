---
layout: post
title: 机器学习笔记第一周
---

### Model and Cost Function

### Model Representation

#### Notation 这门课的Notation 有别于我之前的尝试
- m = Number of training examples
- x's ="input" variable / features
- y's ="output" variable /target variable
- (x,y)  to one training example
- (x^(i),y^(i)) to i_th traing example 
- h : hypothesis: 这里理解的hypothesis 是一个函数，和一般的理解有区别，不过其实也可以直觉性的认为其实任何函数都是人造的，因此称为hypothesis是合适的

### Cost Funtion with univariate linear regression 单一变量回顾
- Cost Function: 可以认为是成本函数，其实这很形象，预测所需要的成本，那些根本不靠谱的模型的成本高，最契合的模型成本最低
- Squared error function，通常情况下使用的函数。
- Notation: J(theta) 
- Notation: theta_j := theta_j - delta J(theta)   ":=" 为assignment
- Simultaneous update:
- convex function: only on global min 
- Batch: Each step of gradient descent uses all the training examples.

### Feature Scaling:
- 让所有feature变为 大致 -1<= x_i <= 1 range
- 可以使得迭代速率增大
- Mean normalization: 
	- (x_i - u) / range(max to min) 代替 x_i 
	- 这样的处理可以使得 总体变得接近于 (-1,1)

### Learning Rate

- 