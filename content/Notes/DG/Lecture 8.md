---
id: "DG8"
tags:
  - DiffGeom
---

>[!Example] 
>Consider a cylinder described by $S=\{(x,y,z)\in\mathbb{R}^3:x^2+y^2=r^2\}$. Then, let $f(x,y)=x^2+y^2$ such that $S=f^{-1}(r^2)$. Notice that $\nabla f_p=2(x,y,0)$ so $df_p\neq 0\;\forall p \in S$, hence $r^2$ is a regular value for $f$ meaning that $S$ is indeed a regular surface. Then, we can define a normal vector field:
>$$
>N(p)=\frac{\nabla f_p}{|\nabla f_p|}=\frac{1}{r}(x,y,0)
>$$
>The surface is orientable. Then, what is
>$$
>dN_p((v_1,v_2,v_3))=\frac{d}{dt}\bigg|_{t=0}(N\circ \alpha)(t) = \frac{d}{dt}\bigg|_{t=0}\frac{1}{r}(x(t),y(t),0) = \frac{1}{r}(v_1,v_2,0)
>$$
>Hence
>$$
>\mathrm{II}_{p}(v,w)=-\langle dN_p(v),w\rangle = -\frac{1}{r}(v_1w_1+v_2w_2)
>$$
>If $v$ is a vertical vector (along the $z$-th direction), $dN_p=0$, if it is a tangent to a circle, $dN_p=\frac{v}{r}$. Finally, we note that $k_1(p)=-\frac{1}{r}$, $k_2(p)=0$, $K(p)=0$, $H(p)=-\frac{1}{2r}$.

>[!Definition]
>Take $\alpha:I\mapsto S$ with $\alpha(0)=p$ being a regular curve, $k$ is the curvature of $\alpha$ as a curve in $\mathbb{R}^3$. Moreover, define an angle between the normal vector field of a surface at that point and a normal to the curve $\overline{n}$ via $\cos\theta = \langle \overline{n},N\rangle$.
>
>![[Pasted image 20260312230102.png|400]]
>We then say that $k_n=k\cos\theta$ is the **normal curvature** of $\alpha$ at $p$. Now, suppose that $\alpha$ is p.a.l. and restrict the normal vector field $N(s)=N(\alpha(s))$. Then,
>$$
>\langle N(s),\alpha'(s)=0\implies \langle N'(s),\alpha'(s)\rangle + \langle N(s),\alpha''(s)\rangle =0\implies \langle N'(s),\alpha'(s)\rangle = - \langle N(s),\alpha''(s)\rangle
>$$
>Now,
>$$
>\mathrm{II}_p(\alpha'(0),\alpha'(0))=-\langle dN_p(\alpha'(0)),\alpha'(0)\rangle = - \langle N'(p),\alpha'(0)\rangle=\langle N(p),\alpha''(0)\rangle =\langle N(p),k(p)\overline{n}(p)\rangle \\
>=k(p)\cos \theta = k_n(p)
>$$
>So if $v\in T_pS$ with $|v|=1$ then $\mathrm{II}_p(v)$ is equal to the normal curvature of *any* curve passing through the point $p$ with velocity $v$. (Euler's Theorem)
>Now, we know that $k_1(p)$ and $k_2(p)$ are the  minimum and maximum of $\mathrm{II}_p$ restricted to the vectors of norm 1.
>
>![[Pasted image 20260312231913.png|400]]
>Here $\{e_1,e_2\}$ is an orthonormal basis of eigenvectors of $-dN_p$. But then, since $k_1\leq k_n\leq k_2$,
>$$
>v=\cos \theta e_1+\sin \theta e_2\\
>k_n^{(v)}=\mathrm{II}_p(v)=\langle - dN_p(v),v\rangle = \langle -dN_p(\cos \theta e_1+\sin \theta e_2),\cos \theta e_1+\sin \theta e_2\rangle\\
>=-\langle k_1\cos\theta e_1 + k_2\sin \theta e_2, \cos \theta e_1+\sin\theta e_2\rangle=-k_1\cos^2\theta -k_2\sin^2\theta
>$$

>[!Definition] 
>$p\in S$ is called:
>1) **elliptic** if $K(p)>0$
>2) **hyperbolic** if $K(p)<0$
>3) **parabolic** if $K(p)=0$ and either $k_1(p)\neq0$ or $k_2(p)\neq0$
>4) **planar** if $K(p)=0$ and $k_1(p)=k_2(p)=0$
>5) **umbilical** if $k_1(p)=k_2(p)$

>[!Example]
>$S^2_{p_0}*r$ is made of umbilical points.

