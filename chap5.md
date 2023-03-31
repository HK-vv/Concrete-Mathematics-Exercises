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
\text{some pre-definition}
$$

### Chap 5

#### 5.5

由于$\C pk=\frac{p^{\underline k}}{k!}$为整数, 且$k<p$. 有$p\nmid k!$, 所以$p|\C pk$.

考虑$\C pk=\C {p-1}{k}+\C {p-1}{k-1}$, 又$\C {p-1}0=1$. 有$\C {p-1}k\equiv (-1)^k\pmod p$.

#### 5.10

展开得到$2\sum_{k\ge 0}\frac{z^k}{(k+2)}$, 其项间的比值为$\frac{(k+2)z}{k+3}$是关于$k$的有理函数.

另外, 原式即是$\F{2,1}{3}z$.

#### 5.15

若$n$为奇, 则原式直接为0.

反之若$n=2m$, 根据公式(5.29)就有$\sum_k\C{2m}{m+k}^3(-1)^k=(-1)^m\frac{(3m)!}{(m!)^3}$.

#### 5.20

观察其相邻项之比, $\frac{t_{k+1}}{t_k}=\frac{(a_1-k)\dots(a_m-k)z}{(b_1-k)\dots(b_n-k)(k+1)}=\frac{(k-a_1)\dots(k-a_m)(-1)^{n+m}z}{(k-b_1)\dots(k-b_n)(k+1)}$.

由于在此定义下F和G的$t_0$相同, 故有$G=\F{-a_1,\cdots,-a_m}{-b_1,\cdots,-b_n}{(-1)^{n+m}z}$.

#### 5.25

直接证明等式两边的展开项相等.
$$
\begin{split}
&a_1\frac{(a_1+1)^\overline k\cdots}{(b_1+1)^{\overline k}\cdots}-b_1\frac{a_1^{\overline k}\cdots}{b_1^{\overline k}\cdots}\\
=&(a_1+k)\frac{a_1^{\overline k}\cdots}{(b_1+1)^{\overline k}\cdots}-(b_1+k)\frac{a_1^{\overline k}\cdots}{(b_1+1)^{\overline k}\cdots}\\
=&(a_1-b_1)\frac{a_1^{\overline k}\cdots}{(b_1+1)^{\overline k}\cdots}
\end{split}
$$
另一些超几何函数也有类似的公式, 使用相同的技巧可以证明$(a_1-a_2)\F{a_1,a_2,\cdots}{\cdots}z=a_1\F{a_1+1,a_2,\cdots}{\cdots}z-a_2\F{a_1,a_2+1,\cdots}{\cdots}z$.

#### 5.30

将左边和右边的项做对比有$\frac{(k+1)a_1^{\overline k}\cdots a_m^{\overline k}z^k}{b_1^{\overline k}\cdots b_n^{\overline k}k!}=z^k$. 显然满足的超几何函数为$\F{1,1}{2}z$.

#### 5.35

**a**. 

其中$\sum_{k\le n}\C nk2^k$的组合解释是: 将n个方格涂成三种颜色的方法数, 即是$3^n$. 所以答案为$(\frac 32)^n$, 仅当$n\ge 0$成立.

**b**. 
$$
\begin{split}
\sum_{n\ge k}\C nk2^{k-n}=&\sum_{n\ge k}\C{n}{n-k}2^{k-n}\\
=&\sum_{n\ge k}\C{-k-1}{n-k}(-\frac 12)^{n-k}\\
=&\sum_{n\ge 0}\C{-k-1}{n}(-\frac 12)^{n}\\
=&(\frac 12)^{-k-1}=2^{k+1}
\end{split}
$$
仅当$k\ge 0$成立.

#### 5.40

$$
\begin{split}

&\sum_{j=1}^m(-1)^{j+1}\C rj\sum_{k=1}^n\C{-j+rk+s}{m-j}\\
=&(-1)^{m+1}\sum_{k=1}^n\sum_{j=1}^m\C rj\C{m-rk-s-1}{m-j}\\
=&(-1)^{m}\sum_{k=1}^n(\C{m-rk-s-1}m-\C{m-r(k-1)-s-1}{m})\\
=&(-1)^m(\C{m-rn-s-1}m-\C{m-s-1}m)\\
=&\C{rn+s}m-\C sm
\end{split}
$$

#### 5.45

$\sum_{k\le n}\C{2k}k4^{-k}=\sum_{k\le n}\C{k-1/2}{k}=\C{n+1/2}n$.

#### 5.50

