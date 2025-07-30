# #4
![[Pasted image 20250730160349.png]]

***Proof***: We break the integral into two parts. First we deal with the integral starting from 1 to $\infty$:
$$
x>1 \implies \frac{n^2 x}{1+x^2}e^{-n^2 x^2}\leq \frac{n^2 x}{n^2 x(1+x^2)}= \frac{1}{1+x^2}\in L^1(1,\infty)
$$
Moreover, we observe the pointwise limit of the integrand is 0 for $x>1$ as $e^{n^2}$ grows faster than $n^2$ (as seen by a basic derivative computation). Thus, we can apply the [[Dominated Convergence Theorem]] to see that 
$$
\lim _{ n \to \infty }\int_{0}^\infty f _{n}(x)dx = \int_{0}^\infty 0 dx = 0.
$$
For the other part of the integral, we make the substitution $u=nx$. Then $du=ndx$, and we have:
$$
\int _{0}^1 \frac{n^2 x}{1+x^2}e^{-n^2 x^2} dx = \int_{0}^n \frac{u}{e^{u^2}\left( 1+\frac{u^2}{n^2} \right)}du = \int _{0}^\infty \frac{u}{e^{u^2}\left( 1+\frac{u^2}{n^2} \right)}\chi_{[0,n]}(u)du
$$
Now observe that the integrand here has:
$$
\frac{u}{e^{u^2}\left( 1+\frac{u^2}{n^2} \right)}\chi_{[0, n]}(u)\leq \frac{u}{e^{u^2}}\in L^1(0,\infty)
$$
Moreover, this is in fact the pointwise limit as well since $u^2/n^2\to 0$ pointwise. Thus, another application of the [[Dominated Convergence Theorem]] allows the calculation:
$$
\lim_{ n \to \infty } \int_{0}^\infty\frac{u}{e^{u^2}\left( 1+\frac{u^2}{n^2} \right)}\chi_{[0, n]}(u) du= \int _{0}^\infty \frac{u}{e^{u^2}}du = -\frac{e^{-u^2}}{2}\Biggr|_{u=0}^{u=\infty} =0+\frac{1}{2}=\frac{1}{2}
$$
This we find that the overall limit in question is $\frac{1}{2}$. 
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

# #5
![[Pasted image 20250730162350.png]]

