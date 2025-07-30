View all problems [[Analysis Exams.pdf#page=12|here]]
# #1
![[Pasted image 20250707191806.png]]

***Proof***: First, observe the equality chain:
$$
\frac{f'(z)}{f(z)}=\frac{g'(z)}{g(z)} \iff \frac{f'(z)}{f(z)}-\frac{g'(z)}{g(z)}=0 \iff \text{($f,g$ non-vanishing)} \ \ f'(z)g(z)-f(z)g'(z)=0
$$
$$
\iff \text{($f,g$ non-vanishing)} \ \left(\frac{f(z)}{g(z)}\right)'=0
$$
Now using the assumptions from the problem, the above chain holds for all $\alpha_{n}$ which accumulate to $\alpha$ in $G$ which is open and connected. Thus, by the [[Identity Theorem]], $(f/g)'=0$ for all $z\in G$. Thus, it follows that $f/g=c$ for some $c\in\mathbb{C}$ since only constant functions have 0 derivative. Then again, multiplying through by $g$ is valid by $g$ non-vanishing so that $f=c\cdot g$ as desired. $$\tag*{$\blacksquare$}$$
_________________________________________________________________ 

# #3
![[Pasted image 20250708123913.png]]

***Proof***: 

# #5
![[Pasted image 20250708123952.png]]

***Proof***: Let $K\subset \mathbb{D}$ be compact. We show that $\mathcal{F}$ is uniformly bounded on $K$ if the series converges for all $z\in\mathbb{D}$. To this end, note that any $f\in \mathcal{F}$ has a natural power series at $z_{0}=0$ valid for all $z\in\mathbb{D}$:
$$
f(z)=\sum_{n=0}^\infty \frac{f^{(n)}(0)z^n}{n!}
$$
Now observe we have the clear bound:
$$
|f(z)|\leq \sum_{{n=0}}^\infty \frac{M_n|z|^n}{n!}<\infty
$$
Now since the series is convergent for all $z\in\mathbb{D}$, it represents a holomorphic function on the disc. Thus, if we take a disc $D_R$ such that $K\subset D_R \subset \mathbb{D}$ with proper containments, then the series satisfies the [[Maximum Modulus Principle]] (the result is trivial if $f$ is constant since then the obvious bound becomes $M_0$ which will be necessarily less than or equal to the ensuing bound). Thus, the series attains its maximum M on the boundary of $D_R$. Moreover, this value is necessarily finite by the convergence of the series for all $z\in \mathbb{D}$ of which $K$ is a subset. Thus, we see that for all $z\in K$, 
$$
|f(z)|\leq M
$$
achieving the uniform bound. Thus, by [[Montel's Theorem]], $\mathcal{F}$ is a [[normal family]].

For the other direction, let $z\in\mathbb{D}$ and assume that $\mathcal{F}$ is a [[normal family]]. Consider the sequence of (holomorphic) polynomials $f_k(z)=\sum_{{n=0}}^k \frac{M_{n}z^n}{n!}$. Each of the $f_k$ are also clearly members of the [[normal family]] $\mathcal{F}$ since their $n^{th}$ derivatives clearly stay at the bound $M_n$ at 0. Thus, as members of a [[normal family]], they admit a uniformly convergent subsequence $f_{k_l}$ on compact subsets. Pick a compact $K$ so that $z\in K$. Then point-wise, we see that 
$$
f _{k}(z)\to \sum_{n=0}^\infty \frac{M_{n}z^n}{n!} 
$$
Thus this must be the object of the uniform limit of the subsequence. Consequently, the series is holomorphic on $K$ as the locally uniform limit of holomorphic functions (note the above convergence is valid for all $z\in K$). But then this must be its convergent power series centered at 0 by construction so that the series converges at $z$. This works for any $z\in\mathbb{D}$, so we conclude the proof. $$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 


# #7
![[Pasted image 20250708124012.png]]

***Proof***: 

# #9

![[Pasted image 20250708124040.png]]

***Proof***: Since the $f$ to be constructed is holomorphic except at $z=i$ on just $\mathbb{C}$, we see that any such $f$ must have a Laurent series about 0 of the form:
$$
f(z)=\frac{a _{-1}}{z-i}+g(z)=\frac{a_{-1}}{z-i}+\sum_{{n=0}}^\infty a_{n}z^n
$$
Now in particular, if we impose the additional condition that $f$ has a simple [[pole]] at $\infty$ on the extended complex plane, we introduce the condition that $f(1/z)$ has a simple [[pole]] at 0. To observe this behavior, we take the above form of $f$ and observe the image of $\frac{1}{z}$:
$$
f\left( \frac{1}{z} \right)=\frac{a _{-1}}{\frac{1}{z}-i}+a_{0}+a _{1}\left( \frac{1}{z} \right)+a_{2}\left( \frac{1}{z^2} \right)+\dots
$$
Now, notice that if $a_n\neq0$ for $n\geq2$, then the order of the [[pole]] at infinity would instead be $n$ rather than the 1 implied by it being a simple [[pole]]. Thus, it follows that $a_n=0$ for $n\geq2$. Moreover, $a_{-1}, \ a_1\neq0$ in particular since these terms are necessary to make the poles. Thus, $a_0$ may be any constant complex number and we arrive at the final form for $f$:
$$
f(z)=\frac{a _{-1}}{z-i}+a_{0}+a _{1}{z} \ \ \ \ \ \ a_{-1}, \ a_{1}\neq 0
$$
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 
