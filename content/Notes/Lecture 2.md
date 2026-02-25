>[!Remark]
>Recall that we have $\alpha:I\mapsto \mathbb{R}^3$ with $t_0\in I$ depicted by: 
>
>![[Pasted image 20260225002502.png]]

>[!Definition]
>Let $s:I\mapsto\mathbb{R}$ be defined by $s(t)=\int^t_{t_0}|\alpha'(u)|du = L^t_{t_0}(\alpha)$. The function $u\mapsto |\alpha'(u)|$  is in general just continuous, not necessarily differentiable or $C^{\infty}(I)$.  Hence, $s$ in general is just $C^1(I)$, as due to the fundamental theorem of calculus, $s'(t)=|\alpha'(t)|$.  In particular, $s$ is not a diffeomorphism, unless $|\alpha(t)|\neq 0\;\forall t\in I$.  In that specific scenario, $s$ is a diffeomorphism between $I$ and $s(I)$.  Such curves are called **regular**. This leads to the fact that $s$ is $C^\infty(I)$. Call $J=s(I)$ and $\phi=s^{-1}$ an inverse of $s$ such that $\phi\circ s = \rm id_{I}$. Now, define $\beta(s)=\alpha \circ \phi:J\mapsto\mathbb{R}^3$. Then, using the chain rule,
>$$
>\beta'(s)=\alpha'(\phi(s))\phi'(s)=\frac{\alpha'(\phi(s))}{|\alpha'(\phi(s))|}\implies |\beta(s)| = 1\;\forall s \in J
>$$
>Such that the "velocity" of the curve $\beta$ is constant at any point in time.

>[!Definition]
>$\alpha:I\mapsto \mathbb{R}^3$ is *parameterised by arc length* (p.a.l.) if $|\alpha'(t)=1\;\forall t\in I$.

>[!theorem] 
>Every regular curve can be parameterised by an arc length. 

>[!Remark] 
>$s$ is not unique, as it depends on the choice of $t_0\in I$ and on the constant of integration.

>[!Example] 
>i) Lines: let $\alpha(t)=t\overline{v}+\overline{v}_0$. Fixing $t_0=0$. For a curve to be regular, $|\alpha'(t)\neq 0\;\forall t\in I$. Thus, since $\alpha'(t)=\overline{v}$, when $\overline{v}\neq0$, $\alpha$ is a regular curve. Then, 
>
>$$
>s(t)=\int^t_0 |\overline{v}|du = t\overline{v}\implies \phi(s) = \frac{s}{|\overline{v}}\implies \beta(s)=\alpha\circ\phi(s)=\frac{\overline{v}s}{|\overline{v}|}+\overline{v}_0
>$$ 
>Clearly, the norm of $\beta$ is constant, hence it is p.a.l.
>ii) Now consider a logarithmic spiral $\alpha(t):\mathbb{R}\mapsto \mathbb{R}^2$, defined by $t\mapsto(ae^{bt}\cos t, ae^{bt}\sin t)$.
>
>![[Pasted image 20260225010833.png]]
>Observe that:
>$$
>s(t) = \int^t_0 |(a(be^{bt}\cos t - e^{bt}\sin t), (a(be^{bt}\sin t + e^{bt}\cos t)))dt = \int^t_0 a e^{bt}\sqrt{b^2+1}
>$$
>Clearly, $\alpha'(t)=a e^{bt}\sqrt{b^2+1}> 0 \;\forall t\in I$ so the curve is regular.
>

>[!Remark]
>Let $T(s)=\alpha'(s)$ where $\alpha$ is p.a.l. and $|T(s)|=1$. It is a trivial fact that $\langle T(s),T(s)\rangle =0$. As the inner product is linear, taking a derivative with respect to $s$ leads to 
>$$
>\langle T'(s),T(s)\rangle + \langle T(s), T'(s)\rangle = 0 \implies 2 \langle T(s),T'(s)\rangle = 0 \implies \langle T(s),T'(s)\rangle = 0
>$$
>where we have used the fact that the inner product is symmetric. Hence, $\forall s\in J$, $T'(s)$ is *orthogonal* to $T(s)$.

>[!Definition]
>$$
>N(s)=\frac{T'(s)}{|T'(s)|}=\frac{T'(s)}{k(s)}
>$$
>is the **normal vector** to $\alpha$ at a point $s\in J$. Moreover,
>$$
>B(s)=T(s)\wedge N(s)
>$$
>is the **binormal vector** to $\alpha$ at a point $s\in J$. Then, $\{B(s),T(s),N(s)\}$ form an *orthonormal basis* on $\mathbb{R}^3$, usually called a **Frenet' basis**.