要证明: $\frac{1}{(1-z)^a}\F{a,b}c{\frac{-z}{1-z}}=\F{a,c-b}cz$.
$$
\begin{split}
LHS=&\sum_{k\ge 0}\frac{a^{\overline k}b^{\overline k}}{c^{\overline k}k!}\frac{(-z)^k}{(1-z)^{k+a}}\\
=&\sum_{k\ge 0}\frac{a^{\overline k}b^{\overline k}}{c^{\overline k}k!}(-z)^k\sum_j\C{-k-a}j(-z)^j\\
=&\sum_{k\ge 0}\frac{a^{\overline k}b^{\overline k}}{c^{\overline k}k!}(-z)^k\sum_{j\ge0}\C{j+k+a-1}jz^j\\
\end{split}
$$
其系数就为
$$
\begin{split}
[z^n]LHS=&\sum_{0\le j\le n}(-1)^j\frac{a^{\overline j}b^{\overline j}}{c^{\overline j}j!}\C{n+a-1}{n-j}\\
=&\sum_{0\le j\le n}(-1)^j\frac{a^{\overline j}b^{\overline j}}{c^{\overline j}j!}\frac{(a+j)^{\overline{n-j}}}{(n-j)!}\\
=&\frac{a^\overline n}{n!}\sum_{0\le j\le n}\frac{b^{\overline j}(-n)^\overline j}{c^{\overline j}j!}\\
=&\frac{a^\overline n}{n!}\F{b,-n}c1\\
=&\frac{a^{\overline n}(c-b)^{\overline n}}{c^{\overline n}n!}=[z^n]RHS

\end{split}
$$

#### 5.55

只考虑对所有$t$, 有$t(k),T(k)\ne0$的情况.

由于
$$
t(k)=cT(k)(\frac{(k+A_1)\cdots Z}{(k+B_1)\cdots(k+1)}-1)\\

\frac{t(k)}{T(k)}=(\frac zZ)^k\frac{a_1\rise k\cdots a_m\rise k B_1\rise k\cdots B_N\rise k}{b_1\rise k\cdots b_n\rise k A_1\rise k\cdots A_M\rise k}=C(\frac zZ)^k\frac{(a_1+k)!\cdots(B_1+k)!\cdots}{(b_1+k)!\cdots(A_1+k)!\cdots}=C(\frac zZ)^k(k!)^{m+N-M-n}r(k)
$$
其中$r(k)$是某个有理函数. 整合上面两式有$c(\frac{(k+A_1)\cdots Z}{(k+B_1)\cdots(k+1)}-1)=(\frac zZ)^k(k!)^{m+N-M-n}r(k)$.

考虑极限$c=\lim_{k\rightarrow\infty}\frac{(\frac zZ)^k(k!)^{m+N-M-n}}{R(k)}$, 显然只有在$m+N-M-n=0$且$\frac zZ=1$时成立, 得证.

#### 5.60

$\C{m+n}n\sim\sqrt{\frac{m+n}{2\pi mn}}\frac{(m+n)^{m+n}}{m^mn^n}$.

$m=n$时, $\C{2n}n\sim 4^n\sqrt\frac 1{\pi n}$. 这也意味着$\C{n-1/2}n\sim\sqrt\frac 1{\pi n}$.

#### 5.65

$$
\begin{split}
\sum_k \C{n-1}kn^{-k}(k+1)!=&\sum_{0\le k\le n-1}\frac{(n-1)!n^{-k}(k+1)}{(n-k-1)!}\\
=&(n-1)!\sum_{0\le k\le n-1}\frac{n^{k+1-n}(n-k)}{k!}\\
=&(n-1)!\sum_{0\le k\le n-1}\frac{n^{(k+1)-n+1}}{k!}-\frac{n^{k-n+1}}{(k-1)!}\\
=&(n-1)!\frac n{(n-1)!}=n
\end{split}
$$

#### 5.70

观察到原式即是$\F{-n,1/2}{1}{2}$. 为了将z转化为已知结果的形式, 将$k$换为$n-k$, 原式就是$(-2)^{-n}\C{2n}n\F{-n,-n}{1/2-n}{\frac 12}$. 再应用高斯恒等式, 其中的超几何函数就变为$\F{-n/2,-n/2}{1/2-n}1=\frac{\Gamma(1/2)\Gamma(1/2-n)}{\Gamma((1-n)/2)^2}$. 当n为奇数时, 原式为0, 否则为$2^{-n}\C{2n}n\frac{\Gamma(1/2)\Gamma(1/2-n)}{\Gamma((1-n)/2)^2}$.

#### 5.75

首先有$S_0+S_1+S_2=2^n$, 其次根据加法公式有$S_i(n)=S_i(n-1)+S_{i-1}(n-1)$.

