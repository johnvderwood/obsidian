# #2
![[Pasted image 20250802155858.png]]

***Proof***: We note that for sufficiently large $n$ 
$$
x^\left(  \frac{n}{\ln(n+2018)} \right) \geq x^2
$$
when $x>1$ since the exponent is increasing as $x$ grows faster than $ln(x+2018)$ via a simple derivative calculation. Thus, we may use this in view of the [[Dominated Convergence Theorem]] to get to: 
$$
\frac{1}{1+x^{ n/\ln(n+2018)}}\leq \frac{1}{1+x^2}
$$
where the RHS is integrable on $(1,\infty)$. Thus, noting the pointwise limit of the LHS is 0,
$$
\lim _{ n \to \infty } \int_{1}^\infty f_{n}(x)dx = \int_{1}^\infty 0 dx = 0
$$
For the $[0,1]$ portion, note that we again can apply the [[Dominated Convergence Theorem]] by noting the bound:
$$
f_{n}(x) \leq 1 \in L^1([0,1])
$$
Moreover, again as the exponent increases but this time for $0<x<1$, $f_n(x)\to 0$ pointwise. It follows then by the DCT,
$$
\lim _{ n \to \infty } \int_{0}^1 f _{n}(x) dx = \int_{0}^11 dx = 1
$$
Combining these results,
$$
\lim _{ n \to \infty } \int_{0}^\infty f_{n}(x)dx = 1
$$
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 

# #6
![[Pasted image 20250802163019.png]]

***Proof***: 


# #8
![[Pasted image 20250802164852.png]]

***Proof***: Let $\delta,\epsilon>0$. We aim to show that there exists an $n\in\mathbb{N}$ such that
$$
\mu(\{ x: |f_{n}^2-f^2|>\epsilon \})<\delta
$$
We begin by observing that finiteness a. e. guarantees that for some $k$
$$
\mu(\{ x: |f_{n}|\geq k \})< \frac{\delta}{2}
$$
and similarly for $f$. Thus, we can find a $K\geq k$ such that 
$$
\mu(\{ x: |f_{n}|\geq K \ \text{or} \ |f|\geq K \})< \frac{\delta}{2}
$$
Let us denote the above set by $A_K$. Then on $A_K^c$, we have
$$
|f_{n}|, |f|\leq K
$$
Thus, 
$$
|f_{n}^2
-f^2| = |f _{n}^2-f_{n}f +f _{n}f -f^2| \leq |f_{n}||f _{n}-f| + |f||f_{n}-f|\leq K|f _{n}-f|+K|f_{n}-f|= 2K|f_{n}-f|
$$
Note that we can find an $N$ such that $n\geq N$ yields
$$
\mu\left( \left\{  x: |f_{n}-f|< \frac{\epsilon}{2 K}  \right\} \right)< \frac{\delta}{2}
$$
by the convergence in measure of $f_n \to f$. To combine these results, note that since $A_k, A_k^c$ are disjoint and choosing $n\geq N$:
$$
\mu (\{ x: |f _{n}^2-f^2 | > \epsilon\}) = \mu (A_{k} \cap \{ x: |f_{n}^2 -f^2| > \epsilon\}) + \mu (A_{k}^c \cap \{ x: |f_{n}^2 -f^2| > \epsilon\})
$$
The first set in question is a subset of $A_k$ so it must have measure of at most $\frac{\delta}{2}$ by construction. Thus the above has the bound:
$$
\leq \frac{\delta}{2}+\mu(A_{k}^c \cap \{ x: |f_{n}^2 -f^2| > \epsilon\})
$$
Applying the before then, noting that both $f_n,f$ are bounded above by $K$ on the remaining set so that
$$
A_{k}^c \cap \{ x: |f_{n}^2 -f^2| > \epsilon\} \subset \left\{  x: |f_{n}-f|> \frac{\epsilon}{2K}  \right\}
$$
coming directly from $|f_{n}^2-f^2|\leq 2K|f_{n}-f|$. But $N$ was chosen to make the RHS set of small measure so that
$$
\mu(A_{k}^c \cap \{ x: |f_{n}^2 -f^2| > \epsilon\}) \leq \frac{\delta}{2}
$$
Combining with the above we see that 
$$
\mu(\{ x: |f_{n}^2 -f^2|>\epsilon\}) < \frac{\delta}{2} + \frac{\delta}{2} = \delta
$$
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 


