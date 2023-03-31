$$
\def\lf{\lfloor}
\def\rf{\rfloor}
\def\lc{\lceil}
\def\rc{\rceil}
\def\fl#1{\lf{#1}\rf}
\def\ce#1{\lc{#1}\rc}
\def\dec#1{\{{#1}\}}
\def\C#1#2{\pmatrix{#1\\#2}}
\def\F#1#2#3{F\left(\begin{gathered}{#1}\\{#2}\end{gathered}\middle|\,{#3}\right)}
\def\fall#1{^{\underline{#1}}}
\def\rise#1{^{\overline{#1}}}
\def\bb#1#2{\left[\array{#1\\#2}\right]}
\def\Bb#1#2{\left\{\array{#1\\#2}\right\}}
\def\ab#1#2{\left<\array{#1\\#2}\right>}
\text{some pre-definition}
$$

### Chap 6

#### 6.5

$$
\begin{split}
U_n(x,y)=&\sum_{k\ge 1}\C nk\frac{(-1)^{k-1}}k(x+ky)^n\\
=&\sum_{k\ge 1}(\C{n-1}k+\C{n-1}{k-1})\frac{(-1)^{k-1}}k(x+ky)^{n-1}(x+ky)\\
=&xU_{n-1}(x,y)+(\frac xn+y)\sum_{k\ge 1}\C nk (-1)^{k-1}(x+ky)^{n-1}\\
=&xU_{n-1}(x,y)+(\frac xn+y)x^{n-1}
\end{split}
$$

因为 $\forall 0\le m<n,\ \sum_{k}\C nk(-1)^kk^m=(-1)^nn! \left\{\array{m\\n}\right\}=0$. (6.19)

求解递归只需要改写为
$$
\begin{split}
\frac1{x^n}U_n&=\frac1{x^{n-1}}U_{n-1}+\frac1n+\frac yx\\
&=U_0+\sum_{k=1}^n(\frac 1k+\frac yx)=H_n+\frac{ny}x
\end{split}
$$
所以$U_n(x,y)=x^nH_n+nx^{n-1}y$.

#### 6.10

由于$\lim_{n\rightarrow\infty}\frac{F_n}{F_{n-1}}=\phi$,  故$\phi$和一个所有位置都为1的连分式相等（$\lim_{n\rightarrow\infty}\frac{K_n(1,\dots)}{K_{n-1}(1,\dots)}$）.

#### 6.15

$$
\Delta^m(LHS)=\Delta^m(\sum_k\Bb nkx\fall k)=\sum_k\Bb nkk\fall mx\fall{k-m}\\
\Delta^m(RHS)=\sum_k\ab nk\frac{n\fall m(x+k)\fall{n-m}}{n!}=\sum_k\ab nk\C{x+k}{n-m}
$$

令x=0, 比较两式就得到$m!\Bb nm=\sum_k\ab nk\C k{n-m}$.

#### 6.20

$$
\sum_{k=1}^nH_k^{(2)}=\sum_{1\le j\le k\le n}\frac 1{j^2}=\sum_{1\le j\le n}\frac{n-j+1}{j^2}=(n+1)H_n^{(2)}-H_n
$$

#### 6.25

第n分钟后, 虫和终点得距离为$f(n)=n(100-H_n)$. 对其差分得到$\Delta f(x)=100-\frac{n}{n+1}-H_{n+1}$. 因此$f(n)-f(n-1)=\Delta f(n-1)=99-H_{n-1}$. 题目中描述的$n$和$N$大约是$e^{99-\gamma}$和$e^{100-\gamma}$.

#### 6.30

原式的证明十分直接, 只需要把两个$K_n$项按6.127式拆开即得证.
$$
\begin{split}
&K(x_1,\cdots,x_m+y,\cdots,x_n)\\
=&K(x_1,\cdots,x_m+y)K(x_{m+1},\cdots,x_n)+K(x_1,\cdots,x_{m-1})K(x_{m+2},\cdots,x_n)\\
=&(K(x_1,\cdots,x_m)+K(x_1,\cdots,x_{m-1})y)K(x_{m+1},\cdots,x_n)+K(x_1,\cdots,x_{m-1})K(x_{m+2},\cdots,x_n)\\
=&K(x_1,\cdots,x_n)+K(x_1,\cdots,x_{m-1})K(x_{m+1},\cdots,x_n)y

\end{split}
$$

#### 6.35

当$\frac 1n<\frac\varepsilon2$, 至少有一个$k$使得$H_k$落在$[\ce{H_n},\ce{H_n}+\varepsilon)$中.

#### 6.40

容易看到当n为奇
$$
\sum_{k=1}^{2n+1}\frac{(-1)^{-1}}k=H_{2n+1}-H_n=\sum_{k=n+1}^{2n+1}\frac 1k=\sum_{k=0}^{n}(\frac 1{k+n+1}+\frac 1{2n+1-k})=\sum_{k=0}^n\frac{3n+2}{(k+n+1)(2n+1-k)}
$$
 因此当$2n+1=1319$时, 其分子整除$3n+2=1979$. 