容易归纳证明：对固定n, $\{S_i(n),i=1,2,3\}$中必有两项相等，且不等项之间差为1. 令$s=\min_iS_i(n)$, 则$2^n=3s+c$, 其中$c\in\{1,2\}$. 因此$s=\fl{2^n/3}$. 这就说明$S_i(n)$只能是$\fl{2^n/3}或者\ce{2^n/3}$.

具体的对应关系是：当n为偶时$S_{n/2\ \text{mod}\ 3}(n)=\ce{2^n/3}$, 为奇时$S_{(n-3)/2\ \text{mod}\ 3}(n)=\fl{2^n/3}$.

#### 5.80

观察到斯特林近似提供的不等式$n!\ge (\frac ne)^n$（此式容易通过两边取对数证明）, 就得到$\C nk\le\frac{n^k}{(\frac ke)^k}=(en/k)^k$. 

#### 5.85

只要证明：若$f$是一个次数不大于$n$的多项式，且$a_i$为它次数为$i$的系数，则
$$
\sum_{0\le\varepsilon_1,\cdots,\varepsilon_n\le 1}(-1)^{\sum\varepsilon_i}f(\sum\varepsilon_ix_i)=(-1)^nn!a_n\prod x_i
$$
对$n$归纳：假设小于$n$的情况正确，设$g(x)=(f(x)-a_0)/x$是$n-1$阶多项式.
$$
\begin{split}
LHS=&\sum_\varepsilon(-1)^{\sum\varepsilon_i}g(\sum\varepsilon_ix_i)(\sum\varepsilon_ix_i)\\
=&\sum_j\sum_{\varepsilon}(-1)^{\sum\varepsilon_i}g(\sum\varepsilon_ix_i)\varepsilon_jx_j\\
=&\sum_j\sum_{\varepsilon}(-1)^{1+\sum_{i\ne j}\varepsilon_i}g(x_j+\sum_{i\ne j}\varepsilon_ix_i)x_j\\
=&\sum_j(-1)^{n}(n-1)!a_n\prod x_i=(-1)^nn!a_n\prod x_i
\end{split}
$$
要证明的式子是$f(x)=\C{x+2^n}n$，$x_i=i^3$的情况.

#### 5.90

这个和式就等于$\F{-r,1}{-s}1$. 根据书中结果, 当s是非负整数或者$r-s>1$时，此式就为$\frac{\Gamma(-s+r-1)\Gamma(-s)}{\Gamma(-s+r)\Gamma(-s-1)}$. 其他情况则不收敛.

#### 5.95

添加条件有二: $p\bot q,p\bot r$, 且$p,r$的最高项系数为1. 第一个条件的限制直观上是为了让gosper过程中从$q,r$中消去对应因子时总选择最近得两个根. 下证明唯一性

如果有两组函数满足条件，分别为$p_1,q_1,r_1$和$p_2,q_2,r_2$, 令$P_1=p_1/\gcd(p_1,p_2),P_2=p_2/\gcd(p_1,p_2)$. 就有
$$
P_1(k+1)q_1(k)P_2(k)r_2(k+1)=P_1(k)r_1(k+1)P_2(k+1)q_2(k)
$$
如果有$P_1(x)=0$, 那么分别带入$x$和$x-1$, 可以得到$P_1(x+1)r_2(x+1)=P_1(x-1)q_2(x-1)=0$, 这是因为$q_1(x), r_1(x), P_2(x)$都不为0. 进一步，总能找到整数$\alpha,\beta\ge0$使得$P_1(x+\alpha)=P_1(x-\beta)=0$且$P_1(x+\alpha+1),P_1(x-\beta-1)\ne 0$, 这就意味着$r_2(x+\alpha+1)=q_2(x-\beta-1)=0$, 和原条件矛盾. 所以$p_1=p_2$. 

$p$一旦唯一确定, 则$q,r$也随之确定, $\frac{q(k)}{r(k+1)}=\frac{t(k+1)p(k)}{t(k)p(k+1)}$，且$q(k)\bot r(k+1)$. 否则有$(k+\alpha)|q,(k+\alpha-1)|r$和原条件矛盾.

#### 5.100

使用Zeilberger扩展的Gosper算法，我们得到$(n+2)\sum_{0\le k<n} 1/\C nk-(2n+2)\sum_{0\le k<n}1/\C{n+1}k=-n$, 用$S_n$表达就得到递归式$(2n+2)S_{n+1}=(n+2)S_n+(2n+2)$. 

两边同乘$\frac{2^{n}}{(n+1)(n+2)}$, 为$2^{n+1}S_{n+1}/(n+2)=2^nS_n/(n+1)+2^{n+1}/(n+2)$, 就得到$S_n=2^{-n}(n+1)(1+\sum_{k=1}^n2^k/(k+1))$.

#### 5.105

g