# #4
![[Pasted image 20250801180438.png]]

***Proof***: For the forward direction, we extract $E_n$ of finite measure and disjoint such that 
$$\bigcup E_{n}= X $$
WLOG, we assume naturally all sets have non-zero measure. *actually need to use the $a_n$ I thought of originally to avoid 0 measure sets* 
$$
f(x)=\sum _{n=1}^\infty \chi_{E _{n}}\cdot \frac{1}{2^n\mu(E_{n})}
$$
Observe now that:

$$
\int _{X}f(x)d\mu = \int_{X}\sum _{n=1}^\infty \chi_{E _{n}}\cdot \frac{1}{2^n\mu(E_{n})}d\mu = \sum _{n=1}^\infty \int_{X}\chi _{E_{n}} \frac{1}{2^n\mu( E _{n})}d\mu = \sum_{n=1}^\infty \frac{\mu(E _{n})}{2^n\mu(E_{n})} = \sum_{n=1}^\infty \frac{1}{2^n}= 1. 
$$
where the interchanging of the sum and integral has been applied with [[Tonelli's Theorem]]. *We should normalize this using f/int(f)*
For the other direction, we suppose there exists a measurable function with the given property. In order to construct the sigma finite defining sets, we consider the sets
$$
E_{n } := \left\{  x\in X \ | \ f(x)\geq \frac{1}{n}  \right\}
$$
All such sets must be of finite measure for, if not for $E_k$ say,
$$
\int _{X}f(x)d\mu \geq \int_{E _{k}}f(x)d\mu \geq \int_{E_{k}} \frac{1}{k}d\mu = \frac{m(E_{k})}{k}=\infty
$$
since $f$ is positive. Moreover,
$$
\left\{  x \in X \ | \ f(x)\geq \frac{1}{n}  \right\}\nearrow \{ x\in X \ | \ f(x)> 0 \} = X
$$
since $f: X\to (0,\infty)$. But now it must be the case that 
$$
\bigcup _{n=1}^\infty E_{n}= X
$$
We note that this is sufficient for $\sigma$-finite, but we may also make them easily pairwise disjoint by requiring $\frac{1}{n-1}> f(x) \geq \frac{1}{n}$ for $n>1$.  
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 

# #6
![[Pasted image 20250802143421.png]]

***Proof***: (a) Suppose that $f_n\to f$ pointwise a. e. Note that 
$$
\int _{0}^1 \frac{{|f-f_{n}|}}{|f-f_{n}|+1}dm
$$
has non-negative integrand. Moreover, by pointwise convergence $\lim_{ n \to \infty }|f-f_{n}|=0$. With the bound:
$$
\frac{{|f-f _{n}|}}{|f-f_{n}|+1}\leq \frac{{|f-f _{n}|}}{|f-f_{n}|} =1 \in L^1([0,1])
$$
Thus, using the [[Dominated Convergence Theorem]], we can pull in the limit:
$$
\lim _{ n \to \infty } \int_{0}^1 \frac{{|f-f _{n}|}}{|f-f_{n}|+1}dm = \int_{0}^1 \frac{0}{0+1}dm = 0 
$$
which shows convergence in $d$. 
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 

***Proof***: (b) Take the sequence of typewriter functions on $[0,1]$. That is, 
$$
f _{1} = \chi_{[0, 1]} , f _{2} = \chi_{\left[ 0, \frac{1}{2} \right]}, f _{3} = \chi_{\left[  \frac{1}{2}, 1 \right]}, f _{4} = \chi_{\left[ 0, \frac{1}{4} \right]},\dots
$$
Then for each $n$
$$
\int _{0}^1 \frac{|f_{n}|}{|f _{n}|+1}dm = \int_{I _{n} } \frac{1}{2} dm = \frac{1}{2}m(I_{n})\to 0
$$
where we use $I_n$ to denote the interval upon which $f_n$ is the indicator function. However, given any $x\in[0,1]$, $f_n(x)$ takes on both 0 and 1 as values for infinitely many $n$. Thus there cannot be a pointwise limit, yielding a counterexample.
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

# #8
![[Pasted image 20250802145844.png]]

***Proof***: 