类似的, 当n为偶
$$
\sum_{k=1}^{2n}\frac{(-1)^{-1}}k=H_{2n}-H_n=\sum_{k=n+1}^{2n}\frac 1k=\sum_{k=0}^{n-1}(\frac 1{k+n+1}+\frac 1{2n-k})=\sum_{k=0}^n\frac{3n+1}{(k+n+1)(2n-k)}
$$
因此若$3n+1=1987$, 则需要$2n=1324$.

#### 6.45

设$X(\alpha,\beta,\gamma,\delta)_n=A\alpha+B\beta+C\gamma+D\delta$, 有下列方程
$$
X(0,1,0,0)_n=F_n\\
X(1,1,0,0)_n=F_{n+1}\\
X(0,1,-1,3)_n=n\\
X(1,1,0,-1)_n=1
$$
解得
$$
\begin{split}
A=&F_{n+1}-F_n\\
B=&F_n\\
C=&F_n+3F_{n+1}-n-3\\
D=&F_{n+1}-1
\end{split}
$$

#### 6.50

**a**.

$3|n\Leftrightarrow f(n)$是偶数.

归纳如下

若n是偶, 则由于$3|n/2$, 故$f(n)=f(n/2)$也是偶数;

若n是奇, 则有$(n-1)/2\mod 3=1$, 故$f(n)=f((n-1)/2)+f((n-1)/2+1)$也是偶数.

**b**.

若$n=(n_1,n_2,\cdots,n_k)_2$, 则$f(n)=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_k)$, $f(n+1)=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_k,\overline{n_k})$.

下面分别证明两式的递推关系

当n为奇, $n_k=1$, 
$$
\begin{split}
f(n)&=f((n-1)/2)+f((n-1)/2+1)\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1})+K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1},\overline{n_{k-1}})1\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_k)\\

f(n+1)&=f((n-1)/2+1)\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1},\overline{n_{k-1}})+K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1},\overline{n_{k-1}},n_k)0\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_k,\overline{n_{k}})

\end{split}
$$
当n为偶, $n_k=0$, 
$$
\begin{split}
f(n)&=f(n/2)\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1})+K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1},\overline{n_{k-1}})0\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_k)\\

f(n+1)&=f(n/2)+f(n/2+1)=f(n)+f(n/2+1)\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1},\overline{n_{k-1}},n_k)1+K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_{k-1},\overline{n_{k-1}})\\
&=K(n_1,\overline{n_1},n_2,\overline{n_2},\cdots,n_k,\overline{n_{k}})

\end{split}
$$

#### 6.55

首先对原式变形
$$
\begin{split}
\C km\C{x+k}k&=\C km\C{-x-1}k(-1)^k\\
&=\C{-x-1}m\C{-x-1-m}{k-m}(-1)^k\\
&=\C{-x-1}m\C{k+x}{k-m}(-1)^m\\
&=\C{x+m}m\C{k+x}{k-m}

\end{split}
$$
求和式即变为
$$
\sum_{0\le k<n}\C km\C{x+k}k=\C{x+m}m\sum_{k\le n-m-1}\C{k+m+x}{k}=\C{x+m}m\C{x+n}{n-m-1}
$$
把上式拆解开即是 (n>m+1)
$$
\begin{split}
&\frac{(x+1)\cdots(x+m)(x+m+2)\cdots(x+n)}{m!(n-m-1)!}\\
=&\frac{(x+1)\cdots(x+m)(m+1)(x+m+2)\cdots(x+n)}{n!}\frac{n!}{(m+1)!(n-m-1)!}\\
=&\frac{(x+1)\cdots(x+m)(m+1)(x+m+2)\cdots(x+n)}{n!}\C{n}{m+1}
\end{split}
$$
对x求导并令x=0即得式6.70如下
$$
\sum_{0\le k<n}\C kmH_k=\C n{m+1}(H_n-\frac{1}{m+1})
$$

#### 6.60

当n为奇
$$
(F_n+1)(F_n-1)=F_{n+1}F_{n-1}
$$
当n为偶
$$
(F_n+1)(F_n-1)=F_{n+2}F_{n-2}
$$
如若$F_n\pm 1$是素数, 在n足够大时, $\frac{F_{n+1}}{F_n\pm1}\approx\phi\approx1.618$, $\frac{F_{n+2}}{F_n\pm1}\approx\phi^2\approx2.618$. 意味着, 这两个比值一定处于一个小数的邻域内, 即不可能整除. 

对上面描述的“足够大”, 一个相当宽松的限制是$n>10$, 这时可以保证两个比值都不为整数. 验证$n\le 10$的所有情况, 为素数的只有$F_1+1,F_2+1,F_3+1,F_4-1,F_6-1$.

#### 6.65

等式左边就是
$$
\sum_kf(k)\int_{\sum_ix_i\in[k,k+1),x_i\in(0,1)}1dx_1\cdots dx_n
$$
因此我们实际上要证明$\int_{\sum_ix_i\in[k,k+1),x_i\in(0,1)}1dx_1\cdots dx_n=\ab nk/n!$.

