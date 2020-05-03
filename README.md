# Machine_learning_code_with_python

只使用python来实现机器学习常见的算法（不借助sklearn等包），主要参考西瓜熟和统计机器学习这两本书，代码有一些是参考了网上其他
人的，我都会在里面注释。欢迎大家给个star或者来提pr，也欢迎大家一起交流。


[![MIT license](https://img.shields.io/dub/l/vibe-d.svg)](https://github.com/lawlite19/MachineLearning_Python/blob/master/LICENSE)


## 目录
* [机器学习算法Python实现](#机器学习算法python实现)
	* [一、Linear_Regression](#一Linear_Regression)
	* [二、PCA](#二PCA)
    * [三、Navie_Bayes](#三Navie_Bayes)
    * [四、SVM](#四SVM)
    * [五、KNN](#五KNN)
    * [六、KMeans](#六KMeans)（TODO）
    * [七、Decision_Tree](#七Decision_Tree)
    * [八、Logistic_Regression](#八Logistic_Regression)
    * [九、LDA](#九Linear_Discriminant_Analysis)
    * TODO
    

## 一、[Linear_Regression](/Linear_Regression)
- [全部代码](/Linear_Regression/linearRegression.ipynb)
- [算法推导](/Linear_Regression/README.md)  
##### 优点：
1、算法简单，可解释性强；  
     
##### 缺点：
1、需要严格的假设；  
2、需处理异常值，对异常值很敏感，对输入数据差；  

##### 适用场景：
自变量和因变量之间是线性关系，适用于low dimension， 而且每一维之间都没有共线性。


## 二、[PCA](/PCA)
- [全部代码](/PCA/PCA.ipynb)
- [算法推导](/PCA/README.md)
##### 优点：
1、可处理大规模数据集；  
2、无需在数据上进行假设；  

##### 缺点：
1、难以搞定非线性数据；
2、难以理解结果的意义；  

##### 适用场景：
维度过高的时候可以用来降低维度。  



## 三、[Navie_Bayes](/Navie_Bayes)
- [全部代码](/Navie_Bayes/navieBayes.ipynb)
- [算法推导](/Navie_Bayes/README.md)
##### 优点：
1、快速、易于训练、给出了它们所需的资源能带来良好的表现；

##### 缺点：
1、如果输入变量是相关的，则精度会出现一定幅度的下降；

##### 适用场景：
需要一个比较容易解释，而且不同维度之间相关性较小的模型的时候。可以高效处理高维数据，虽然结果可能不尽如人意。



## 四、[SVM](/SVM)
- [全部代码](/SVM/SVM.ipynb)（TODO）
- [算法推导](/SVM/README.md)
##### 优点：
1、在非线性可分问题上表现优秀；  
2、SVM 的最终决策函数只由少数的支持向量所确定,计算的复杂性取决于支持向量的数目,而不是样本空间的维数,这在某种意义上避免了“维数灾难”。  
3、少数支持向量决定了最终结果,这不但可以帮助我们抓住关键样本、“剔除”大量冗余样本,而且注定了该方法不但算法简单,而且具有较好的“鲁棒”性。这种“鲁棒”性主要体现在: 
①增、删非支持向量样本对模型没有影响; ②支持向量样本集具有一定的鲁棒性; ③有些成功的应用中,SVM 方法对核的选取不敏感；  
4、它基于结构风险最小化原则，这样就避免了过学习问题，泛化能力强；  
5、它是一个凸优化问题，因此局部最优解一定是全局最优解的优点；  
6、泛华错误率低，分类速度快，结果易解释；  

##### 缺点：
1、大规模的训练样本比较难训练。SVM的空间消耗主要是存储训练样本和核矩阵，由于SVM是借助二次规划来求解支持向量，而求解二次规划将涉及m阶矩阵的计算（m为样本的个数），当m数目很大时该矩阵的存储和计算将耗费大量的机器内存和运算时间。  
2、对缺失数据敏感，对参数和核函数的选择敏感；  

##### 适用场景：
SVM在很多数据集上都有优秀的表现。相对来说，SVM尽量保持与样本间距离的性质导致它抗攻击的能力更强。和随机森林一样，这也是一个拿到数据就可以先尝试一下的算法。



## 五、[KNN](/KNN)
- [全部代码](/KNN/KNN.ipynb)
- [算法推导](/KNN/README.md)（TODO）
##### 优点：
1、算法简单，可解释性强；  
2、可以生成任意形状的决策边界，因此在分割线比较模糊的分类问题上表现也能不错；
     
##### 缺点：
1、内存消耗高；计算成本高；  
2、不可能用于高维特征空间；  
3、数据量不能过少，否则会因样本数量过少或（和）特征数量过多而导致维度灾难：无法满足密采样条件（样本稀疏问题：维度越高，填充空间所需的数据量越多，可能导致无法找到一个“最近”的样本）；计算量太大（高维空间在距离计算上的问题）；  
4、数据量也不能过多，因为其所耗时间和空间随着数据量增大。这是由于基于实例的方法需要把所有的实例数据（训练样本）都打包做成模型（因为它需要计算对所有样本的距离，然后排序取最近的），所谓数据即模型。其它方法只需提交训练得到的模型和参数即可；  

##### 适用场景：
由于KNN训练的代价小(lazy learning不作训练)，KNN或可被用于在线学习(online machine learning)中，即使用新数据不断训练和更新已有模型从而作出更好的预测。
需要一个特别容易解释的模型的时候，比如需要向用户解释原因的推荐算法。


## 七、[Decision_Tree](/Decision_Tree)
- [全部代码](/Decision_Tree/decision_Tree.ipynb)
- [算法推导](/Decision_Tree/README.md)（TODO）
##### 优点：

     
##### 缺点：

##### 适用场景：



## 八、[Logistic_Regression](/Logistic_Regression)
- [全部代码](/Logistic_Regression/logisticRegression.ipynb)
- [算法推导](/Logistic_Regression/README.md)（TODO）
##### 优点：

     
##### 缺点：

##### 适用场景：


## 九、[Linear_Discriminant_Analysis](/LDA)
- [全部代码](/LDA/LDA.ipynb)（TODO）
- [算法推导](/LDA/README.md)
##### 优点：

     
##### 缺点：

##### 适用场景：