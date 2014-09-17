# Michael Jordan 2014 Reddit

标签（空格分隔）： Jordan ML Statistics Reddit index

---
##非参贝叶斯
从LDA到HDP，贝叶斯非参。
出新书。[Yee Whye Teh][1]

##读书三遍
为博士准备的练内功的[新书单][2]
读书三遍，其意自现。
barely understand -> start to get it -> it all seems obvious

##ML = statistical inference = decision-making

## Deep = Layering
DL成功：有监督 (backpropagation)+大数据。
weight-sharing，ensembling。
无监督学习是圣杯。
将表示/特征形式化为贝叶斯先验。
Stat/ML要进入计算机系统和数据库中。

##不确定性。data science。
>* ML:
Throughout the eighties and nineties, it was striking how many times people working within the "ML community" realized that their ideas had had a lengthy pre-history in statistics. 
Decision trees, nearest neighbor, logistic regression, kernels, PCA, canonical correlation, graphical models, K means and discriminant analysis come to mind, and also many general methodological principles (e.g., method of moments, which is having a mini-renaissance, Bayesian inference methods of all kinds, M estimation, bootstrap, cross-validation, ROC, and of course stochastic gradient descent, whose pre-history goes back to the 50s and beyond),and many many theoretical tools (large deviations, concentrations, empirical processes, Bernstein-von Mises, U statistics, etc).
>* Stat:
the "statistics community" was also not ever that well defined,
and while ideas such as Kalman filters, HMMs and factor analysis originated outside of the "statistics community" narrowly defined, there were absorbed within statistics because they're clearly about inference. 
**注1**：统计推断是现代统计学的同义词，卡尔皮尔逊和戈赛特(笔名学生)是两位先驱，而RA Fisher则是其创立者。
**注2**：不涉及推断的统计学是描述统计学，如计算样本均值，此时也一般不涉及概率和不确定性。
>* NN:
layered neural networks can and should be viewed as nonparametric function estimators, objects to be analyzed statistically.

##PGM从chain(HMM CRF)到tree(LDA, etc)
I continue to find much inspiration in tree-based architectures, particularly for problems in three big areas where trees arise organically---evolutionary biology, document modeling and natural language processing. 
### 1. Evolutionary biology
I've worked recently with Alex Bouchard-Cote on evolutionary trees, where the entities propagating along the edges of the tree are strings of varying length (due to deletions and insertions), and one wants to infer the tree and the strings. 
### 2. Document modeling
In the topic modeling domain, I've been very interested in multi-resolution topic trees, which to me are one of the most promising ways to move beyond latent Dirichlet allocation. 
John Paisley, Chong Wang, Dave Blei and I have developed something called the nested HDP in which documents aren't just vectors but they're multi-paths down trees of vectors. 
### 3. Natural language processing
Lastly, Percy Liang, Dan Klein and I have worked on a major project in natural-language semantics, where the basic model is a tree (allowing syntax and semantics to interact easily), 
but where nodes can be set-valued, such that the classical constraint satisfaction (aka, sum-product) can handle some of 
the "first-order" aspects of semantics.

## FnT@ML
most important high level trends in machine learning research and industry applications these days.
>* the merger of statistical thinking and 
computational thinking;
>* the need for statistics/ML to ally itself more with CS systems and database researchers rather than focusing mostly on AI.

[@truth4sex][3]

**原文**：http://www.reddit.com/user/michaelijordan

[1]:http://www.stats.ox.ac.uk/~teh/npbayes.html
[2]:http://www.reddit.com/r/MachineLearning/comments/2fxi6v/ama_michael_i_jordan/ckejn25?context=3
[3]:http://weibo.com/truth4sex




