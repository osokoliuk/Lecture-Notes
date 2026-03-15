---
id: "DG10"
tags:
  - DiffGeom
---
>[!Remark]
>Let 
>$$
>f:S\mapsto\mathbb{R}\\
>p\leadsto |p-p_0|^2
>$$
>Recall that $p$ is a critical point if and only if $p_0\in p+\lambda N(p)$. Then,
>$$
>(d^2f)_p=\frac{d^2}{dt^2}\bigg|_{t=0}|\alpha(t)-p_0|^2=\frac{d}{dt}\bigg|_{t=0}2\langle \alpha'(t),\alpha(t)-p_0\rangle = 2\langle \alpha''(0),p-p_0\rangle + 2 |v|^2\\
>\implies (d^2f)_p=2(|v|^2-\lambda \langle \alpha''(0),N(p)\rangle)=2(|v|^2-\lambda \mathrm{II}_p(v))

>[!Corollary] 
>If $S$ is compact then $\exists p\in S$ such that $K(p)\geq 0$.

>[!Proof]
>Since $S$ is compact, $\exists p_1,p_2\in S$ where $p_1$ is a minimum for $f$ and $p_2$ is a maximum. But then,
>$$
>(d^2f)_{p_1}>0\implies (2|v|^2-\lambda\mathrm{II}_{p_1}(v))>0\implies |v|^2>\lambda \mathrm{II}_{p_1}(v)\implies \lambda \mathrm{II}_{p_1}(v)\leq 0\\
>(d^2f)_{p_2}>0\implies (2|v|^2-\lambda\mathrm{II}_{p_2}(v))>0\implies |v|^2>\lambda \mathrm{II}_{p_2}(v)\implies \lambda \mathrm{II}_{p_2}(v)\geq 0
>$$
>So, if from the choice of $N$, $\lambda$ is negative, the point $p_1$ has a non-negative Gaussian curvature, on the other hand, if $\lambda\geq 0$ then $K(p_2)\geq 0$.

>[!Theorem] Hilbert's Theorem
>Let $S$ be an oriented regular surface, $k_1\leq k_2$ be the principle curvatures. Suppose that there exists a point $p\in S$ such that:
>1) $K(p)>0$
>2) $k_1$ has a local minimum at $p$
>3) $k_2$ has a local maximum at $p$
>
>then $p$ is an umbilical point.

