# #3
![[Pasted image 20250730112623.png]]

***Proof***: We first deal with the $p=1$ case:
$$
\lvert Tf \rvert_{1}=\int\int|K(x, y)||f(y)| \ dy \ dx 
$$
Since the integrand is non-negative and measurable, we see that we may apply [[Tonelli's Theorem]] to interchange the order of integration. Then we have:
$$
\int \int|K(x, y)||f(y)| \ dx \ dy=\int |f(y)|\int |K(x, y)| \ dx \ dy \leq C\int |f(y) | dy = C\cdot\lvert f \rvert_{p} 
$$
Thus, we pass to considering the case where $p>1$: 
In this case, we notice that we may find $q$ such that $1/p+1/q=1$, allowing:
$$
|K(x, y)||f(y)|=|K(x, y)|^{1/q} |K(x, y)|^{1/p} |f(y)|
$$
With this in mind, observe that taking the $p\text{th}$ norm of $Tf$ now yields:
$$
||Tf||_{p}= \left(\int \left|\int K(x, y)f(y) dy \right|^{p} dx\right)^{1/p}\leq \left( \int \left(\int|K(x, y)||f(y)|dy \right)^p dx \right)^{1/p}
$$
Applying the before identity,
$$
= \left( \int \left(\int|K(x, y)|^{1/q} |K(x, y)|^{1/p} |f(y)|dy \right)^p dx \right)^{1/p}
$$
And now we apply [[Holder's Inequality]] to the innermost integrand:
$$
\leq \left( \int \left(\int|K(x, y)| dy \right)^{p/q} \left( \int |K(x, y)| |f(y)|^pdy \right) dx \right)^{1/p} \leq \left( \int C^{ p/q } \int |K(x, y)| |f(y)|^pdy \ dx   \right)^{1/p}
$$
Now, again by [[Tonelli's Theorem]], we achieve:
$$
= \left(C^{p/q} \int \int |K(x, y)||f(y)|^pdx dy \right)^{1/p}\leq \left( C^{p/q+1 } \int |f(y)|^pdy\right)^{1/p} = C^{1/q+1/p}||f||_{p}=C\cdot||f||_{p}
$$
as desired. Noting that both of these inequalities also shows that $Tf\in L^p(\mathbb{R})$, we are done.
$$\tag*{$\blacksquare$}$$
_________________________________________________________________ 

# #4
![[Pasted image 20250730115348.png]]

***Proof***: We note that the set $E$ is precisely the $\limsup E_{n}=\bigcap_{n=1}^\infty\bigcup_{k=n}E_{k}$. To see this precisely, we note that if $x\in E$, then $x$ is in infinitely many $E_n$. Thus, for each $n$, $x\in\bigcup_{k=n}^\infty E_k$ so that $x\in\limsup E_n$. On the other hand, if $x\in \limsup E_n$, we suppose for a contradiction that $x$ is not in infinitely many $E_n$. Then there exists $N$ such that $n\geq N$ implies that $x\notin E_n$. Then $x\notin \bigcup_{k=n}^\infty E_k$ so that it can also not be in the intersection of all such unions over $n$. Thus, $x\notin \limsup E_n$, a contradiction. So $E$ is indeed the prescribed set. 
For the other part, note that $\bigcup_{k=n}^\infty E_k$ is a decreasing sequence as $n$ grows since we take the union over fewer sets. Moreover $\mu(\bigcup_{k=1}^\infty E_k) < \infty$ since we have that $\mu$ is a finite measure. Consequently, we observe [[Continuity from Above]]:
$$
\mu\left(\bigcap _{n=1}^\infty \left(\bigcup_{k=n}^\infty E _{k}\right) \right) = \lim_{ n \to \infty } \mu \left(\bigcup_{k=n}^\infty E_{k}\right) 
$$ Now by the given condition that $\mu(E_k)\geq \alpha$ for all $k$, the resulting limit must observe the same lower bound in measure for the above union:
$$
\lim _{ n \to \infty } \mu \left(\bigcup_{k=n}^\infty E_{k}\right)  \geq \alpha
$$
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

# #8 
![[Pasted image 20250730121329.png]]

***Proof***: We proceed by assuming for a contradiction that there exists $E\subset(-\infty,-1)\cup(1,\infty):=A$ wherein $f\neq 0$ on $E$ and $m(E)>0$. Note that for each $n$ we have the valid splitting of the integral:
$$
\int _{A \setminus  E} |x|^nf(x)dx + \int_{E}|x|^n f(x) dx + \int_{-1}^1 |x|^n f(x) dx
$$
Our concentration lies within the middle integral here. Note that if we define $f_n(x)=|x|^n f(x)$, then $f_n$ is increasing as n increases for a fixed $x$ since $|x|>1$ on $E$. Moreover, the $f_n$ are non-negative clearly. We lastly see that the pointwise limit for some $x\in E$ has $f_n(x)\to \infty$ since $f(x)>0$ on $E$ and $|x|^n$ grows without bound for $|x|>1$. Thus, we can apply the [[Monotone Convergence Theorem]] to assert that:

$$
\lim _{ n \to \infty } \int_{E} |x|^nf(x) dx \to \infty
$$

Consequently then the unsplit integral tends toward infinity as $n$ grows since the other integrands are always non-negative so that we have at worst some non-negative value plus an infinitely growing value. Thus 
$$
\lim _{ n \to \infty } \int_{\mathbb{R}} |x|^nf(x)dx \to \infty 
$$
contradicting the given condition that the supremum over $n$ is finite. 
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

# #9
![[Pasted image 20250730143455.png]]

***Proof***: We proceed by contradiction, assuming that $f_n$ is Cauchy. Since $L^1$ is complete, then $f_n\to f\in L^1$ in $L^1$ norm. Now, notice further that we have the following convergence by [[Holder's Inequality]] directly:
$$
\left|\int _{\mathbb{R}} f_{n}g \ - \int _{\mathbb{R}} fg\right| \leq ||g||_{\infty}||f _{n}-f||_{1} \to 0 
$$
by the $L^1$ convergence and since $g$ has finite essential supremum by being a continuous and compactly supported function. By the given condition on $f_n$ then we conclude
$$
\int_{\mathbb{R}}fg = g(0)
$$
We now define a sequence of continuous and compactly supported functions:
$$
g_{k}(x) := \begin{cases} 
nx+1 \hspace{0.5 in} &\text{if } x \in \left[ -\frac{1}{n}, 0 \right) \\ \\
-nx+1 \hspace{0.5 in} &\text{if } x \in \left[ 0, \frac{1}{n} \right] \\ \\
0 \hspace{0.5 in} &\text{else}
\end{cases}  
$$
Notice then that we have the pointwise convergence
$$ g_{k}(x)\to g(x):=
\begin{cases}
&1 \hspace{0.5 in} x=0 \\
&0 \hspace{0.5 in} \text{else}
\end{cases}
$$
Now observe that
$$
|fg _{k}|\leq |fg_{1}| 
$$
where $fg_{1}\in L^1(\mathbb{R})$ and we have as before the pointwise convergence $fg_k \to fg$. Thus, we can apply the [[Dominated Convergence Theorem]] to note that
$$
\lim _{ n \to \infty }\int_{\mathbb{R}}fg _{k } = \int_{\mathbb{R}} \lim _{ n \to \infty } fg_{k } = \int _{\mathbb{R}} f\chi_{\{0\}} = 0
$$
But this limit contradicts the fact that for all $k$:
$$
\int _{\mathbb{R}} fg_{k }=1
$$ Thus we have the result. $$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 
