# #1

![[Pasted image 20250802180124.png]]

***Proof***: We begin by going by way of contradiction. To this end, we suppose there exists $\epsilon>0$ such that for all $n$
$$
\mu(\{ x: |f_{n}-f|>\epsilon \})\geq \epsilon
$$
Call the above referenced set $A_\epsilon$Consider 
$$
\lim _{ n \to \infty } \int_{X} |f_{n}-f| dm 
$$
Note the integrand bound has the clear pointwise limit of 0 directly from a. e. convergence of $f_n\to f$. Moreover
$$
|f _{n}-f|\leq |f_{n}|+|f| \leq F + F = 2F
$$
wherein the pointwise convergence of the $f_n$ guarantees $|f|\leq F$. So the [[Dominated Convergence Theorem]] applies to obtain:
$$
\lim _{ n \to \infty } \int_{X} |f _{n}-f| dm = \int_{X}0 dm = 0 
$$
On the other hand,
$$
\int _{X}|f_{n}-f| dm = \int _{X \setminus A_{\epsilon}}|f_{n}-f|dm + \int_{A_{\epsilon}}|f_{n}-f|dm
$$
By definition though,
$$
\int _{X \setminus A_{\epsilon}}|f _{n}-f|dm + \int_{A _{\epsilon}}|f_{n}-f|dm\geq \int _{X\setminus A_{\epsilon}}|f _{n}-f|dm + \int_{A _{\epsilon}}\epsilon \ dm \geq \int _{X \setminus A _{\epsilon}}|f_{n}-f|dm + \epsilon^2 > 0
$$
Since this holds for all $n$, the above $L^1$ convergence has been contradicted. Thus, we conclude the desired result.
$$\tag*{$\blacksquare$}$$ 
_________________________________________________________________ 

# #3

![[Pasted image 20250802182546.png]]

***Proof***: 
