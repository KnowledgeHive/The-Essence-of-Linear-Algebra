# The-Essence-of-Linear-Algebra

[线性代数的本质笔记完整版](http://knowledgehive.github.io/The-Essence-of-Linear-Algebra)



[线性代数的本质](https://www.bilibili.com/video/BV1ys411472E)这个课程我大概已经完整的看过两遍以上了，但是当我想要找找当年的笔记，去回顾回顾里面的直观的动画时，发现已经基本上对里面的内容完全忘光了。

目前仅仅有一些笔记的记录，后续可能会上传一些动图的展示，看个人的时间吧。



回顾几个本质性的动画：

+ chapter3: 二维矩阵 $$\begin{pmatrix}a & b\\ c &d\end{pmatrix}$$实际上就是一个坐标系的变换：原来的横坐标$$\hat{i} = \begin{pmatrix}
  1\\ 
  0
  \end{pmatrix}$$ 变换为$$\begin{pmatrix}
  a\\ 
  c
  \end{pmatrix}$$。纵坐标$$\hat{j}$$同理。

$$
\begin{pmatrix}
a & b\\ 
c &d 
\end{pmatrix} * \begin{pmatrix}
x\\ 
y
\end{pmatrix} = x*\begin{pmatrix}
a\\ 
c
\end{pmatrix} + y*\begin{pmatrix}
b\\ 
d
\end{pmatrix}
$$



+ chapter4: 二维矩阵的乘法实际上就是一系列坐标系变换。


$$
\begin{pmatrix}
a & b\\ 
c &d 
\end{pmatrix} * \begin{pmatrix}
e & f\\ 
g & h 
\end{pmatrix}\\
可以看成是对基向量\begin{pmatrix}
e\\ 
g
\end{pmatrix}和\begin{pmatrix}
f\\ 
h
\end{pmatrix}的变换。\\
\begin{pmatrix}
a & b\\ 
c &d 
\end{pmatrix} * \begin{pmatrix}
e\\ 
g
\end{pmatrix}\\
\begin{pmatrix}
a & b\\ 
c &d 
\end{pmatrix} * \begin{pmatrix}
f\\ 
h
\end{pmatrix}\\
最后将这两个向量合并，形成结果矩阵\begin{pmatrix}
ae+bg & af+bh\\ 
ce+dg & cf+dh 
\end{pmatrix}
$$

+ chapter5: 二维行列式的值实际上就是带有方向的向量围成的面积，同理三维的表示体积。

+ chapter6: $$ Ax=b $$要有解必须$$det(A)\ne 0$$，原因是若为0，那么就会将二维的坐标压成一条直线，或者是原点，那么若压成一条直线与$$b$$不同方向，那么肯定是无解的。

  当然$$Ax=0$$想要有非0解必须$$det(A) = 0$$，原因很形象，若不为0，那么显然A可逆，对应的变换唯一，只能是0向量。只有为$$det(A)=0$$，才会使二维的向量压缩到一维，那么，才会有非零解向量压缩到零向量。

+ chapter7: 点积的直观解释
  $$
  \begin{bmatrix}
  a\\ 
  b
  \end{bmatrix}·
  \begin{bmatrix}
  y\\ 
  y
  \end{bmatrix} = \begin{bmatrix}
  a & b
  \end{bmatrix}*\begin{bmatrix}
  x\\ 
  y
  \end{bmatrix} = ax+by
  $$
  其中$$\begin{bmatrix}
  a & b
  \end{bmatrix}$$看成是$$\hat{i} 和 \hat{j}$$从二维的向量投影到一维的数轴的坐标。$$\begin{bmatrix}
  x\\ 
  y
  \end{bmatrix}$$实际上也是往数轴上进行投影。

+ chapter8: 叉积

二维的叉积就是矩阵行列式的值。

三维叉积是一个向量，大小为围成的面积，方向根据右手定则进行确定。

$$\overrightarrow{v}\times \overrightarrow{w} = \overrightarrow{p}$$，至于结果p为什么是面积大小，且垂直于四边形，且看下面的直观解释。

定义下面的运算：
$$
\begin{bmatrix}
p_1\\ 
p_2\\ 
p_3
\end{bmatrix}·\begin{bmatrix}
x\\ 
y\\ 
x
\end{bmatrix} = det(\begin{pmatrix}
 x & v_1 & w_1\\ 
 y & v_2 & w_2\\ 
 z & v_3 & w_3
\end{pmatrix})
$$
等式的右边就是一个立方体的体积，三条边就是竖着的三个向量。那么体积怎么算呢？就是$$\overrightarrow{v}$$和$$\overrightarrow{w}$$构成的四边形面积*x向量在高度上的投影长度。

我们之前知道__点积其实就是投影长度的积__。

那么很显然，p长度就是$$\overrightarrow{v}$$和$$\overrightarrow{w}$$构成四边形面积大小，方向与平面垂直。

至于具体怎么计算，则
$$
\overrightarrow{p} = \begin{pmatrix}
 \overrightarrow{i} & v_1 & w_1\\ 
\overrightarrow{j}  & v_2 & w_2\\ 
\overrightarrow{k} & v_3 & w_3
 \end{pmatrix}
$$


+ chapter9: 基变换

$$Ax = b$$, $$x$$是变换后坐标系的观察，$$b$$是正常坐标系。

至于为什么$$x$$是变化后坐标系的视野，根据前面的运算：
$$
\begin{pmatrix}
a & b\\ 
c &d 
\end{pmatrix} * \begin{pmatrix}
x\\ 
y
\end{pmatrix} = x*\begin{pmatrix}
a\\ 
c
\end{pmatrix} + y*\begin{pmatrix}
b\\ 
d
\end{pmatrix}
$$
$$\begin{pmatrix}
a\\ 
c
\end{pmatrix}$$和$$\begin{pmatrix}
b\\ 
d
\end{pmatrix}$$分别是新的__基底__，那么（x, y）就是新坐标视野下的坐标。

+ chapter10：特征向量和特征值

就是找到那么坐标变换后方向没有改变的向量，对应的特征值就是变化后的放缩值。

注意如何使用该特性对任意的矩阵进行幂运算。

