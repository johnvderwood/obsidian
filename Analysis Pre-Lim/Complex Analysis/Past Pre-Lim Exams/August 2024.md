# #2
![[Pasted image 20250725224546.png]]

***Proof***: Let $f$ have the given conditions. It is immediate that $f$ cannot be constant by the given conditions. By the Fundamental Theorem of Algebra, we may write $f(z)=z^2\left( z-\frac{1}{2} \right)g(z)$ where $g$ is holomorphic and non-vanishing on $B(0,2)$. Since $1- \frac{1}{2}z$ is non-zero on $B(0,2)$, we may additionally write 
$$
f(z)=\frac{z^2\left( z-\frac{1}{2} \right)}{1-\frac{1}{2}z}h(z)
$$
where $h$ is holomorphic and non-zero on $B(0,2)$. Then letting $|z|=1$, 
$$
1=|f(z)|=|z^2|\cdot \left|\frac{z-\frac{1}{2}}{1-\frac{1}{2}z}\right|\cdot|h(z)|\implies |z^2||h(z)|=1 \implies |h(z)|=1
$$
By this fact, we observe that $h(z)$ is a non-vanishing holomorphic function on $\overline{\mathbb{D}}$ so that it observes the Maximum Modulus Principle. Moreover, the Maximum Modulus Principle may additionally be applied to $1/h$, yielding $1\leq |h(z)|\leq 1$ for all $z\in\mathbb{\overline{D}}$. Since then $h$ attains its maximum within the disc, $h$ must be a constant value. In particular, as it has modulus 1, $h$ must be a rotation of the form $e^{i\theta}$ for some $\theta\in[0,2\pi)$. Thus, we may characterize $f$ as:
$$
f(z)=e^{i\theta} \cdot z^2 \cdot \frac{{z-\frac{1}{2}}}{1-\frac{1}{2}z}
$$
$$\tag*{$\blacksquare$}$$ _________________________________________________________________ 

# #4
![[Pasted image 20250725231634.png]]

***Proof***: 