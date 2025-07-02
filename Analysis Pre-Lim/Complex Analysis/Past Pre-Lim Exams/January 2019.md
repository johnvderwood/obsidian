# #1
![[Pasted image 20250629192256.png]]

***Proof***: We follow the following contour which we will call $\gamma$ for the function $f(z)=\sqrt{z}/({1+z^2})$ with a choice of $R>1, \ 0<r<1$:

![[Pasted image 20250702183416.png]]

Explicitly then, we are computing:
$$
\int_{\gamma}f(z)dz = \sum_{i=1}^4
\int_{\gamma_{i}}f(z)dz$$
Note that, since $f$ has one simple pole at $z=i$ and is otherwise holomorphic on and within the selected contour (with a branch cut choice along the negative imaginary axis; angles from $[-\frac{\pi}{2},\frac{3\pi}{2})$), by the Residue Theorem, we have
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

_________________________________________________________________ 

# #3 
![[Pasted image 20250629192343.png]]

***Proof***: 

_________________________________________________________________ 

# #5 
![[Pasted image 20250629192420.png]]

***Proof***: 

_________________________________________________________________ 

# #7
![[Pasted image 20250629192456.png]]

***Proof***: 

_________________________________________________________________ 
# #9
![[Pasted image 20250629192521.png]]

***Proof***: 

_________________________________________________________________ 
