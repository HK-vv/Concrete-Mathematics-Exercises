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

### Chap 3

#### Ex 3.5

充要条件是$n\dec x<1$.

由于
$$
n\fl{x}=nx-n\dec x\\
\fl{nx}=nx-\dec{nx}
$$
故两者相等的充要条件是$n\dec x=\dec{nx}$.

进一步, 当$n\dec x<1$时, $\dec{nx}=\dec{n\dec x}=n\dec x$.

反之上式显然不成立.

#### Ex 3.10

首先
$$
\ce{\frac{2x+1}2}=\left\{\array{\fl x+1,\dec x\le\frac12\\\ce x+1,\dec x>\frac 12}\right.
$$
其次, 第二三项之和为0当且仅当$\frac{2x+1}4$为整数, 否则为-1. 其中$\frac{2x+1}4$为整数当且仅当$\dec x=\frac12$且$\fl x$为奇.

因此其总的作用为
$$
\left\{
\begin{array}{}
\fl x,\dec x<\frac12\\
\ce x,\dec x>\frac12\\
\fl x\text{和}\ce x\text{中的偶数}, \dec x=\frac12
\end{array}
\right.
$$

#### Ex 3.15

将原等式取负号
$$
-\fl{mx}=-\fl x-\fl{x+\frac 1m}-\cdots-\fl{x+\frac{m-1}m}\\
\ce{m(-x)}=\ce{-x}+\ce{-x-\frac 1m}+\cdots+\ce{-x-\frac{m-1}m}\\
$$
由于原式$x$取遍实数, 故用$x$代替$-x$, 即得
$$
\ce{mx}=\ce x+\ce{x-\frac 1m}+\cdots+\ce{x-\frac{m-1}m}
$$

#### Ex 3.20

令$a=\ce{\frac \alpha x}, b=\fl{\frac\beta x}$. 则其和为
$$
\begin{split}
&\sum_{k}[\alpha\le kx\le\beta]kx\\
=&\sum_{k}[\frac\alpha x\le k\le\frac\beta x]kx\\
=&\sum_k[a\le k\le b]kx\\
=&\frac{(a+b)(b-a+1)x}2
\end{split}
$$

#### Ex 3.25

直接证明$K_n>n$.

设$k\le n$时, 都有$K_k>k$. 由于
$$
2K_{\fl {n/2}}\ge2\fl {n/2}+2\ge n+1\\
3K_{\fl{n/3}}\ge3\fl{n/3}+3\ge n+1
$$
则$K_{n+1}=1+\min(2K_{\fl {n/2}},3K_{\fl{n/3}})\ge n+2>n+1$. 归纳得证.

#### Ex 3.30

归纳证明$X_n=\alpha^{2^n}+\alpha^{-2^n}$, 假设对$n$成立.

则$X_{n+1}=\alpha^{2^{n+1}}+\alpha^{-2^{n+1}}+2\alpha^{2^n}\alpha^{-2^n}-2=\alpha^{2^{n+1}}+\alpha^{-2^{n+1}}$, 归纳得证.

由于$\alpha^{-1}<1$, 故$\alpha^{-2^n}<1$. 又根据定义$X_n$总是整数, 所以$X_n=\ce{\alpha^{2^n}}$.

#### Ex 3.35

$$
\begin{split}
&\fl{(n+1)^2n!e}\mod n\\
=&\fl{\sum_{k\ge0}\frac{(n+1)^2n!}{k!}}\mod n\\
=&\sum_{0\le k<n}\frac{(n+1)^2n!}{k!}+(n+1)^2+(n+1)+\fl{\sum_{k>n+1}\frac{(n+1)^2n!}{k!}}\mod n\\
=&2\mod n
\end{split}
$$

其中$\sum_{k>n+1}\frac{(n+1)^2n!}{k!}<\sum_{k>0}\frac{n+1}{(n+2)^k}=1$, 故取整项为0.

#### Ex 3.40

注意到对于每个$k=(2l+1)^2$, 其位置都在$(l,l+1)$. 设$t=\sqrt k$, 那么容易得到从$k$起始的四条线段如下
$$
\begin{split}
n=[k,k+t](\fl{2\sqrt n}=4l):&(l,l+1)\sim(-l-1,l+1)\\
n=[k+t+1, k+2t+1](\fl{2\sqrt n}=4l+1):&(-l-1,l)\sim(-l-1,-l-1)\\
n=[k+2t+2, k+3t+2](\fl{2\sqrt n}=4l+2):&(-l,-l-1)\sim(l+1,-l-1)\\
n=[k+3t+3, k+4t+3](\fl{2\sqrt n}=4l+3):&(l+1,-l)\sim(l+1,l+1)
\end{split}
$$
设$k$为最大不大于$n$满足上述要求的整数. 注意到$\fl{\sqrt n/2}=l$, $\ce{m/2}=\ce{\fl {\sqrt n}/2}=l+1$, 且$(n-k)\text{mod}(t+1)$总是上述四条线段中和左端点的距离.

则$x(n)$可以写作
$$
x(n)=(-1)^{\ce{((\fl{2\sqrt n}\text{mod}4l)\text{mod}3)/2}}\bigg(-\big((n-k)\text{mod}(t+1)+1\big)[\fl{2\sqrt n}为偶]+\ce{\frac m2}\bigg)
$$
类似的, $y(n)$为
$$
y(n)=(-1)^{\fl{((\fl{2\sqrt n}\text{mod}4l)/2}}\bigg(-\big((n-k)\text{mod}(t+1)+1\big)[\fl{2\sqrt n}为奇]+\ce{\frac m2}\bigg)
$$
对第二问, 容易验证对前两条线段取-, 后两条线段取+, 因此可以写作$(-1)^{\fl{(\fl{2\sqrt n}\text{mod}4l)/2}+1}$.

#### Ex 3.45

若$m=2^x+2^{-(x+2)}$. 

归纳证明$Y_n=2^{2^nx+2^n-1}+2^{-(2^nx+2^n+1)}$, 设对$n$已成立.

则$Y_{n+1}=2Y_n^2-1=2(2^{2^{n+1}x+2^{n+1}-2}+2^{-(2^{n+1}x+2^{n+1}+2)}+1/2)-1=2^{2^{n+1}x+2^{n+1}-1}+2^{-(2^{n+1}x+2^{n+1}+1)}$.

因此$Y_n=\ce{2^{2^nx+2^n-1}}$.