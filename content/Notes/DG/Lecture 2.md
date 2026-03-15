---
id: "DG2"
tags:
  - DiffGeom
---
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
>$\alpha:I\mapsto \mathbb{R}^3$ is *parameterised by arc length* (p.a.l.) if $|\alpha'(t)|=1\;\forall t\in I$.

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

>[!Definition] Frenet' Formula
>$$
>N(s)=\frac{T'(s)}{|T'(s)|}=\frac{T'(s)}{k(s)}
>$$
>is the **normal vector** to $\alpha$ at a point $s\in J$ and $k(s)$ is the **curvature** of $\alpha$ at $s\in J$. Moreover,
>$$
>B(s)=T(s)\wedge N(s)
>$$
>is the **binormal vector** to $\alpha$ at a point $s\in J$. Then, $\{B(s),T(s),N(s)\}$ form an *orthonormal basis* on $\mathbb{R}^3$, usually called a **Frenet' basis** with each element being $C^\infty(J)$. Note that, 
>$$
>T'(s) = k(s)N(s)\\
>B'(s) = \tau(s)N(s)\\
>N'(s) = -k(s)T(s)-\tau(s)B(s)
>$$
>where $\tau(s)$ is the **torsion** of $\alpha$ at $s\in J$. It is simply $\tau(s)=\langle B'(s),N(s)\rangle$, i.e. a projection of $B'(s)$ onto $N(s)$.

>[!Example] 
>i) Lines: Let $\alpha(t)=t\overline{v}+\overline{v}_0$ be a p.a.l. curve. Then,
>$$
>T(t) = \alpha'(t)= \overline{v}\implies T'(t)=0\implies k(t)=0\;\forall t\in I
>$$
>so as expected, a line is flat everywhere.
>ii) Circles: Let $\alpha(t)=r(\cos(t/r),\sin(t/r),0)+\overline{c}$. Then,
>$$
>T(t) = \alpha'(t) = (-\sin(t/r),\cos(t/r),0)
>$$
>Observe that $|T(t)|=1$ everywhere which makes $\alpha$ p.a.l. Moreover, 
>$$
>T'(t) = \frac{1}{r}(-\cos(t/r),-\sin(t/r),0)\implies k(t)=|T'(t)| = \frac{1}{r}
>$$
>so the curvature is constant. Finally,
>$$
>N(t)=\frac{T'(t)}{k(t)}=(-\cos(t/r),-\sin(t/r),0)\\
>B(t) = T(t)\wedge N(t) = (0,0,1)\implies B'(t)=0\implies \tau(s)=0
>$$
>so a circle has a vanishing torsion but non-vanishing curvature.
>iii) Helices: we are just going to state that  
>$$
>k(t) = \frac{|a|}{a^2+b^2},\quad \tau(s)=\frac{b}{a^2+b^2}
>$$
>so both curvature and torsion are non-vanishing in the scenario when $a,b\neq0$ which is assumed a priori.

>[!Theorem] 
>Let $\alpha:I\mapsto \mathbb{R}^3$, p.a.l. with $k>0$. Then, $\alpha$ is planar iff $\tau=0$.

>[!Proof]
>Suppose that $\tau=0$. Then, $|B'(t)|=0$, so $B(t)=\overline{u}$, some constant vector. Then, 
>$$
>\langle \alpha(t), \overline{u}\rangle'=\langle \alpha'(t),\overline{u}\rangle + \langle \alpha(t),0\rangle =\langle \overline{v},\overline{u}\rangle + \langle \alpha(t),0\rangle= 0
>$$
>using the fact that $B(t)$ is orthogonal to $\alpha$ at any point in time. Then, $\langle \alpha(t),\overline{u}\rangle = a$ with $a\in\mathbb{R}$. But that just means that $\alpha(t)$ projected onto $z$-axis for any $t\in I$ is constant, hence $\alpha(t)$ is a regular curve.

>[!Theorem]
>$\alpha:I\mapsto \mathbb{R}^3$ p.a.l. with $k=0$ iff $\alpha$ is a segment of a line.

>[!Proof]
>$\boxed{\Longleftarrow}$ Trivial.
>$\boxed{\Longrightarrow}$ Now assume that $k=0$, then $T'(t)=0$ hence $T(t)$ is a constant. But $T(t)=\alpha'(t)$ so if $T(t)$ is constant for any $t\in I$ then $\alpha'(t)=\overline{v}$ for some constant vector. Integrating, we get $\alpha(t)=t\overline{v}+\overline{v}_0$ where $\overline{v}_0$ is the constant of integration. This is an equation for a line.