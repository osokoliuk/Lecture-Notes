
>[!Definition] 
>i) A **differentiable curve** ($C^\infty$) is a map $\alpha: I \mapsto \mathbb{R^3}$ where $I=(a,b)\subset \mathbb{R}$ such that $\alpha \in C^\infty(I)$. Hence,
>$$\alpha(t)= (x(t),y(t),z(t))$$
> with $x(t),y(t),z(t)\in C^{\infty}(I)$.
ii) A **tangent vector** of $\alpha$ at a point $t\in I$ is $\alpha'(t)=(x'(t),y'(t),z'(t))$
iii) $\alpha$ is called **planar** if there exists $P\subset \mathbb{R}^3$ with $\alpha(I)\subset P$. By rigid motion (linear change in coordinates), 
$$\alpha (t) = (x(t),y(y),z(t))$$


>[!Remark] 
>i) $\alpha$ is not required to be injective, e.g., if $\alpha (t) = (t^3-4t,4-t^2)$ then $t_{1,2}=\pm 2$ which implies that $\alpha(t_1)=(0,0)=\alpha(t_2)$.
ii) $\alpha$ could have corners, e.g. $\alpha (t) = (t^2, t^3)$.
![[Pasted image 20260224210137.png]]
    Here, clearly $\alpha(I)$ is the graph for $f(x)=x^{2/3}$ which is not infinitely-differentiable.
iii) Even if $\alpha$ is injective, $\alpha$ could be not a homeomorphism onto its image, e.g. $\alpha:(-1,\infty)\mapsto \mathbb{R}^2$ such that 
    $$\alpha(t) = \bigg(\frac{3t}{1+t^3},\frac{3t^2}{1+t^3}\bigg)$$
    In that case, any neighborhood of $(0,0)$ will not be homeomorphic to a line.


>[!Example]
>i) Parameterised curve: $\alpha(t)=t\overline{v}+\overline{v}_0$ with $\overline{v},\overline{v}_0\in \mathbb{R}^3$ and $t\in\mathbb{R}$ describes a line.
  ii) Circles: $\alpha(t)=\overline{c}+r(\cos t/r + \sin t/r)$ with $\overline{c}\in \mathbb{R}^2$, $r>0$ and $t\in \mathbb{R}$. Here $t/r$ is chocen for further convenience and the factor $1/r$ can be absorbed into $t$ as it is an arbitrary parameter. 
>iii) Helices:
>$$   
>\alpha(t) = \bigg(a\cos \frac{t}{\sqrt{a^2+b^2}},a\sin\frac{t}{\sqrt{a^2+b^2}},\frac{bt}{\sqrt{a^2+b^2}}\bigg)
>$$
>with $a,b\neq 0$ and $t\in\mathbb{R}$.


>[!Definition]
>Given $\alpha:I\mapsto \mathbb{R}^3$, $[a,b]\in I$, what is $L(\alpha[a,b])?$ There is a partition of $[a,b]$, i.e. a choice $P=\{a=t_0<...<t_n=b\}$. Then,  $L_a^b(\alpha,P) = \sum ^n_{i=1}|\alpha(t_i)-\alpha(t_i-1)|$
One can then make the partition infinitesimally fine such that $|P|=\max _{1\leq i \leq n}|t_i-t_{i-1}|\ll 1$ (the "norm" is small as long as partition is fine enough)

>[!Theorem]
>$\forall \epsilon <0$, $\exists \delta >0$ such that $|P|<\delta$, then,
>$$
>\bigg | L^b_a(\alpha,P)-\int ^b_a |\alpha'(t)|dt\bigg | < \epsilon
>$$
>Hence, for fine enough partition, the measure of length converges to the given integral.

>[!Definition] 
>The length of a curve $\alpha$ is defined as $L^b_a(\alpha)=\int^b_a|\alpha'(t)|dt$.

