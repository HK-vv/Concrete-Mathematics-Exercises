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

### Chap7

#### 7.5

考虑到$\sum_k\C rk\C r{n-2k}=\sum_k(\C r{k/2}[2|k])\C r{n-k}$

所以$S(z)$就是$(1+z^2)^r=\sum_n\C r nz^{2n}=\sum_n\C r{n/2}z^n[2|n]$和$(1+z)^r=\sum_n\C rn z^n$的卷积, 故$S(z)=((1+z^2)(1+z))^r$.

#### 7.10

$$
\begin{split}
LHS&=\sum_k\C {-1/2+k}k\C{-1/2+n-k}{n-k}(H_{k-1/2}-H_{-1/2})\\
&=\sum_k\C{2k}k\C{2(n-k)}{n-k}(H_{k-1/2}-H_{-1/2})/2^{2n}\\
&=\sum_k\C{2k}k\C{2(n-k)}{n-k}(2H_{2k}-H_k)/2^{2n}\\

RHS&=H_n
\end{split}
$$

所以$4^nH_n=\sum_k\C{2k}k\C{2(n-k)}{n-k}(2H_{2k}-H_k)$.

#### 7.15

递归式$\bar\omega_{n+1}=\sum_k\C nk\bar\omega_{n-k}$的含义是枚举第$(n+1)$个元素所出现在子集的所有可能, 第$k$个求和项代表有$k$个元素和它分在一个子集的可能数.

求解递归式, 首先
$$
\begin{split}
P'(z)&=\sum_n\frac{\bar\omega_n}{(n-1)!}z^{n-1}\\
&=\sum_{n,k}\frac{\bar\omega_{n-1-k}}{(n-1-k)!}z^{n-1-k}\frac 1{k!}z^k\\
&=e^zP(z)
\end{split}
$$
添加条件$P(0)=1$, 解之得$P(z)=e^{e^z-1}$.

#### 7.20

$[z^n]az^kG^{(m)}(z)=a(n+(m-k))\fall mg_{n+(m-k)}$.

#### 7.25

其生成函数为
$$
G(z)=\sum_{n=0}^{m-1}\sum_k nz^{km+n}=\frac 1{1-z^m}\sum_{n=0}^{m-1}nz^n=\frac{P(z)}{Q(z)}
$$
其中$P(z)=\sum_{n=0}^{m-1}nz^n=\frac{(m-1)z^{m+1}-mz^m+z}{(1-z)^2}$, $Q(z)=1-z^m=\prod_{k=0}^{m-1}(1-\omega^kz)$.

根据7.29，有
$$
\begin{split}
n\ \text{mod}\ m=[z^n]G(z)&=\sum_{k=0}^{m-1}\omega^{kn}\frac{\omega^k\frac{m}{1-\omega^{-k}}}{m\omega^{(-k)(m-1)}}\\
&=\frac{m-1}2+\sum_{k=1}^{m-1}\frac{\omega^{kn}}{1-\omega^{-k}}
\end{split}
$$

#### 7.30

根据习题5.39给出的结论$(xy)^n=\sum_{k=1}^n\C{2n-1-k}{n-1}(a^nb^{n-k}x^k+a^{n-k}b^ky^k)$， 带入$x=\frac1{1-\alpha z}, y=\frac 1{1-\beta z}$就得到结果.

#### 7.35

**a**. 对其直接求和就有$\sum_{0<k<n}\frac1{k(n-k)}=\sum_{0<k<n}\frac 1n(\frac 1k+\frac 1{n-k})=\frac 2nH_{n-1}$.

**b**. 令$G(z)=\sum_{n>0}\frac 1nz^n=\ln \frac 1{1-z}$, 则所求就是$[z^n]G(z)^2=[z^n]\ln^2\frac 1{1-z}$.

对其求导就得到$(G(z)^2)'=2\frac1{1-z}\ln\frac1{1-z}=2\sum_{n>0}H_nz^n$. 

所以$[z^n]G(z)^2=[z^{n-1}](G(z)^2)'/n=\frac 2nH_{n-1}$.

#### 7.40

$\sum_k\C nkk¡=n!$.

#### 7.45
#### 7.50
#### 7.55