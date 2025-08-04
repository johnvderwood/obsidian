# #4
![[Pasted image 20250803195256.png]]

# #6
![[Pasted image 20250803195340.png]]

***Proof***: Via the definition of the $f_{n}$, we have that they form a uniformly bounded family of holomorphic functions (we may easily bound their moduli by 1). Thus, by Montel's Theorem, they form a normal family. Let $K\subset \mathbb{D}$ be compact. Then from the definition of normal family, $f_n$ admits a uniformly convergent subsequence $f _{n_ k}\to f$ where $f$ is holomorphic and maps the disc to at most the closed disc. Now, for the particular $z$ guaranteed by the hypothesis, $f _{n_ k}(z)\to 1$, which implies that $f(z)=1$ by, say, continuity. But now, by the maximum modulus principle, $f$ must be a constant function, and consequently the constant 1 function on $K$. 
For a contradiction, we now suppose that $f_n\not\to 1$ uniformly. Then there exists $\epsilon>0$ such that for all $n$, $|f_n(z_{0})-1|>\epsilon$ for some $z_0\in \mathbb{K}$. But notice that the above $f_{n_{k}}\subset f_{n}$ so that, consequently, 
$$
|f _{n_{k}}(z_{0})-1|>\epsilon \ \ \ \forall n_{k}
$$
But this contradicts the uniform convergence of $f_{n_{k}}$ to 1 on $K$. Thus, it must be that $f_n \to 1$ locally uniformly. 
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

