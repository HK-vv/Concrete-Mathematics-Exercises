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

### Chap 2

#### Ex 2.5

第二个等号把两个不相关的指标换成了相关的指标.

#### Ex 2.10

右边关于$u,v$也是对称的.
$$
\begin{split}
u\Delta v+Ev\Delta u=&u(x)(v(x+1)-v(x))+v(x+1)(u(x+1)-u(x))\\
=&-u(x)v(x)+v(x+1)u(x+1)+u(x+1)v(x)-u(x+1)v(x)\\
=&v(x)(u(x+1)-u(x))+u(x+1)(v(x+1)-v(x))\\
=&v\Delta u+Eu\Delta v
\end{split}
$$

#### Ex 2.15

注意到$n^2=2\sum_{1\le j\le k\le n}1-n$
$$
\begin{split}
&\sum_{k=1}^nk^3+\sum_{k=1}^nk^2\\
=&\sum_{1\le l\le n} l(2\sum_{1\le j\le k\le l}1-l)+\sum_{1\le k\le n} k^2\\
=&2\sum_{1\le j\le k\le l\le n}l\\
=&2\sum_{1\le k\le l\le n}kl\\
=&(\sum_{1\le k\le n}k)^2+\sum_{1\le k\le n}k^2\\
\end{split}
$$
因此$\sum_{k=1}^nk^3=(\sum_{k=1}^nk)^2=\frac 14n^2(n+1)^2$.

#### Ex 2.20

$$
\begin{split}
\sum_{k=1}^nkH_k=&nH_n+\sum_{k=1}^n(k-1)H_{k-1}\\
=&nH_n+\sum_{k=1}^nkH_k+H_n-n-\sum_{k=1}^nH_k\\
\end{split}
$$

因此$\sum_{k=1}^nH_k=nH_n+H_n-n$. 

下面直接求$\sum_{k=1}^nkH_k$.
$$
\begin{split}
\sum_{k=1}^n kH_k=&\sum_{1\le j\le k\le n} \frac kj\\
=&\sum_{1\le j\le n}\frac 1j\frac{(j+n)(n-j+1)}2\\
=&\sum_{1\le j\le n}\frac{-j^2+j+n(n+1)}{2j}\\
=&\square_nH_n-\frac 12\square_n+\frac n2
\end{split}
$$

#### Ex 2.30

令解集合为$S$, 下面证明存在一个一一映射$f:S\rightarrow T=\{(j,k)|j为奇,k为偶,jk=2100\}$.

映射方式为: 对每一种解, 若序列长度为$x$, 令$y=1050/x$为序列均值, $f(x,y)=\left\{\array{(2y,x),x为偶\\(x,2y), x为奇}\right.$.

考虑一个象$(j,k)$的原像如何, 有两种可能$f^{-1}(j,k)=\left\{\array{(x=k,y=j/2), j>k\\(x=j,y=k/2),k>j}\right.$, 其条件是根据序列项为正整数约束得到的. 注意到每个$(j,k)$都有原象且不交, 因此映射即单又满, 为双射.

分解$2100=2^2*3*5^2*7$. 因此$|T|=2*3*2=12$.

#### Ex 2.35

设$Q=\{2,3,4,5,\dots\}-P$, 根据定义, $T=\{x^n|x\in Q, n\ge 2\}=P$.

证明: $\forall k\in P$, 有唯一的$k=x^n$形式, 其中$x\in Q, n\ge 2$.

若$k=x^n$满足条件, 设$k$的素因子幂次序列为$<p_0,p_1,\cdots>$, $g=\gcd(p_0,p_1,\cdots)$. 则应有$n|g$. 因此$n=g$唯一.

否则若$nl=g\ (g,l>1)$, $x=k^{1/n}=k^{l/g}=(k^{1/g})^l$, 即$x\notin Q$.

因此有
$$
\begin{split}
\sum_{k\in P}\frac1{k-1}&=\sum_{k\in P}\frac1k\frac1{1-\frac1k}\\
&=\sum_{k\in P}\sum_{j\ge1}\frac1{k^j}\\
&=\sum_{x\in Q}\sum_{n\ge2}\sum_{j\ge1}\frac1{x^{nj}}\\
&=\sum_{l\ge2}\sum_{n\ge2}\frac1{l^n}\\
&=\sum_{l\ge2}\frac1{l(l-1)}\\
&=1
\end{split}
$$

### 