>[!Proposition]
>If $S$ is connected and every $p\in S$ is umbilical then $S$ is contained in a plane or in a sphere.

>[!Proof]
>Consider a local chart $\overline{X}:U\mapsto S$ with $u\in T_pS$. Then,
>$$
>u = a\overline{X}_u+b\overline{X}_v
>$$
>Since every point is umbilical by definition, 
>$$
>dN_p(w) = \lambda(p)w=aN_u(p)+bN_v(p)=\lambda(p)(a\overline{X}_u+b\overline{X}_v)\;\forall a,b
>$$
>Taking two separate scenarios, $a=0$ and $b=0$, we get
>$$
>N_u(p)=\lambda(p)\overline{X}_u\\
>N_v(p)=\lambda(p)\overline{X}_v\\
>$$
>Since both $N$ and $\overline{X}$ are $C^\infty$, clearly $\lambda$ is a differentiable function. Then,
>$$
>N_{uv}=\lambda_v\overline{X}_u+\lambda \overline{X}_{uv}\\
>N_{vu}=\lambda_u\overline{X}_v+\lambda \overline{X}_{uv}\\
>\implies \lambda_u\overline{X}_v=\lambda_v\overline{X}_u
>$$
>But, as $\{\overline{X}_u\overline{X}_v\}$ forms an orthogonal basis of $T_pS$, $\overline{X}_u$ and $\overline{X}_v$ are linearly independent, so the only choice is that $\lambda_u=\lambda_v=0$ hence $\lambda$ is a constant function.  We now have two possibilities:
>1) If $\lambda=0$ then $N$ is constant so $S$ is a piece of a plane
>2) If $\lambda\neq 0$ then, integrating 
>$$
>\overline{X}(u,v)-\frac{1}{\lambda}N(u,v)=\overline{c}\implies \bigg|\overline{X}(u,v)-\overline{c}\bigg|^2=\bigg|\frac{1}{\lambda}N(u,v)\bigg|^2=\frac{1}{|\lambda|^2}
>$$
>Where we have used the fact that $N$ is a a vector field of norm 1. Above equation describes a surface for which any point is located at a distance of $|\lambda|$ from the center $\overline{c}$, hence a piece of a sphere. Due to the continuity of $\lambda$ we only have to worry about a single sphere. 

>[!Proposition]
>$K$ and $H$ are smooth functions, $k_1$ and $k_2$ are continuous which are smooth on the open sets of non-umbilical points.

>[!Proof]
>Let $\overline{X}:U\mapsto S$ be a local chart. Define a normal vector field on that chart via
>$$
>N^{\overline{X}}=\frac{\overline{X}_u\wedge\overline{X}_v}{|\overline{X}_u\wedge\overline{X}_v|}
>$$ 
>Then, $\mathrm{I}_p\leadsto M$ (represented by), $\mathrm{II}_p\leadsto \Sigma$, $dN_p\leadsto A$ with
>$$
>M = \begin{pmatrix}\mathrm{I}_p(\overline{X}_u)&\mathrm{I}_p(\overline{X}_v,\overline{X}_u)\\ \mathrm{I}_p(\overline{X}_v,\overline{X}_u)&\mathrm{I}_p(\overline{X}_v)\end{pmatrix}=\begin{pmatrix}E&F\\ F&G\end{pmatrix},\quad \Sigma = \begin{pmatrix}e&g\\ f&g\end{pmatrix},\quad A =M^{-1}\Sigma
>$$
>Via some tedious algebra, we get the components of $A$
>$$
>a_{11} = \frac{Ef-Ge}{EG-F^2},\quad a_{21}=\frac{Fe-Ef}{EG-F^2}\\
>a_{12}=\frac{Fg-Gf}{EG-F^2},\quad a_{22} = \frac{Ff-Eg}{EG-F^2}
>$$
>Recall that 
>$$
>K(p)=\det (-dN_p)=a_{11}a_{22}-a_{21}a_{12}=\frac{eF-fE}{EG-F^2}
>$$
>As $M$ is invertible, $EG-F^2\neq0$. Moreover,
>$$
>H = -\frac{\mathrm{Tr} A}{2}=\frac{1}{2}\frac{eG+gE-2fF}{EG-F^2}
>$$
>Hence we conclude that $K$ and $H$ are smooth functions. Finally, note that 
>$k_i=H\pm \sqrt{H^2-K}$. If the point is umbilical, $H=k_i$, $K=k_i^2$ amd so $H^2=K$, making the aforementioned expression for $k_i$ not differentiable but only continuous. Otherwise $k_i$ is clearly smooth as $H^2-K\neq0$.