>[!Proof]
>Define $f: I\times I\times I \mapsto \mathbb{R}$ by
>  $$
>    (t_1,t_2,t_3)\mapsto \sqrt{x'(t_1)+y'(t_1)+z'(t_3)}
> $$
>    Note that
>    $$
>    |\alpha'(t)|=\sqrt{x'(t)+y'(t)+z'(t)}
>    $$
>    Clearly, $f$ is continuous, hence it is uniformly continuous on compact subsets. So, $\forall \epsilon>0$, $\exists \delta >0$ such that if $t_1,t_2,t_3$ and $(s_1,s_2,s_3)\in [a,b]^3$ with
>    $$
>    \begin{cases}
>|t_1-s_1|<\delta\\
>|t_2-s_2|<\delta \\
>|t_3-s_3|<\delta
>\end{cases}
>  $$
>    then $|f(t_1,t_2,t_3)-f(s_1,s_2,s_3)|<\epsilon$. By the mean value theorem, 
>    $$
>    |\alpha'(t_i)-\alpha'(t_{i-1})|=f(\beta_i,\gamma_i,\delta_i)(t_i-t_{i-1})
>   $$
>    for some $\beta_i,\gamma_i,\delta_i\in [t_{i-1},t_i]$. Now,
>    $$
>     L^b_a(\alpha,P)=\sum^n_{i=1}|\alpha(t_i)-\alpha(t_{i-1})|\\
>    = \sum^n_{i=1}f(\beta_i,\gamma_i,\delta_i)(t_i-t_{i-1})
>    $$
>    But
>    $$
>    \int^b_a |\alpha'(t)|dt = \sum^n_{i=1}\int^{t_i}_{t_{i-1}}|\alpha'(t)|dt
>    $$
>    So again, by the mean value theorem, 
>    $$
>    \int^b_a|\alpha'(t)|dt = \sum^n_{i=1}|\alpha'(\xi_i)|(t_i-t_{i-1})\\
>    = \sum^n_{i=1}|f(\beta_i,\gamma_i,\delta_i)(t_i-t_{i-1})
>    $$
>    We know that $|P|<\delta$ and $\xi_i\in [t_{i-1},t_i]$, hence $\xi_i<\delta$. But $\beta_i,\gamma_i,\delta_i\in[t_{i-1},t_i]$ hence $|f(\xi_i,\xi_i,\xi_i)-f(\beta_i,\gamma_i,\delta_i)|<\epsilon$ so 
>    $$
>    \bigg|L^b_a(\alpha,P)-\int^b_a|\alpha'(t)|dt\bigg|<\epsilon
>    $$

>[!Remark]
>We now want to check the invariance of the curve length under isometric transformations. If we have a curve $\alpha:I\mapsto \mathbb{R}^3$, then an isometry of $\mathbb{R}^3$ is a transformation $\phi: \mathbb{R}^3\mapsto \mathbb{R}^3$ such that $d(p,q)=d(\phi(p),\phi(q))\;\forall p,q\in \mathbb{R}^3$. Therefore, $\phi$ is, up to translation, an orthogonal transformation (if $\phi$ is represented by a matrix $A$, then $AA^T=I_3$).

>[!Example]
>Consider a curve $\alpha:I\mapsto \mathbb{R}^3$ with $[a,b]\in I$. Then,
$$
|\alpha(a)-\alpha(b)| = \bigg|\int^b_a\alpha'(t)dt\bigg|\leq \int^b_a|\alpha'(t)|dt=L^b_a(\alpha)
$$
 The minimum for $L^b_a(\alpha)$ is achieved if and only if $\alpha$ is a parameterised curve for a line.
    
>[!Definition]
>A **diffeomorphism** $\phi:J\mapsto I$ with $I$ and $J$ being open intervals is a $C^\infty(J)$ map which is also invertible with a $C^\infty(I)$ inverse. Given $\alpha:J\mapsto \mathbb{R}^3$ we can construct a new map $\beta:J\mapsto \mathbb{R}^3$. In that case, $\beta$ is called a **reparameterisation** of $\alpha$.

>[!Proposition]
>Let $\phi:J\mapsto I$ be a diffeomorphism, $\alpha:J\mapsto \mathbb{R}^3$, $[a,b]\subset J$, $\phi([a,b])=[c,d]$. Then, $L^b_a(\alpha \circ \phi) = L^d_c(\alpha)$.

>[!Proof]
>Note that $|(\alpha\circ \phi)'(t)|=|\alpha'(\phi(t))||\phi'(t)|dt$ with $ds = |\phi'(t)|dt$. In the case when $\phi'(t)>0$,
>$$
>s = \int^d_c\bigg|\frac{d\alpha(s)}{ds}\bigg|ds
>$$