# 矩阵的Schur补和群论的Lagrange定理

标签（空格分隔）： Schur-MatrixInverse Lagrange-SubGroup Gauss-MultivariateNormal index

---

本文先介绍通过将矩阵对角化得到分块矩阵的Schur补，然后用一个直观的记号代表该Schur补，从中可以得到一个形式上美丽的公式，不禁让人想起贝叶斯定理、群论中的Lagrange定理。

##矩阵的Schur补
已知矩阵$\Sigma$可分块如下：
$$\Sigma = \left[ \begin{array}{cc}
  \Sigma_{11} & \Sigma_{12} \\
  \Sigma_{21} & \Sigma_{22} \end{array} \right]. $$
在$\Sigma_{22}$可逆的情况下，可将$\Sigma$块对角化得到：
$$\begin{equation} \left[\begin{array}{cc}
    I & -\Sigma_{12}\Sigma_{22}^{-1} \\
    0 & I \end{array} \right]
  \Sigma
  \left[ \begin{array}{cc}
    I       &       0  \\
    -\Sigma_{22}^{-1}\Sigma_{21} & I \end{array} \right]
=  \left[ \begin{array}{cc}
\Sigma_{11}-\Sigma_{12}\Sigma_{22}^{-1}\Sigma_{21} & 0  \\
0 & \Sigma_{22} \end{array} \right]. \end{equation}$$

这里，左上的非零块矩阵$\Sigma_{11}-\Sigma_{12}\Sigma_{22}^{-1}\Sigma_{21}$就叫做矩阵$\Sigma$关于分块$\Sigma_{22}$的**Schur补**。可用一个直观的记号代表他：
$$\Sigma/\Sigma_{22} \equiv \Sigma_{11}-\Sigma_{12}\Sigma_{22}^{-1}\Sigma_{21}. $$
***为什么用这个记号呢？***
来看看当对上述矩阵对角化等式两边施加行列式算子时能得到什么吧！因为：
>* $\begin{vmatrix}AB\end{vmatrix} = \begin{vmatrix}A\end{vmatrix} \begin{vmatrix}B\end{vmatrix}$，和
>* 三角矩阵的行列式等于对角块上的行列式之积

所以等式左边=$\begin{vmatrix}\Sigma\end{vmatrix}$，等式右边=$\begin{vmatrix}\Sigma_{11}-\Sigma_{12}\Sigma_{22}^{-1}\Sigma_{21}\end{vmatrix} \begin{vmatrix}\Sigma_{22}\end{vmatrix}$，用刚才的Schur补记号可以得到如下行列式等式：
$$\begin{vmatrix} \Sigma \end{vmatrix} = \begin{vmatrix} \Sigma/\Sigma_{22} \end{vmatrix}  \begin{vmatrix} \Sigma_{22} \end{vmatrix}.$$
现在撇开什么矩阵啊行列式啊Schur补啊，就只看这个行列式等式，是不是从形式上***自然***就成立了！在$\Sigma_{11}$可逆的情况下，模仿上述等式可得到：
$$\begin{vmatrix} \Sigma \end{vmatrix} = \begin{vmatrix} \Sigma/\Sigma_{11} \end{vmatrix}  \begin{vmatrix} \Sigma_{11} \end{vmatrix}.$$
这里记号$\Sigma/\Sigma_{11}$表示$\Sigma$关于$\Sigma_{11}$的Schur补。
通过$\Sigma$作为桥梁，可将两者联系起来：
$$ \begin{vmatrix} \Sigma/\Sigma_{11} \end{vmatrix}  \begin{vmatrix} \Sigma_{11} \end{vmatrix} = \begin{vmatrix} \Sigma/\Sigma_{22} \end{vmatrix}  \begin{vmatrix} \Sigma_{22} \end{vmatrix}.$$
***再看一眼，联想到了什么？贝叶斯定理？Lagrange定理？抑或群同态基本定理？***
$$......$$

##贝叶斯定理
贝叶斯定理在形式上可由联合概率$ P(X,Y)$作为桥梁：
$$P(X)P(Y|X) = P(Y)P(X|Y)$$
导出：
$$P(Y|X) = \frac{P(Y)P(X|Y)}{P(X)}, P(X) \neq 0.$$

##Lagrange定理
群论Lagrange定理说明有限群$G$与其子群$H$的规模之比是一个整数（毕达哥拉斯：“一切真理都可以用比例去反映和证实”）：
$${|G|}/{|H|} = [G:H],$$
这个整数比叫做$H$在$G$中的指数，即陪集数。
可能由于历史的原因，这个指数的记号是$[G:H]$，不过我认为完全可以用$|G/H|$来代替更直观：
$${|G|}/{|H|} = |G/H|.$$
另一个原因是记号$G/H$已经有固定含义了：表示由群$G$和$G$的正规子群$H$构造得到的商群：$G/H = $ { $Hg|g \in G$ } 注意集合元素的型构是陪集，同态基本定理说商群$G/H$是群$G$的同态像。

##多元正态分布
在第一个部分**矩阵的Schur补**中用的记号是$\Sigma$，自然联想到多元高斯分布的的协方差矩阵。是的本篇小文的源头就是Jordan和Bishop的书稿 *An Introduction to Graphical Models* 第12章[*The Multivariate Gaussian*][1]，里面还讲了如何用Trace Trick求多元高斯分布关于协方差矩阵的导数，从而得到分布参数$(\mu,\Sigma)$的最大似然估计。

[1]: http://people.csail.mit.edu/yks/documents/classes/mlbook/pdf/chapter12.pdf
