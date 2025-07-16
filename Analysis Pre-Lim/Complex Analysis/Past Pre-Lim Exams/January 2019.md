# #1
![[Pasted image 20250629192256.png]]

***Proof***: We follow the following contour which we will call $\gamma$ for the function $f(z)=\sqrt{z}/({1+z^2})$ with a choice of $R>1, \ 0<r<1$:

![[Pasted image 20250702183416.png]]

Explicitly then, we are computing:
$$
\int_{\gamma}f(z)dz = \sum_{i=1}^4
\int_{\gamma_{i}}f(z)dz$$
Note that, since $f$ has one simple [[pole]] at $z=i$ and is otherwise holomorphic on and within the selected contour (with a branch cut choice along the negative imaginary axis; angles from $[-\frac{\pi}{2},\frac{3\pi}{2})$), by the [[Residue Theorem]], we have
$$
\int _{\gamma}f(z)dz = 2\pi i\lim_{ z \to i } (z-i)\frac{\sqrt{ z }}{(z-i)(z+i)}
$$
$$
=2\pi i \frac{\sqrt{ i }}{2 i}=\pi \sqrt{ i }= \pi \sqrt{ e^{i\pi/2} }=\pi e^{i\pi/4}=\frac{\pi \sqrt{ 2 }}{2}
$$
in accordance with the selected branch cut. Thus, the remaining integrals to be determined are those on the RHS of the first equality. To tackle this one by one, we start with $\gamma_{1}$ using a standard circular parametrization:
$$
\int _{\gamma_{1}}f(z)dz=\int_{0}^{2\pi} \frac{\sqrt{ R e^{i\theta} }}{(1+R e^{i\theta})^2}R i e^{i\theta}d\theta 
$$
Via some algebra,
$$
=\int_{0}^{2\pi} \frac{R^{3/2}\sqrt{ e^{i\theta} }ie^{i\theta}}{(1+R e^{i\theta})^2}d\theta
$$
Now observing the integrand on its own:
$$
\left|\frac{R^{3/2}\sqrt{ e^{i\theta} }ie^{i\theta}}{(1+R e^{i\theta})^2}\right| = \frac{|R^{3/2}|}{|1+R e^{i\theta}|^2}\to 0 \ \text{ as $R \to \infty$ }
$$
We obtain a similar bound along $\gamma_{3}$ using a similarly constructed parametrization:

$$
\int _{\gamma_{3}}f(z)dz = \int_{0}^{2\pi}  \frac{\sqrt{ r e^{i\theta} }}{(1+r e^{i\theta})^2}r i e^{i\theta}d\theta 
$$
where
$$
\left|\frac{\sqrt{ r e^{i\theta} }}{(1+r e^{i\theta})^2}r i e^{i\theta}\right|=\left|\frac{r^{3/2}}{(1+r e^{i\theta})^2}\right|=\frac{|r^{3/2}|}{|1+r e^{i\theta}|^2}\leq |r^{3/2}|\to 0 \ \text{ as $r\to 0$}
$$

Next, we note that along $\gamma_{2}$, we can perform a simple substitution of $z=-x$:
$$
\int _{\gamma_{2}} f(z) dz = \int _{-R}^{-r}f(z)dz = \int_{R}^r -f(-x)dx = \int _{r}^R \frac{\sqrt{ -x }}{1+x^2}dx= i \int_{r}^R \frac{\sqrt{ x }}{1+x^2}dx
$$
where the integrand is now fully real valued. Similarly,

$$
\int _{\gamma_{3}} f(z)dz = \int_{r}^R \frac{\sqrt{ x }}{1+x^2}dx
$$
We start by collecting these for finite and fixed $R,r$:

$$
\int _{\gamma} f(z)dz = \int_{0}^{2\pi} \frac{R^{3/2}\sqrt{ e^{i\theta} }ie^{i\theta}}{(1+R e^{i\theta})^2}d\theta + i \int _{r}^R \frac{\sqrt{ x }}{1+x^2}dx + \int_{0}^{2\pi}  \frac{\sqrt{ r e^{i\theta} }}{(1+r e^{i\theta})^2}r i e^{i\theta}d\theta + \int_{r}^R \frac{\sqrt{ x }}{1+x^2}dx 
$$
Sending $R$ to $\infty$ and $r$ to 0,

$$
\frac{\pi \sqrt{ 2 }}{2} = i\int_{0}^\infty \frac{\sqrt{ x }}{1+x^2}dx + \int_{0}^\infty \frac{\sqrt{ x }}{1+x^2}dx
$$
Taking real parts on both sides then, we find that 

$$
\frac{\pi \sqrt{ 2 }}{2} = \int_{0}^{\infty} \frac{\sqrt{ x }}{1+x^2}dx
$$
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

# #3 
![[Pasted image 20250629192343.png]]

