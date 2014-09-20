# Jacobian和Hessian，线性变换和极值

标签（空格分隔）： Jacobian-Hessian FirstSecond-PartialDerivative matrix linear-map index

---

##Jacobian矩阵，一阶偏导，和线性变换

向量函数$y=F(x)$ ($x \in R^n$, $y \in R^m$) 关于自变量$x \in R^n$的一阶偏导定义为：
$$\frac{\partial F}{\partial x} \stackrel{def}{=} \left[ \begin{array}{ccc}
  \frac{\partial F_1}{\partial x_1} & ... & \frac{\partial F_1}{\partial x_n} \\
  \vdots & \vdots &  \vdots \\
  \frac{\partial F_m}{\partial x_1} & ... & \frac{\partial F_m}{\partial x_n} \end{array} \right]  \stackrel{def}{=} J. $$
  
矩阵$J$叫做Jacobian矩阵，以纪念德国数学家Jacobi (1804-1851).
实际上，从$x \in R^n$到$y \in R^m$的线性变换的矩阵表示$J^{m \times n}$，就是向量函数$y=Jx$的一阶偏导：
$$ \frac{\partial (Jx)}{\partial x} = J.$$

##Hessian矩阵，二阶偏导，和极值
实值函数$y=f(x)$关于自变量$x \in R^n $的二阶偏导定义为：

$$\frac{\partial^2 f}{\partial x^2} \stackrel{def}{=} \left[ \begin{array}{ccc}
\frac{\partial^2 f}{\partial x_1^2} & ... & \frac{\partial^2 f}{\partial x_1 \partial x_n} \\
\vdots & \vdots &  \vdots \\
\frac{\partial^2 f}{\partial x_n \partial x_1} & ... & \frac{\partial^2 f}{\partial x_n^2} \end{array} \right] \stackrel{def}{=} H  \equiv  \nabla^2f . $$
  
矩阵$H$叫做Hessian矩阵，以纪念德国数学家Hesse (1811-1974). 由欧拉定理(1734年）可知，矩阵$H$是对称的。
Hessian矩阵的正定性，可用于判断二次型$f(x) = \frac 1 2 (x-x_0)^\intercal H(x_0) (x-x_0) + \nabla f(x_0) (x-x_0) + f(x_0)$的局部极值性。而矩阵的正定性，又与该矩阵的特征值紧密相关。








