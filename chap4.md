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

### Chap 4

#### Ex 4.5

容易归纳
$$
L^k=\left[\matrix{1&k\\0&1}\right]\\
R^k=\left[\matrix{1&0\\k&1}\right]
$$


#### Ex 4.10

$$
\phi(999)=999(1-\frac1{3})(1-\frac1{37})=648
$$

#### Ex 4.15

不能, 至少不包含5.

因为容易验证若$5\nmid e_{n-1}$, 则$5\nmid e_n=e_{n-1}^2-e_{n-1}+1$. 

#### Ex 4.20

令$a_{k+1}$是$(2^{a_k},2^{a_k+1})$中的某个素数, $a_1=2$. 则$b=\lim_{n\rightarrow \infty}\log^{(n)} a_n$.

1. 容易验证此极限收敛. 因为
   $$
   \begin{split}
   
   \log^{(n)}a_n<\log^{(n+1)}a_{n+1}<\log^{(n)}(a_n+1)<\log^{(n)}a_n+r^n
   
   \end{split}
   $$
   其中$r<1$. 因此$|\log^{(n+k)}a_{n+k}-\log^{(n)}a_n|<\frac{r^n(1-r^k)}{1-r}$.

2. 归纳即可证明: $a_k<\log^{(d)}a_{k+d}<a_k+1$, 这说明$\fl{\exp_2^{(k)}b}=a_k$. 

   因为当对上式中的d取极限, 有$a_k<\exp_2^{(k)}a_k<a_k+1$.

#### Ex 4.25

**a**.

'$\Rightarrow$': $km/gcd(k,m)|n$, 即$km|n$; 由于$k\bot n/(km)$且$m\bot n/(km)$, 故$km\bot n/(km)$.

'$\Leftarrow$': 直接有$k|n, m|n$; 另外由于$km\bot n/(km)$, 且$k\bot m$, 有$k\bot n/k,\ m\bot n/m$.

**b**.

错误的. 考虑$(m,n)=(12,18)$.

#### Ex 4.30

当$m_1\bot m_2$, 存在一个双射$f:[m_1m_2]\rightarrow[m_1]\times[m_2], f(x)=(x\mod m_1,x\mod m_2)$. 

这是因为两个域大小相等, 且若有$f(x_1)=f(x_2)$, 则$(x_1-x_2)|m_1m_2$, 即$x_1\equiv x_2\pmod{m_1m_2}$.

(注意这里集合$[n]$里面的每个元素代表一个剩余系)

因此可以归纳得到存在一个双射$g:[m]\rightarrow [m_1]\times[m_2]\times\cdots[m_r]$, 得证.

#### Ex 4.35

令$r_1=m\mod n,\ r_2=n\mod m$, 则

