!SLIDE center subsection

# 激活函数

!SLIDE

# 什么是激活函数

* 根据输入确定神经元的输出
* 每神经元拥非线行传递函数
* 每层各别定义
* 使神经网络为特征做出复杂的边界决策

!SLIDE

# 激活函数

* 隐藏层
  * 控制发向连接神经元的信号
* 输出层
  * 决定输出值
    * 回归
    * 分群
    * 等等


!SLIDE

# 常用激活函数

* ReLU
  * 最近的突破
  * 用于缺省值
* Sigmoid
  * S 型 范围 0 到 1
  * 用于缺省值
* TanH
  * S 型 范围 -1 到 1


~~~SECTION:notes~~~
# Keep SImple Listing and move most to the appendix
~~~ENDSECTION~~~

!SLIDE

# Activation Functions

![img](../resources/Activation-func.png)

!SLIDE

# Output Layer Activation

* Special Case
* Goal of hidden Layer activation is to squash intermediate values
* Goal of output Layer is to answer our question
  * Classification = softmax
  * regression = identity

~~~SECTION:notes~~~

Add One Hot Encoding discussion with Classification and SoftMax

~~~ENDSECTION~~~

!SLIDE

# Output Layer Guidelines

* Classification
  * softmax activation
  * Negative Log Likelihood for loss Function
  * Multi Class Cross Entropy
* Softmax
  * Probability Distribution over classes
  * Outputs sum to 1.0
* Regression
  * Identity Activation
  * MSE(Mean Squared Error) Loss Function

!SLIDE

# Quick Statistics Review: Probability

* Probability
	* We define probability of an event E as a number always between 0 and 1
	* In this context the value 0 infers that the event E has no chance of occurring and the value 1 means that the event E is certain to occur
* The Canonical Coin Example
	* Fair coin flipped, looking for heads/tails (0.5 for each side)
	* Probability of sample space is always 1.0
	* P( Heads ) = 0.5 every time


!SLIDE


# Classification

* A type of answer we can get from a model
* Example:
	* “Is this an image of a cat or a dog?”
	* Binary classification
	* Classes: { cat, dog }
* Binary classification is where we have only 2 labels
	* Example: { positive, negative }
* Multi-Label Classification
	* N number of labels

!SLIDE



# Regression


* Where we seek a continuous value output from the model
* Example: “predict the temperature for tomorrow”
	* Output: 75F
* Example: “predict price of house based on square footage”
	* Output: $250,000.00



~~~SECTION:notes~~~

activation function for the output layer:
this is usually application specific.
For classification problems, you generally want to use the softmax activation function, combined with the negative log likelihood / MCXENT (multi-class cross entropy).

The softmax activation function gives you a probability distribution over classes (i.e., outputs sum to 1.0). For regression problems, the “identity” activation function is frequently a good choice, in conjunction with the MSE (mean squared error) loss function.


~~~ENDSECTION~~~
