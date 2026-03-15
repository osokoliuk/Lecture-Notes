---
id: "DG9"
tags:
  - DiffGeom
---

>[!Example]
>Consider an elliptic paraboloid, described by
>$$
>S = \{(x,y,z)\in \mathbb{R}^3:z=\frac{x^2+y^2}{2}\}
>$$
>
>![[Pasted image 20260313203636.png]]
>Notice that $\overline{X}(u,v)=(u,v,\frac{u^2+v^2}{2})$. Therefore,
>$$
>\overline{X}_u=(1,0,u),\quad \overline{X}_v=(0,1,v),\quad \overline{X}_{uu}=\overline{X}_{vv}=(0,0,1),\quad \overline{X}_{uv}=(0,0,0)
>$$
>Then,  pick a normal vector field
>$$
>N = \frac{\overline{X}_u\wedge\overline{X}_v}{|\overline{X}_u\wedge\overline{X}_v|} = \begin{vmatrix}1&0&u\\0&1&v\end{vmatrix}=
>frac{(-u,-v,1)}{\sqrt{u^2+v^2+1}}
>$$
>And then calculate
>$$
>E = 1+ u^2,\quad F = uv,\quad G=1+v^2\\
>e =\frac{1}{\sqrt{u^2+v^2+1}}, \quad f =0, \quad g =\sqrt{1}{\sqrt{u^2+v^2+1}} 
>$$
>Hence,
>$$
>K(\overline{X}(u,v))=\frac{1}{\sqrt{u^2+v^2+1}},\quad H(\overline{X}(u,v))=\frac{1}{2}\frac{2+u^2+v^2}{(u^2+v^2+1)^{3/2}}
>$$
>Clearly, for any $(u,v)\in U$, $K(\overline{X}(u,v))>0$ so the points are all elliptic.

>[!Example]
>Now, let us construct a helicoid.
>![[Pasted image 20260313210747.png]]
>The local chart for a helicoid is described via
>$$
>\overline{X}(u,v)=(v\cos u,v\sin u,au),\quad a\in \mathbb{R}\setminus \{0\},\; v,u\in\mathbb{R}
>$$
>Then, analogously to the previous example,
>$$
>\overline{X}_u=(-v\sin u, v\cos u, a)\\
>\overline{X}_v=(\cos u, \sin u, 0)\\
>\overline{X}_{uu}=(-v\cos u, -v\sin u, 0)\\
>\overline{X}_{vv}=(0,0,0)\\
>\overline{X}_{uv}=(-\sin u, \cos u, 0)
>$$
>Subsequently,
>$$
>N = \begin{vmatrix}-v\sin u & v \cos u & a \\ \cos u & \sin u & 0\end{vmatrix} = \frac{(-a\sin u, a \cos u, -v)}{\sqrt{a^2+v^2}}\\
>E = v^2 + a^2, \quad F = 0, \quad G = 1\\
>e = 0, \quad f = \frac{a}{\sqrt{a^2+v^2}},\quad g = 0
>$$
>Such that,
>$$
>K(\overline{X}(u,v))=-\bigg(\frac{a}{a^2+v^2}\bigg)^2,\quad H(\overline{X}(u,v))=0
>$$

>[!Definition]
>Let $S$ be a regular surface, $f:S\mapsto \mathbb{R}$ be a $C^\infty$ function, let $p$ be a critical point for $f$. Then, 
>$$
>(d^2f)_p: T_pS\mapsto \mathbb{R}\\
>v\leadsto \frac{d^2}{dt^2}\bigg|_{t=0}(f\circ \alpha)
>$$
>is called a **Hessian** of $f$ at $p$.

>[!Proposition]
>If $f$ is critical then $(d^2f)_p$ is well-defined. Moreover,
>1) It is a quadratic form on $T_pS$
>2) If $p$ is a local maximum (minimum) then the Hessian is semidefinite negative (positive)
>3) If $(d^2f)_p$ is negative (positive) definite then $p$ is a local minimum (maximum)

>[!Proof]
>As usual, introduce a local chart on $S$ as $\overline{X}:U\mapsto S$ via $X(q)=p$, $q=(a,b)\in U$, without the loss of generality pick $\alpha(-\epsilon,\epsilon)\subset X(U)$, introduce $\beta = \overline{X}^{-1}\circ \alpha$ defined by $\beta(t)=(u(t),v(t))$. Then,
>$$
>\frac{d}{dt}(f\circ \alpha)(t)=u'(f\circ \overline{X})_u+v'(f\circ \overline{X})_v\\
>\frac{d^2}{dt^2}(f\circ \alpha)(t)=u''(f\circ \overline{X})_u + u' \left[u'(f\circ\overline{X})_{uu}+v'(f\circ \overline{X})_{uv}\right]\\
>+ v''(f\circ\overline{X})_v+v' \left[u'(f\circ\overline{X})_{uv}+v'(f\circ \overline{X})_{vv}\right]
>$$
>If the point is critical, then by the definition, $df_p=0$. hence $(f\circ\overline{X})_u=(f\circ\overline{X})_v=0$. Then we clearly see that $(d^2f)_p$ is well-defined as there are no $\alpha$-dependent quantities left. Moreover, then,
>$$
>(d^2f)_p=u'(0)^2(f\circ\overline{X})_{uu}(a,b)+2u'(0)v'(0)(f\circ\overline{X})_{u,v}(a,b)+v'(0)^2(f\circ\overline{X})_{vv}(a,b)
>$$

>[!Example]
>i) Consider a height function $h(p)=\langle p-p_0,a\rangle$:
>
>![[Pasted image 20260314161829.png | 400]]
>Clearly, one can see that $p$ is critical only in the case when $N(p)= a$. Now,
>$$
>(d^2f)_p=\frac{d^2}{dt^2}\bigg|_{t=0}\langle \alpha(t)-p_0,a\rangle = \langle \alpha''(0),a\rangle = \langle \alpha''(0),N(p)\rangle=\mathrm{II}_p(v,v)
>$$
>In the case when $P=T_pS$, $p$ is always a critical point.

>[!Theorem]
>1) If $K(p)>0$, i.e., $p$ is an elliptic point, then there exists a neighbourhood of $p$ in $S$ which lies on the same side of an **affine tangent plane** to $S$ at $p$
>2) If $K(p)<0$, i.e., $p$ is hyperbolic, then in every neighbourhood of $p$ in $S$ there are points which lie on both sides of the affine tangent plane.

>[!Remark]
>There is no such definition for $K(p)=0$.

>[!Definition]
>By affine tangent plane, it is meant that the tangent plane no longer is a vector field as it is translated to the point $p$.

>[!Example]
>$\underline{\rm Planar \;point:}$ Let $\overline{X}(u,v)=(u,v,u^3-3v^2u)$. This local charts describes a "monkey saddle" surface.
>
>![[Pasted image 20260314163207.png]]
>
>Following the usual procedure and computing the Gaussian curvature $K(p)$ at $p=\overline{X}(0,0)$,  we find that $K(p)=k_1(p)=k_2(p)=0$ so the point is planar.
>$\underline{\rm Parabolic \;point:}$
>
>![[Pasted image 20260314163727.png]]
>For the surface described by a graph above, the points along the blue dotted line are parabolic.
>