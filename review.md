数学分析复习
==========

微积分
---

### 一元函数积分

* 第一换元法：（凑微分）$$\int{f[g(x)]dg(x)}=F[g(x)]+C$$ 从原积分函数中凑出一个因子，凑成等式左边的形式。

* 第二换元法：换元 $x=x(t)$，积分后再把x换回来。主要用于无理函数的积分中消去根号。有时使用三角函数换元来达到这个目的。

* 分部积分法：$$\int{udv}=uv-\int{vdu}$$ 可以很容易从$(uv)'=u'v+uv'$推出。

* 有理函数的积分：分解成最简真分式之和，方法为确定分母为一次或二次多项式的n次方，分子由待定系数确定，最高次数为多项式次数减一。

* 基本积分表：
  $$dtanx=\frac{1}{cos^2x}dx\\
  dcotx=-\frac{1}{sin^2x}dx\\
  dsecx=secxtanxdx\\
  dcscx=-cscxcotxdx\\
  darctanx=\frac{1}{1+x^2}dx\\
  darcsinx=\frac{1}{\sqrt{1-x^2}}dx$$

### 多元函数微分

* 偏导数、全微分
* 方向导数、梯度
  $$\nabla f=\{\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z}\}\\
  \frac{\partial f}{\partial l}=\nabla f\cdot\mathbf{l}$$
* 隐函数微分：求全微分
* 最优化问题
  * 无约束
     * 必要条件：各个一阶偏导数都等于0。即梯度为0。鞍点
  * 有约束
     * 拉格朗日乘数：构造辅助函数，必要条件为辅助函数梯度为0。

### 重积分

* 二重积分
  * 二重积分化累次积分，注意积分顺序可能影响很大。
  * 化极坐标二重积分，注意乘以雅可比行列式r
* 三重积分
  * 先单后重
  * 先重后单
  * 柱坐标系换元，雅可比行列式r
  * 球坐标系换元
    $$x=\rho sin\varphi cos\theta, y=\rho sin\varphi sin\theta,z=\rho cos\varphi$$
    雅可比行列式$\rho^2sin\varphi$
* 曲线积分
  * 第一类曲线积分
    有曲线C：$\mathbf{r}(t)=x(t)\mathbf{i}+y(t)\mathbf{j}+z(t)\mathbf{k}$，则
    $$\int_{C}{f(x,y,z)ds}=\int_{\alpha}^{\beta}{f(x(t),y(t),z(t))\sqrt{x'^2(t)+y'^2(t)+z'^2(t)}dt}$$
  * 第二类曲线积分
    向量值函数$\mathbf{F}(x,y)=P(x,y)\mathbf{i}+Q(x,y)\mathbf{j}$，则
    $$\int_L{\mathbf{F}\cdot d\mathbf{s}}=\int_L{Pdx+Qdy}=\int_\alpha^\beta{[P(x(t),y(t))x'(t)+Q(x(t),y(t))y'(t)]dt}$$
* 曲面积分
  * 第一类曲面积分
    有曲面S：$z=z(x,y),\space(x,y)\in D$，则，
    $$\iint_Sf(x,y,z)dS=\iint_D{f(x,y,z(x,y))\sqrt{1+p^2+q^2}dxdy},\\
    p=\frac{\partial z}{\partial x},q=\frac{\partial z}{\partial y}$$
  * 第二类曲面积分
    $$\iint_S{Pdydx+Qdzdx+Rdxdy}=\\\pm\iint_D{[P(x,y,z(x,y))\cdot(-z_x)+Q(x,y,z(x,y))\cdot(-z_y)+R(x,y,z(x,y))\cdot1]dxdy}$$
    也可以对不同的D分别求P、Q、R的积分，以避开复杂的求导
* 格林公式$$\iint_D(\frac{\partial Q}{\partial x}-\frac{\partial P}{\partial y})dxdy=\oint_LPdx+Qdy$$L是Q取正向的边界曲线。（内部区域在左手为正）
  计算面积：$$A=\frac12\oint_Lxdy-ydx$$
  用二重积分计算曲线积分
  利用保守场求曲线积分
* 散度$$div\mathbf{F}=\nabla\cdot\mathbf{F}=\frac{\partial P}{\partial x}+\frac{\partial Q}{\partial y}+\frac{\partial R}{\partial z}$$
* 高斯公式：$$\iiint_Vdiv\mathbf{F}=\iint_\Sigma{\mathbf{F}d\mathbf{S}}(环路积分)$$
* 旋度：$$rot\mathbf{F}=\left|\begin{array}{cccc}   
    \mathbf{i} & \mathbf{j} &  \mathbf{k}\\   
    \frac{\partial}{\partial x} & \frac{\partial}{\partial y} & \frac{\partial}{\partial z}\\   
    P& Q & R
\end{array}\right|$$
* 斯托克斯公式：$$\oint_L\mathbf{F}\cdot d\mathbf{l}=\iint_Srot\mathbf{F}\cdot d\mathbf{S}$$

级数
------

* 基本
  * 几何级数$$\sum_{n=1}^\infty{q^{n-1}}$$当$|q|<1$时收敛于$\frac{1}{1-q}$
  * 