上式左端用概率论语言讲, 若$x_1,\cdots,x_n$是在(0,1)上均匀分布的随机变量, 则$y=\sum_i x_i\in[k,k+1)$的概率就是上式.

设$y_j=\sum_{i=1}^jx_i$, 则$\{y_1\},\cdots,\{y_n\}$也是在[0,1)上均匀分布且独立的随机变量. 同时我们发现, $\fl{y_j}<\fl{y_{j+1}}\Leftrightarrow \{y_{j}\}>\{y_{j+1}\}$. 因此所描述的概率等于随机排列里有k个下降的概率, 即是$\ab nk/n!$.

#### 6.70

当$|z|<1$ 
$$
\begin{split}
\sum_{k\ge 1}(\frac 1k-\frac1{k+z})&=\sum_{k\ge 1}\frac 1k(1-\sum_{n\ge 0}(-1)^n\frac{z^n}{k^n})\\
&=\sum_{k\ge 1}\sum_{n\ge 2}(-1)^{n}\frac {z^{n-1}}{k^{n}}\\
&=\sum_{n\ge 2}(-1)^nH^{(n)}_\infty z^{n-1}

\end{split}
$$

#### 6.75

首先，定义二元奇偶函数分别满足如下等式
$$
odd:\ f(x,y)=-f(-x,-y)\\
even:\ f(x,y)=f(-x,-y)
$$
容易看到对任意变量求偏导交换函数奇偶性.

二元函数 $f(x,y)$ 的泰勒级数展开式为：$f(x,y) = \sum_{m=0}^\infty \sum_{n=0}^\infty \frac{1}{m!n!} \frac{\partial^{m+n} f}{\partial x^m \partial y^n}\bigg|_{(0,0)} x^my^n$. 因此奇函数的展开只有指标和为奇的项, 偶函数只有偶项. //

回到题目, 设$A(w,z)=\frac{\sin z}{\cos(w+z)},\ B(w,z)=\frac{\cos z}{\cos(w+z)},\ A+B=C=\sum c_{m,n}\frac{w^mz^n}{m!n!}$.

由于A奇B偶, 故A的幂级数展开只有指标和为奇的项, B的展开只有和为偶的项.

计算
$$
\begin{split}
\frac{\partial A}{\partial w}&=\frac{\sin(w+z)\sin z}{\cos^2(w+z)},\ 
\frac{\partial A}{\partial z}=\frac{\cos(w+z)\cos z+\sin(w+z)\sin z}{\cos^2(w+z)} \\
\frac{\partial B}{\partial w}&=\frac{\sin(w+z)\cos z}{\cos^2(w+z)},\ 
\frac{\partial B}{\partial z}=\frac{\sin(w+z)\cos z-\cos(w+z)\sin z}{\cos^2(w+z)}

\end{split}
$$
有$A(w,0)=0,\ B(0,z)=1$以及$(\frac{\partial }{\partial z}-\frac{\partial }{\partial w})A=B,\ (\frac{\partial }{\partial w}-\frac{\partial }{\partial z})B=A$.

根据上面四个观察以及A, B展开的形式可以得到

当m为奇, 有$c_{m,0}=0$, 当和为偶$c_{m,n+1}-c_{m+1,n}=c_{m,n}$;

当n为偶, 有$c_{0,n}=[n=0]$, 当和为奇$c_{m+1,n}-c_{m,n+1}=c_{m,n}$.

所以$c_{m,n}$刚好就得到了三角形第$(m+n)$行的第$(n+1)$个数. 其左侧序列$c_{m,0}$是$1/\cos z$的系数, 右侧$c_{0,n}$是正切数($+[n=0]$).


#### 6.80

关于$O(N\log N)$暴力...

正式的做法是, 首先考虑这样一个数列, 即反向斐波那契
$$
B_0=N,B_1=k\\B_n=B_{n-2}-B_{n-1}
$$
通过各种手段, 可以求得其通解为
$$
B_n=\frac{k+\hat\phi N}{\hat\phi-\phi}(-\phi)^n-\frac{k+\phi N}{\hat\phi-\phi}(-\hat\phi)^n
$$
那么$B_n>0$就等价于$(k+\hat\phi N)(-\phi)^n>(k+\phi N)(-\hat\phi)^n$.

1. 当$k>-\hat\phi N$, 上式等价于$(\frac{\phi}{\hat\phi})^{n}>\frac{k+\phi N}{k+\hat\phi N}$, 因此我们的目标就是令不等式右端尽量大, 因此取$k=\ce{-\hat\phi N}$.
2. 当$k<-\hat\phi N$, 上式等价于$(\frac{\phi}{\hat\phi})^{n}<\frac{k+\phi N}{k+\hat\phi N}$, 此时$k=\fl{-\hat\phi N}$.

因此, 我们只需分别计算$k$取$-\hat\phi N$最近两个整数所对应的结果, 取最好即可, 复杂度是$O(\log N)$.

对应原问题, $k=618034, x=154, y=144$, 题目中的$m=20$.

#### 6.85

#### 6.90