$I(m,n)=\left\{\array{I(r_1,n),\ m>n\\I(m,r_2)-\fl{n/m}I(r_2,m),\ m<n}\right.$

边界条件是$I(k,0)=1,\ I(0,k)=0$. ($k>0$).

#### Ex 4.40

观察到若一个正整数$n=(a_m,\cdots,a_1,a_0)_p$, 且$k$是最小使得$a_k\neq0$, 则$\varepsilon_p(n)=k$. 且$n/p^{\varepsilon_p(n)}\equiv a_k\pmod p$.

首先对$k$归纳证明$(mp^k)!/p^{\varepsilon_p((mp^k)!)}\equiv (-1)^{\varepsilon_p((mp^k)!)}m!\pmod p$. ($0\le m<p$)

当$k=0$时, 显然正确.

当$k<n$成立,
$$
\begin{split}
&(mp^{n})!/p^{\varepsilon_p(mp^{n})!}\\
\equiv& m!((p^{n}-1)!)^m\\
\equiv& m!(\prod_{i=0}^{n-1}((p-1)p^i)!)^m\\
\equiv& m!(\prod_{i=0}^{n-1}(-1)^{\varepsilon_p(((p-1)p^i)!)}(p-1)!)^m\\
\equiv& m!(\prod_{i=0}^{n-1}(-1)^{\varepsilon_p(((p-1)p^i)!)}(-1))^m\\
\equiv& m!(-1)^{\varepsilon_p((mp^n)!)}\pmod p
\end{split}
$$
因此, 对任意数$n=(a_m,\cdots,a_1,a_0)_p$, 有
$$
\begin{split}
n!/p^{\varepsilon_p(n!)}&\equiv \prod_{i=0}^m (a_i(p^k))!/p^{\varepsilon_p((a_i(p^k))!)}\\
&\equiv \prod_{i=0}^m (-1)^{\varepsilon_p((a_i(p^k))!)}a_i!\\
&\equiv (-1)^{\varepsilon_p(n!)}\prod_{i=0}^m a_i!\pmod p
\end{split}
$$

#### Ex 4.45

总有2个.

首先, 对于n=1, 只有5和6成立.

假设n=k时数m满足条件, 且以 a=5或6 结尾, 则考虑新的一位需要满足的条件为$(2a-1)x\equiv C\pmod {10}$, 其中这里的C等于$m^2$在第k+1位的大小.

观察上面的需要满足的等式, 对a=5和6, 分别可以改写为
$$
x\equiv C\\
x\equiv -C
$$
因此对任意C, 总有且恰有一个数字(<10)满足条件. 得证.

值得一提的是，由于这里的C可能为0，所以得到的n位数并不总是以非0位起始.

#### Ex 4.50

**a**.
$$
\begin{split}

z^m-1&=\prod_{0\le k<m}(z-w^k)\\
&=\prod_{d|m}\ \prod_{0\le k<m,\ \gcd(k,m)=d} (z-w^k)\\
&=\prod_{d|m}\ \prod_{0\le k<m/d,\ k\bot m/d} (z-w^{kd})\\
&=\prod_{d|m}\ \prod_{0\le k<d,\ k\bot d} (z-w^{km/d})\\
&=\prod_{d|m}\ \psi_d(z)

\end{split}
$$

**b**.

对$f(n)=\log (z^n-1),\ g(n)=\log\psi_n(z)$.

由于$f(m)=\sum_{d|m}g(d)$, 反演得到$g(m)=\sum_{d|m}\mu(m/d)f(d)$, 即$\psi_m(z)=\prod_{d|m}(z^d-1)^{\mu(m/d)}$.

#### Ex 4.55

归纳证明一个更强的结论: $\frac{P_{2n}}{P_n^4(n+1)}$是整数.

容易验证$n=1$时上式等于2.

由于
$$
\frac{P_{2(n+1)}}{P_{n+1}^4(n+2)}=\frac{P_{2n}(2n+1)!(2n+2)!}{P_n^4((n+1)!)^4(n+2)}
$$
假设$\frac{P_{2n}}{P_n^4(n+1)}$是整数, 只需证明$\frac{(2n+1)!(2n+2)!(n+1)}{((n+1)!)^4(n+2)}$是整数.

变形得
$$
\frac{(2n+1)!(2n+2)!(n+1)}{((n+1)!)^4(n+2)}=\frac{(2n+2)!}{((n+1)!)^2(n+2)}\frac{(2n+2)!}{2((n+1)!)^2}=C_{n+1}\cdot\pmatrix{2n+1\\n}
$$
其中卡特兰数$C_k:=\pmatrix{2k\\k}/(k+1)$总是整数, 因为其有组合解释.

#### Ex 4.60

给定$\theta=2/3$, 设$p_1$对$\theta$充分大, $p_{n+1}$是大于$p_n^3$得最小素数, 令$a_n=3^{-n}\ln p_n,b_n=3^{-n}\ln (p_n+1)$, 则$P=\lim_{n\rightarrow\infty}e^{a_n}$.

证明之前首先观察到一个性质: $p_{n+1}<(p_{n}+1)^3$. 这是因为若非, 则最大的素数$q<p_n^{3}$满足$q+q^\theta>(p_n+1)^3$. 这就导出$-2q^{2/3}+3q+1<0$, 矛盾.

1. 证明此极限收敛.

   由于$p_n^{3^{-n}}<e^{a_{n+1}}<(p_n+1)^{3^{-n}}$, $|e^{a_{n+1}}-e^{a_n}|<r^n$, 其中$r<1/3$.

2. 证明$\fl{P^{3^n}}=p_n$. 只要证$p_n\le p_{n+k}^{3^{-k}}<p_n+1$.

   由于$p_{n+k+1}^{3^{-k-1}}-p_{n+k}^{3^{-k}}<(p_{n+k}+1)^{3^{-k}}-p_{n+k}^{3^{-k}}<3^{-k-1}$, 因此$p_{n+k}^{3^{-k}}=p_n+\sum_{i=0}^{k-1} 3^{-i-1}<p_n+1$.