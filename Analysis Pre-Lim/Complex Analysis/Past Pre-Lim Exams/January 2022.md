# #1
![[Pasted image 20250620184933.png]]

# #2
![[Pasted image 20250624232944.png]]

***Proof***: Suppose that $f$ had more than one fixed point. That is, suppose for instance, $f(z_0)=z_0$ and $f(z_1)=z_1$. Now since $G$ is an open simply connected domain, by the [[Riemann Mapping Theorem]], there exists a conformal map $\phi:\mathbb{D}\rightarrow G$ such that $\phi(0)=z_0$. Consider the composition of $g=\phi^{-1} \circ f \circ \phi$. Note that $g$ is analytic and maps $\mathbb{D}\rightarrow \mathbb{D}$, and that, moreover $g(0)=0$. Thus, we may apply [[Schwarz Lemma]] to conclude that for any $z\neq 0$, $|g(z)|\leq |z|$, wherein equality implies that $g$ is in fact a rotation. Now observe that by conformality, we may let $y=\phi^{-1}(z_1)\in \mathbb{D}$. Then $g(y)=y$. Thus, we determine that $g$ is in fact a rotation since $|g(y)|=|y|$ is apparent. However, the only rotation that fixes two points (here, 0 and $y$) is the trivial one. i. e., the identity map. But then $$ \phi\circ g = f\circ \phi \implies \phi =f\circ \phi 
$$
Thus, 
$$ \phi(z)=f(\phi(z))
$$ By conformality, we can write $z=\phi^{-1}(w)$ for any $w\in G$ to view this instead as a map from $G$ to $G$. Thus, 
$$\phi(\phi^{-1}(w))=f(\phi(\phi^{-1}(w)))\implies w = f(w)
$$
But now this holds for all $w\in G$. We then conclude that no such $f$ under the hypotheses may exist as then $f$ must be the identity. 
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 
# #4
![[Pasted image 20250625002010.png]]
*This problem has a typo in it! It should read $\Re(a) >1$!*

***Proof***: We have the goal of applying [[Rouche's Theorem]]. To this end, let us fix a disc in which we will observe the moduli. Consider for instance the disc centered at $a+1$ of radius $1+\Re(a)$. i. e., $D=D_{1+\Re(a)}(a+1)$.  For any $z$ on the boundary of $D$,
$$ |e^{-z}|= |e^{-(1+a)-(1+\Re(a))\cos(\theta)-i(1+\Re(a))\sin(\theta)}|=e^{-1-\Re(a)}e^{-(1+\Re(a))\cos({\theta})}\leq 1
$$
Now, note that
$$ |a-z| = |a-(1+a)+(1+a)-z|=|(1+a)-z-1| \geq 1+\Re(a)-1 > 1 
$$
by the [[Reverse Triangle Inequality]]. Thus, on the boundary of $D$, $|a-z|>|-e^{-z}|$ where both are holomorphic on any disc containing the closure of $D$. It follows that, by [[Rouche's Theorem]], that $a-z$ and $a-z-e^{-z}$ have the same number of zeros (clearly 1) explicitly within D since $a\in D$. 
# #9
![[Pasted image 20250624143123.png]]
No, there does not.
***Proof***: Suppose such an $f$ did exist. Then $f$ admits a power series centered at $z=0$ on any $C_R$, $R>0$, with 
$$ a_n = \frac{f^{(n)}(0)}{n!}
 $$ Moreover, by [[Cauchy's Integral Formula]] and [[Cauchy's Inequality]]
 $$\frac{f^{(n)}(0)}{n!}=\frac{1}{2\pi i}\int_{C_R}\frac{f(\zeta)}{\zeta^{n+1}}d\zeta 
 $$  Taking moduli,
$$ \left|\frac{f^{(n)}(0)}{n!}\right|=\frac{1}{2\pi}\left|\int _{C_ R}\frac{f(\zeta)}{\zeta^{n+1}}d\zeta \right|\leq \frac{1}{2\pi}\frac{\sup _{C_ R}|f(\zeta)|}{R^{n+1}}\cdot 2\pi R \leq \frac{R^{\frac{2}{3}}}{R^n}
 
 $$
Now, explicitly when $n\geq 1$, the right hand side goes to 0 as $R\rightarrow \infty$, and since the LHS does not depend on $R$, we conclude that $f^{n}(0)=0$ if $n\geq 1$. Thus, $f$ must be a constant function. However, there is no constant function mapping 0 to 0 and $i$ to $i$. Thus, no such function may exist. 
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 
Can I make changes?