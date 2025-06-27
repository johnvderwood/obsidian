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
$$\tag*{$\blacksquare$}$$
_________________________________________________________________ 

# #2
![[Pasted image 20250625123757.png]]

***Proof***: With the goal of employing [[Schwarz Lemma]], we want to funnel $f$ such that 0 is mapped to 0. To this end, we first consider a couple transformations:
$$
\psi(z)=\psi_{\frac{1}{2}}(z)=\frac{\frac{1}{2}-z}{1-\overline{\frac{1}{2}}z}
$$
It should be noted that this standard map from $\mathbb{D}\rightarrow \mathbb{D}$ sends 0 to $\frac{1}{2}$ and vice versa. Now we further consider 
$$
\Psi_2(z)=\psi_{f(\frac{1}{2})}(z)
$$
defined similarly. For both of these maps, we further note that they are their own inverses. Now, under the composition,
$$
\Psi(f(\psi(z)))
$$
we have a map to and from the unit disc sending 0 to 0. Thus, [[Schwarz Lemma]] applies to this composition we will call $g$. Thus, we conclude that
$$
|g'(0)|\leq 1
$$
In this way, we pass back to the composition:
$$
|\Psi'(f(\psi(0)))f'(\psi(0))\psi'(0)|\leq 1
$$
$\implies$ 
$$
|\Psi'(f(\frac{1}{2}))f'(\frac{1}{2})\psi'(0)|\leq 1 \implies |f'(\frac{1}{2})|\leq \frac{1}{|\Psi'(f(1/2))\psi'(0)|}
$$
For a generic $\alpha$
$$
\psi_\alpha'(z) = \frac{1-|\alpha|^2}{(1-\overline{\alpha}z)^2}
$$
Substituting the appropriate values, 
$$
\Psi'(f(1/2))=\frac{1}{1-|f(1/2)|^2} \ \text{ and } \ \psi'(0)=\frac{3}{4}
$$
Thus, the RHS of the before inequality becomes
$$
|f'(1/2)|\leq \frac{4(1-|f(1/2)|^2)}{3}\leq \frac{4}{3}
$$
The function $f(z)=\psi(z)$ attains this bounding value since, as per the above formula for $\psi_\alpha'(z)$, $\psi_{1/2}'(1/2)=$ 

# #8
![[Pasted image 20250626140707.png]]
hello:()