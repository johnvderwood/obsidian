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

***Proof***: Our goal is towards Holder's, so to this end, rewrite the given expression as:

$$
\frac{1}{p} + \frac{1}{q } =\frac{1}{r } \iff \frac{r}{p} +\frac{r}{q} = 1 \iff \frac{1}{ \frac{p}{r} } + \frac{1}{ \frac{q}{r} } = 1
$$
Now observe that by [[Holder's Inequality]]: 
$$
||fg||^r_{L^r}=\int|f^r||g^r|  \leq \left(\int(|f|^r)^{p/r}\right)^{r/p}\left(\int(|g|^r)^{q/r}\right)^{r/q}
$$
Now reapplying the $1/r$ power to both sides:
$$
||fg||_{L^r}\leq \left(\int|f|^p\right)^{1/p}\left(\int|g|^q\right)^{1/q} = ||f||_{L^p}||g||_{L^q}
$$
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 

# #6
![[Pasted image 20250801015240.png]]

***Proof***: Under the hypotheses, we let $\epsilon>0$. By [[Egorov's Theorem]], there exists a set $E$ measurable with $m(E)< \frac{\epsilon}{2}$ such that $f_{n}\to 0$ uniformly on $[0,1]\setminus E$. By uniform convergence, there additionally exists a $N$ such that $n\geq N$ guarantees
$$
|f_{n}|\leq \frac{\epsilon}{2}
$$
on $E$. In order to put these together, notice that
$$
||f _{n}||_{L^1[0, 1]}=\int _{E}|f_{n}| + \int_{[0, 1]\setminus E}|f _{n}|\leq \int_{E}|f_{n}|+ \frac{\epsilon^2}{4}
$$
by the above. To bound the other integral, we apply [[Holder's Inequality]]:
$$
\int _{E^c}|f_{n}| \leq \left(\int|f_{n}|^2\right)^{1/2} \left(\int dm\right)^{1/2} \leq 1\cdot {m(E)}^{1/2}= \sqrt{ \frac{\epsilon}{2} }
$$
Thus,
$$
||f _{n}||_{L^1[0, 1]}\leq \sqrt{ \frac{\epsilon}{2} }+ \frac{\epsilon^2}{4}
$$
which is sufficient to show the $L^1$ convergence to 0 as $\epsilon$ was arbitrary. 
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 


# #7
![[Pasted image 20250801021213.png]]

***Proof***: Consider the sequence of functions $f_n(x)=1+1/n$. 

# #9
![[Pasted image 20250801174812.png]]

***Proof***: 