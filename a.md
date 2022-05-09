# Answer

## 1.

### (a)

Use the substitution $x=cos\theta$, we get $dx=-sin(\theta)$ and
$$
\begin{align*}
\frac{2}{\pi}\int_{-1}^1\frac{T_m(x)T_n(x)}{\sqrt{1-x^2}}dx
&=\frac{2}{\pi}\int_{\pi}^0 \frac{\cos(m\theta)\cos(n\theta)}{\sin(\theta)}(-\sin(\theta)d\theta\\
&=\frac{1}{\pi}\int_{0}^\pi [\cos((m+n)\theta)+\cos((m-n)\theta)]d\theta\\
&=\begin{cases}1, & \text{if } m=n,\\ 0, & \text{otherwise}\end{cases}
\end{align*}
$$
because $\int_0^\pi cos(k\theta)d\theta=\begin{cases}0, & \text{if} \ k\neq 0\\ \pi, & \text{if} \ k= 0\end{cases}$   for any integer $k$.

### (b)

$$
\begin{aligned}
R_N
&=\frac{2}{\pi}\int_{-1}^1 \frac{[f(x)-\sum_{n=0}^N \kappa_n c_n T_n(x)]^2}{\sqrt{1-x^2}}dx\\
&=\frac{2}{\pi}\int_{-1}^1 \frac{f^2(x)}{\sqrt{1-x^2}}dx
-\frac{4}{\pi}\sum_{n=0}^N \kappa_n c_n\int_{-1}^1 \frac{f(x) T_n(x)}{\sqrt{1-x^2}}dx
+\sum_{n=0}^N \sum_{m=0}^N \kappa_n c_n \kappa_m c_m\frac{2}{\pi}\int_{-1}^1 \frac{T_m(x)T_n(x)}{\sqrt{1-x^2}}dx
\end{aligned}
$$

Using the result of (a), the last term equals $\sum_{n=0}^N  \kappa_n c_n^2$. Thus
$$
\frac{\partial R_N}{\partial c_j}=2\kappa_j(-\frac{2}{\pi}\int_{-1}^1\frac{T_j(x)f(x)}{\sqrt{1-x^2}}dx+c_j), \ j=0,1,\cdots
$$
If 
$$
c_j=\frac{2}{\pi}\int_{-1}^1\frac{T_j(x)f(x)}{\sqrt{1-x^2}}dx,
$$
 then 
$$
\frac{\partial R_N}{\partial c_j}=0.
$$
 As 
$$
\frac{\partial^2 R_N}{\partial^2 c_j}=2\kappa_j>0, \  j=0,1,\cdots
$$
a minimum of the residual is reached.

### (c)

From Problem 6.5, we know that
$$
T_{n}(x)-2xT_{n+1}(x)+T_{n+2}(x)=0, \ n\geq 0.
$$
Thus $T_0(x)=1, T_1(x)=x, T_2(x)=2x^2-1$ and
$$
T_{n-2}(x)-2xT_{n-1}(x)+T_{n}(x)=0, \ n>1.
$$
So
$$
\begin{aligned}
S_N(x)
&=\frac{1}{2}c_0+\sum_{n=1}^N c_nT_n(x)\\
&=\frac{1}{2}[b_0(x)-2xb_{n1}(x)+b_2(x)]+\sum_{n=1}^N [b_{n}(x)-2xb_{n+1}(x)+b_{n+2}(x)]T_n(x)\\
&=\frac{1}{2}[b_0(x)+b_2(x)]-xb_1(x)+\sum_{n=1}^N b_{n}(x)T_n(x)-\sum_{n=1}^N 2xb_{n+1}T_n(x)+\sum_{n=1}^N b_{n+2}(x)T_n(x).\\
\end{aligned}
$$
The last three terms can be transformed into 
$$
\begin{aligned}
\sum_{n=1}^N b_{n}(x)T_n(x)&=xb_1(x)+(2x^2-1)b_2(x)+\sum_{n=3}^N b_{n}(x)T_n(x);\\
\sum_{n=1}^N 2xb_{n+1}T_n(x)&=2x^2b_1(x)+\sum_{n=3}^N 2xb_{n}(x)T_{n-1}(x);\\
\sum_{n=1}^N b_{n+2}(x)T_n(x)&=\sum_{n=3}^N b_{n}(x)T_{n-2}(x).\\
\end{aligned}
$$
Therefore
$$
\begin{aligned}
S_N(x)
&=\frac{1}{2}[b_0(x)-b_2(x)]+\sum_{n=3}^N b_{n}(x)[T_{n-2}(x)-2xT_{n-1}(x)+T_{n}(x)]\\
&=\frac{b_0(x0)-b_2(x)}{2}.
\end{aligned}
$$

## 2

### (a)

#### (i)

$C_5$ rule uses nodes at which $T_4(t)=8t^4-8t^2+1=\pm 1$. Thus the nodes are
$$
t_1=-1, t_2=-\frac{\sqrt{2}}{2},t_3=0,t_4=\frac{\sqrt{2}}{2},t_5=1.
$$
Suppose polynomials of degree less than five are integrated exactly, then 
$$
\sum_{q=1}^5 \omega_qt_q^i=\int_{-1}^1 t^i=
\begin{cases}
\frac{2}{i+1},&i=0,2,4\\
0,&i=1,3.
\end{cases}
$$
This leads to  5 equations. By solving this equation group, we get
$$ {1}
\omega_1=\omega_5=\frac{1}{15}, \omega_2=\omega_4=\frac{8}{15},\omega_3=\frac{4}{5}.
$$ {1}



#### (ii)

$$
\begin{aligned}
S_p
&=1+(-1)^p-(p+1)[\omega_1(-1)^p+\omega_2(-\frac{\sqrt{2}}{2})^p+\omega_2(\frac{\sqrt{2}}{2})^p+\omega_1]\\
&=\big[ 1+(-1)^p \big] \bigg[ 1-(p+1)\big(\omega_1+2^{-\frac{p}{2}}\omega_2 \big) \bigg]\\
&=\big[ 1+(-1)^p \big] \bigg[ 1-(p+1)\bigg(\frac{1}{15}+2^{-\frac{p}{2}}\frac{8}{15}  \bigg) \bigg]\\
&=\big[ 1+(-1)^p \big] \bigg[ 1-\frac{p+1}{15}\bigg(1+2^{3-\frac{p}{2}} \bigg) \bigg]\\
\end{aligned}
$$

Then $S_6=\frac{2}{15}$ is the first nonzero coefficient.

#### (iii)

For $C_{5}$ rule,  define $\Delta t_j=t_{j+1}-t_j, j=1,2,...$ and $t_j^*$ as  the length  and the midpoint of the $j$-th interval  . The error is
$$
E_j = \sum_{p=0}^\infty \Big(\frac{\Delta t_j}{2} \Big)^{p+1}\frac{f^{(p)}(t_j^*)}{(p+1)!} S_p
\approx \frac{2}{15} \Big(\frac{\Delta t_j}{2} \Big)^{7}\frac{f^{(6)}(t_j^*)}{7!}
$$
with $\Delta t_j=1-\frac{\sqrt{2}}{2}$ or $ \frac{\sqrt{2}}{2} $.

For five-point Newton-Cotes rule, $S_6=-\frac{1}{3}$ . The error is
$$
E_j \approx -\frac{1}{3} \Big(\frac{\Delta t_j}{2} \Big)^{7}\frac{f^{(6)}(t_j^*)}{7!}
$$
with $\Delta t_j=\frac{1}{2}$ .

So the error of five-point Newton-Cotes rule is expected to be 2.5 times  that of $C_5$ rule.



#### (iv)

$C_9$ rule uses nine nodes at which $T_8(t)=\pm 1$. For the five nodes computed in (i),
$$
T_8(t_j)=\cos(8\acos(t_j))=2\cos^2(4\acos(t_j))-1=2T_4^2(t_j)-1=1.
$$
So only four more nodes are needed to for evaluation in each subinterval. Totally $4N$ evaluations are required.

### (b)

#### (i)

The left hand side is
$$
\begin{aligned}
\int_{-1}^{1}g(t)dt
&=\int_{-1}^{1}T_{2j}(t)dt\\
&=\int_{0}^{\pi}T_{2j}(\cos \theta)\sin \theta d\theta\\
&=\int_{0}^{\pi}\cos (2j\theta)\sin \theta d\theta \\
&=\frac{1}{2}\int_{0}^{\pi} \Big[\sin \big((2j+1)\theta\big)-\sin \big((2j-1)\theta\big) \Big]d\theta \\
&=\frac{1}{2j+1}-\frac{1}{2j-1}.
\end{aligned}
$$
$T_{n-1}(t_q)=\cos((n-1) \acos(t_q))=\pm 1$  implies
$$
(n-1)\acos(t_q)=(q-1)\pi, q=1,2,...n.
$$


So the right hand side is
$$
\sum_{q=1}^n \omega_q T_{2j}(t_q)=\sum_{q=1}^n \omega_q \cos(2j\acos (t_q))=\sum_{q=1}^n \omega_q \cos(\frac{2(q-1)j\pi}{n-1}).
$$


#### (ii)

The fact implies that
$$
S_k[T_{2j}(t_q)]=-\frac{1+T_{2k}(t_q)}{2}+\sum_{j=0}^kT_{2j}(t_q)=0,q=0,...,n-1,
$$
and
$$
S_k[T_{2j}(t_1)]=S_k[T_{2j}(t_n)]=k.
$$
So
$$
\begin{aligned}
2k\omega_1
&=\omega_q S_k[T_{2j}(t_1)]+\omega_q S_n[T_{2j}(t_n)]\\
&=\sum_{q=1}^n \omega_q S_k[T_{2j}(t_q)]\\
&=\sum_{q=1}^n\bigg[-\frac{\omega_q+\omega_qT_{2k}(t_q)}{2}+\sum_{j=0}^k \omega_qT_{2j}(t_q)\bigg]\\
&=-\frac{1}{2}\sum_{q=1}^n \omega_q -\frac{1}{2}\sum_{q=1}^n \omega_qT_{2k}(t_q)+\sum_{q=1}^n\sum_{j=0}^k \omega_qT_{2j}(t_q)\\
&=-1 -\frac{1}{2}(\frac{1}{2k+1}-\frac{1}{2k-1})+\sum_{j=0}^k \sum_{q=1}^n\omega_qT_{2j}(t_q)\\
&=-1 +\frac{1}{4k^2-1}+\sum_{j=0}^k (\frac{1}{2j+1}-\frac{1}{2j-1})\\
&=-1 +\frac{1}{4k^2-1}+\frac{1}{2k+1}+1\\
&=\frac{2k}{4k^2-1}.
\end{aligned}
$$
Thus
$$
\omega_1=\frac{1}{4k^2-1}.
$$