***Proof***: We start by assuming $f$ is non-constant toward the goal of showing that $A(r)$ must then be strictly increasing. Under this primary condition, we now show $A(r)$ is strictly increasing by way of contradiction. That is, we suppose that for some $0\leq r<R<1$, $A(r)\geq A(R)$. Observe that by $f$ holomorphic on $\mathbb{D}$, the function $e^{f(z)}$ is then also holomorphic on the same domain. Thus, $e^{f(z)}$ observes the [[Maximum Modulus Principle]]. Furthermore, we may find the modulus of this function, call it $g$, via:
$$
|g(z)|=|e^{f(z)}| = |e^{\mathrm{Re} f + i \mathrm{Im}f}|=|e^{\mathrm{Re}f}||e^{i\mathrm{Im}f}| = e^{\mathrm{Re} f}
$$
But now, if say $A(r) > A(R)$, then:
$$
\sup _{{z \in C_{r}}} |g(z)| > \sup_{{z \in C_{R}}}|g(z)|
$$
in violation of the [[Maximum Modulus principle]] for the disc $D_R$. In the equality case, this still violates the [[Maximum Modulus principle]] since the assumption that $f$ was non-constant forces $g$ to be non-constant, wherein $g$ would have to be constant since it achieves its maximum not on the boundary (in particular, on $C_r$). These contradictions imply that $A(r)$ must be a strictly increasing function. $$\tag*{$\blacksquare$}$$ 

_________________________________________________________________ 

# #5 
![[Pasted image 20250629192420.png]]

***Proof***: We continue via a contradiction argument. To begin, assume $f(\mathbb{H})$ is not a dense subset. Under the given conditions, $f$ satisfies the hypotheses of the [[Schwarz Reflection Principle]]. That is, $f$ extends to a function holomorphic on the entirety of $\mathbb{C}$. For simplicity, we replace this extension with the former name we gave: $f$. By non-density, there exists $w\in \mathbb{H}$ and a $\delta >0$ such that:
$$
|f(z)-w|>\delta \ \ \ \ \ \ \ \ \forall z\in\mathbb{H}
$$
Under this scenario, $f-w$ stays away from 0 since it is bounded below by $\delta$. Thus, $\frac{1}{f(z)-w}$ is nowhere vanishing and thus holomorphic on $\mathbb{C}$. Note that this remains valid for the extension since the extension is defined via $f(\overline{z}) := \overline{f(z)}$ so that the extension admits no new values in the upper half-plane. Moreover, $\frac{1}{f-w}$ can be easily bounded via the above:
$$
\frac{1}{|f(z)-w|}\leq \frac{1}{\delta}<\infty
$$
But now $\frac{1}{f-w}$ is bounded and entire, implying that it is constant by [[Liouville's Theorem]]. But $\frac{1}{f-w}$ is constant $\iff$ $f$ is constant $\iff$ the original non-extended $f$ is constant. However, if the original $f$ were constant, it must be a real constant by (iii). But this is contradictory for any $z\in \mathbb{H}$ as (iv) puts that function value in the upper half plane, omitting the real line. This contradiction forces the original $f$ to have a dense image in $\mathbb{H}$. $$\tag*{$\blacksquare$}$$  
_________________________________________________________________ 

# #7
![[Pasted image 20250629192456.png]]

***Proof***: We edit the standard conformal map from $\mathbb{D}\to \mathbb{H}$ to obtain a map to the right half plane sending 0 to a chosen $w\in\mathbb{C}_+$:  
$$
g^{-1}(z)= \frac{{w-z}}{\overline{w}+z}
$$
Thus, we can easily construct the inverse:
$$
g(z)=\frac{{\overline{w}z-w}}{-z-1}
$$
We use the same notion in the original construction for a map sending $f(w)$ to 0:
$$
h(z)=\frac{{f(w)-z}}{\overline{f(w)}+z}
$$
Observe that now the composition $h(f(g(z))):\mathbb{D}\to\mathbb{D}$ where this map is holomorphic and sends 0 to 0. Thus, we can apply [[Schwarz Lemma]]:
$$
|[h(f(g(0)))]'|\leq 1\implies |f'(g(0))|\leq \frac{1}{|h'(f(g(0))|\cdot|g'(0)|}
$$
$$
\implies |f'(w)|\leq \frac{1}{|h'(f(w))|\cdot|g'(0)|}=\frac{|4\cdot \mathrm{Re}(f(w))^2|}{|-2\cdot\mathrm{Re}(f(w))|}\cdot\frac{1}{|-2\cdot\mathrm{Re}(w)|}=\frac{\mathrm{Re}(f(w))}{\mathrm{Re}(w)}
$$
which was to be shown. 
_________________________________________________________________ 
# #9
![[Pasted image 20250629192521.png]]

***Proof***: Consider the family of functions $\mathcal{F}:=\{f(z), f(z+1), f(z+2),... \}$. Since shifting the domain $G$ returns the same domain, all of these functions remain analytic and maintain the same uniform bound from $|f(z)|\leq M$ given under the assumptions. Thus, this family is uniformly bounded and, by [[Montel's Theorem]], is then a [[normal family]]. Let $x\in \mathbb{R}$, and denote $f_n(z)=f(z+n)$. We have that $f_n(z)$ is a sequence in the normal family $\mathcal{F}$, and therefore, it must have a convergent subsequence $f_{n_k}(z)$. By $f _{n_ k}(x)\to c$ by the hypothesis, $f _{n_ k}\to c$ on the real line. But then the limiting function of the $f_{n_k}$, $c$ is holomorphic as the locally uniform limit of holomorphic functions. It then satisfies the [[Identity Theorem]] on $G$ so that it must be the constant function $c$ on the whole of $G$. The necessary limit then follows:
$$
\lim_{ x \to +\infty }  f(z+x)=c \ \ \ \ \text{for all } z\in G
$$
$$\tag*{$\blacksquare$}$$ 

_________________________________________________________________ 
