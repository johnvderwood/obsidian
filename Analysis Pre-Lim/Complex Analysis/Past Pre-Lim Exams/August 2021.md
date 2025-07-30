View all problems [[Analysis Exams.pdf#page=10&selection=0,29,0,39|here]]
# #1
![[Pasted image 20250620122017.png]]

***Proof**:* We first consider the image of the given set:
![[Pasted image 20250620130005.png]]
In the view of the [[Riemann Sphere]], we want to send this to a 180 degree arc. In this light, under the mapping
$$ \phi(z)=\frac{z-i}{z+i} \left(-\frac{1+i}{1-i}\right) $$
This yields a transformation to the upper half-plane, which we now apply the standard (inverse) [[Cayley transformation]] to: 

![[Pasted image 20250620131535.png]]
$$ \rho(z)=\frac{i-z}{i+z}
$$
This obtains the unit disc. Thus, composing $\rho \circ\phi$ yields the desired transformation.  
*This is not the correct problem. This is #1 from Aug 2020. Oops!*
$$\tag*{$\blacksquare$}$$
_________________________________________________________________ 

# #2
![[Pasted image 20250620151035.png]]

***Proof***: In order to compute the given integral, we go by way of observing:
$$
\int_\gamma f(z)dz=\int_\gamma \frac{e^{i az}}{1+z^2}dz
$$
where $\gamma$ is given for $R>1$, and we note that the integrand has a simple [[pole]] at $z=i$:
![[Pasted image 20250623224751.png]]
Now, observe the following breakdown:
$$
I = \int _\gamma \frac{e^{i az}}{1+z^2}dz=\int_{-R}^R f(z)dz \ + \ \int _{C_ R^+}f(z)dz = I_1+I_2
$$
To begin the calculation, we invoke the [[Residue Theorem]]. In this view, we can compute:
$$
I = 2\pi i\cdot \text{Res}_f(i)=2\pi i\cdot \lim_{z\rightarrow i}\frac{e^{i az}}{(z-i)(z+i)}(z-1)=\frac{\pi}{e^a}
$$
On the other hand, we observe that, along $C_R^+$,
$$
|f(z)|=\frac{|e^{iaz}|}{|1+z^2|}\leq \frac{1}{R^2-1}\rightarrow 0 \  \text{ as} \ R\rightarrow\infty
$$
where we applied the [[reverse triangle inequality]] to the denominator and the fact that $|e^{iaz}|=|e^{iaRe^{i\theta}}|=|e^{iaR(\cos{\theta}+i\sin{\theta})}|= e^{-a\sin{\theta}}\leq 1$. Thus,
$$
|I_2|\leq \pi R\frac{1}{R^2-1}\rightarrow 0 \ \text{ as } \ R\rightarrow\infty
$$
Thus, we now conclude that
$$
\frac{\pi}{e^a}=\lim _{R\rightarrow\infty}I = \int_{-\infty}^\infty f(z)dz
$$
Taking real parts on both sides, we have the final result:
$$
\frac{\pi}{e^a}=\int_{-\infty}^\infty \frac{\cos(ax)}{1+x^2}dx
$$

$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 
# #5 
![[Pasted image 20250620161715.png]]

***Proof***: Let $\gamma$ be a closed rectifiable curve in $U$. If $[-1,1]$ is not contained in the interior of $\gamma$ then $f$ is holomorphic for values inside $\gamma$ and thus the integral is immediately 0. So we suppose that the interval is indeed within open components formed by the interior of the curve. Moreover, if $\gamma$ self intersects, any sub-loop formed by $\gamma$ and not containing the interval has 0 integral as $f$ is again holomorphic completely within the interior of $\gamma$. Thus, we note that we are focusing in on loops of the type:
![[Pasted image 20250620163200.png]]
Note that $f$ extends holomorphically to $g$ on the set $V=\mathbb{C}\setminus \{-1,1\}$ where $g$ is just given by $f$'s function rule exactly. Then $g$ has two poles at -1 and 1 respectively and moreover 
$$
\int _\gamma f(z)dz = \int_\gamma g(z)dz
$$
For $g$, we now perform [[residue]] calculations:
$$
\text{res}_{-1}(g(z))= \lim_{z\rightarrow-1}(z+1)\frac{2}{(z-1)(z+1)}=-1
$$
$$
\text{res}_{1}(g(z))= \lim_{z\rightarrow1}(z-1)\frac{2}{(z-1)(z+1)}=1
$$
We have, as $V$ is simply connected except at -1 and 1, by the [[Residue Theorem]]
$$
\int _\gamma g(z)dz = 2\pi i\cdot \sum (-1+1)=0 \implies \int_\gamma f(z) dz=0
$$
as desired. 
*This proof is not correct. Needs refinement*
$$\tag *{$\blacksquare$}$$
_________________________________________________________________

# #6 
![[Pasted image 20250620173525.png]]

***Proof***: We proceed by first assuming that $f$ is not identically zero. Thus our aim is to show $f$ is non-vanishing in this case. To do this, we go by way of contradiction. So we make the further assumption that $f$ vanishes at some $z_0$ say. Thus, $f(z_0)=0$. Let $\gamma$ be a circle whose interior contains $z_0$ and no other zeros of $f$. We note this is possible since, by the [[Identity Theorem]], the zeros of $f$ cannot accumulate since $f$ was assumed to be non-vanishing. Now, for each $n$, since $f_n$ is non-vanishing, holomorphic and $U$ is open and connected, by the [[Argument Principle]],
$$
\frac{1}{2\pi i}\int _\gamma \frac{f_ n'(z)}{f_n(z)}dz = \# \text{ zeros} - \# \text{ poles }
$$
From this, we note that $f_n$ is completely non-vanishing and that $f_n$ has no poles as a holomorphic function so that the RHS becomes 0-0=0. Now we consider the limit of these: 
$$
\lim _{n\rightarrow \infty}\frac{1}{2\pi i}\int _\gamma \frac{f _ n'(z)}{f_ n(z)}dz = 0
$$
By the uniform convergence of the $f_n$ on the compact $\gamma$, we now bring in the limit to obtain
$$
\frac{1}{2\pi i}\int _\gamma \frac{f'(z)}{f(z)}dz = 0
$$
wherein the [[Argument Principle]] once again applies this time to $f$ so that (since we already have that $f$ has no poles by it being holomorphic) $f$ must have no zeros inside $\gamma$, contradicting our assumption about $z_0$. Thus, we conclude that $f$ is non-vanishing, finishing the proof. $$\tag*{$\blacksquare$}$$ _________________________________________________________________ 
_________________________________________________________________ 

# #7
![[Pasted image 20250620175235.png]]

***Proof***: 
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 