>[!Proof]
>We can suppose that $p=(0,0,0)$, $N(p)=(0,0,1)$ due to the rotation/translation invariance. Moreover, assume that $e_1=(1,0,0),\;e_2=(0,1,0)$ are the principal direction to the same argument. Around $p$, $S$ is locally a graph of a function with $f(0,0)=0$. We can construct a local chart $\overline{X}(u,v)=(u,v,f(u,v))$. Then, without the loss of generality, since $T_pS$ is a horizontal plane, $f_u(0,0)=f_v(0,0)=0$. But then, $\overline{X}_u=e_1$, $\overline{X}_v=e_2$. Hence, 
>$$
>e = \frac{f_{uu}}{\sqrt{1+f_u^2+f_v^2}},\quad f = \frac{f_uv}{\sqrt{1+f_u^2+f_v^2}},\quad g = \frac{f_{vv}}{\sqrt{1+f_u^2+f_v^2}}
>$$
>with $f_{uu}(0,0)=k_1(p)$, $f_{uv}(0,0)=0$, $f_{vv}(0,0)=k_2(p)$. Define, 
>$$
>\alpha(u)=\overline{X}(u,0),\quad \beta (v)=\overline{X}(0,v)\\
>E_1(u)=\frac{\overline{X}_u(0,v)}{|\overline{X}_u(0,v)|},\quad E_2(v)=\frac{\overline{X}_v(u,0)}{|\overline{X}_u(0,v)|}
>$$
>Clearly,
>$$
>\overline{X}_u(0,v)=T_{\beta(v)}S,\quad  \overline{X}_v(u,0)=T_{\alpha(u)}S\\
>k_1(v)=\mathrm{II}_{\beta(v)}(E_1(v),E_1(v)),\quad k_2(v)=\mathrm{II}_{\alpha(u)}(E_2(u),E_2(u))
>$$
>As $E_1,\;E_2$ are linear as well as the second fundamental form, 
>$$
>k_1(v)=\frac{f_{uu}}{\sqrt{1+f_u^2+f_v^2}}\frac{1}{1+f_u^2}(u,0),\quad k_2(u)=\frac{f_{vv}}{\sqrt{1+f_u^2+f_v^2}}\frac{1}{1+f_v^2}(0,v)\\
>\implies k_1(0)=\mathrm{II}_p(e_1),\quad k_2(0)=\mathrm{II}_p(e_2)
>$$
>Finally, we know that $k_2$ has a maximum at $p$ and $k_1$ has a minimum at $p$, hence,
>$$
>k_2(0)\geq k_2(\alpha(u))\geq \mathrm{II}_{\alpha(u)}(E_2(u))=k_2(u)\;\forall u \in\mathbb{R}\\
>k_1(0)\leq k_1(\beta(v))\leq \mathrm{II}_{\beta(v)}(E_1(v))=k_1(v)\;\forall v \in\mathbb{R}
>$$
>Hence, $k''_1(0)\leq 0 \leq k_2''(0)$ but
>$$
>k_2'(u)=\bigg[-2(1+f_v^2)^{-2}f_vf_{vu}(1+f_u^2+f_v^2)^{-1/2}f_{vv}-\frac{1}{2}(1+f_u^2+f_v^2)^{-3/2}(1+f_v^2)^{-1}f_{vv}(2f_uf_{uu}+2f_vf_{uv})\\
>+(1+f_u^2+f_v^2)^{-1/2}(1+f_v^2)^{-1}f_{vvu}\bigg](u,0)\\
>\implies k_2''(0)=-f_{vv}(0)f_{uu}^2(0)+f_{vvuu}(0),\quad k_1''(0)=-f_{vv}^2(0)f_{uu}(0)+f_{vvuu}(0)\\
>\implies k_2''(0)-k_1''(0)=-f_{vv}(0)f_{uu}^2(0)+f_{vv}(0)f_{uu}(0)\\
>=f_{uu}(0)f_{vv}(0)(f_{vv}(0)-f_{uu}(0))=k_1(p)k_2(p)(k_2(p)-k_1(p))=K(p)(k_2(p)-k_1(p))\leq 0
>$$
>But our initial assumption was that $K(p)>0$ and thus the only possibility for the above inequlity to hold is that $k_2(p)=k_1(p)$, which is exactly the definition of an umbilical point.

>[!Corollary]
>Let $S$ be a compact and connected regular surface, $K>0$, suppose that $H$ is constant. Then, $S$ is a sphere.

>[!Proof]
>Let $c\in\mathbb{R}$ such that $H(p)\equiv c\;\forall p\in S$. Clearly, $c\neq 0$, otherwise $k_1=-k_2$ and hence $K\leq 0$, which is a contradiction to our initial assumption. We firstly claim that $S$ is an orientable surface. To show that, notice that the choice of $c$ depends on $N$. If at some point in $S$, the sign of $N$ switches (which would mean that $S$ is non-orientable), then $H(p)\neq c$, a contradiction. Hence, $S$ is orientable. But then, $k_1,k_2:S\mapsto \mathbb{R}$ are glovally defined functions, they are well-defined and continuous. Take $p$ such that $k_1$ has a local minimum at $p$. Notice that $p$ is automatically a local maximum for $k_2$ because $H$ is constant. Then, via the Hilbert's theorem, $p$ is umbilical. Now, take another point $q\in S$. Trivially, $k_2(q)\leq k_2(p)=k_1(p)\leq k_1(q)$. The only possibility is that $k_2(q)=k_1(q)$, hence $q$ is umbilical. The choice of $q$ was arbitrary, so all of the points in $S$ are umbilical. Since the surface is connected and compact, $S$ is a sphere.

>[!Corollary]
>Let $S$ be compact and connected. If $K$ is a positive constant, then $S$ is a sphere.

>[!Proof]
>Proven in a similar way as the previous corollary.