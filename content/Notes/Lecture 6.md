---
id: "DG6"
tags:
  - DiffGeom
---
>[!Definition]
>Let $f:S\mapsto \mathbb{R}^n$ be a differentiable function. Fix $p\in S$, $v\in T_pS$. Then, $\exists \alpha:(-\epsilon,\epsilon)\mapsto S$ such that $\alpha(0)=p$, $\alpha'(0)=v$. Thus,
>$$
>df_p(v)=\frac{d}{dt}\bigg|_{t=0}(f\circ \alpha)(t)
>$$

>[!Proposition]
>$df_p$ is well-defined.

>[!Proof]
>Let $\overline{X}:U\mapsto S$ be a local chart around $p$. We have previously shown that 
>$$
>T_pS=d\overline{X}_q(\mathbb{R}^2),\quad q=\overline{X}^{-1}(p)
>$$
>Assume that $\alpha(-\epsilon,\epsilon)\subset \overline{X}(U)$. Then,  $(\overline{X}^{-1}\circ \alpha)(0)=q$ and $\alpha=\overline{X}\circ (\overline{X}^{-1}\circ \alpha)$. Taking the derivative at $t=0$,
>$$
>\alpha'(0)=\frac{d}{dt}\bigg|_{t=0}(\overline{X}\circ (\overline{X}^{-1}\circ \alpha))(t)=d\overline{X}_q((\overline{X}^{-1}\circ\alpha)'(0)) = v\\
>\implies (d\overline{X}_q)^{-1}(v)=(\overline{X}^{-1}\circ\alpha)'(0)
>$$
>But,
>$$
>(f\circ\alpha)'(0)=((f\circ\overline{X})\circ(\overline{X}^{-1}\circ \alpha))'(0)=d(f\circ \overline{X})_q((\overline{X}^{-1}\circ\alpha)'(0))=d(f\circ\overline{X})[(d\overline{X}_q)^{-1}(v)]
>$$
>So the definition of $df_p$ is independent of the choice of $\alpha$, hence it is a well-defined function.

>[!Remark]
>if $f:S\mapsto S_1$, then $\forall p \in S$, $\forall v\in T_pS$, $df_p(v)\in T_{f(p)}S_1$. Moreover,
>$$
>\begin{CD}  
>p \in S_1 @>f>> f(p) \in S_2 \\  
>@V{g \circ f}VV @VV{g}V \\  
>g(f(p)) \in S_3 @= g(f(p)) \in S_3  
>\end{CD}
>$$
>So $d(g\circ f)_p=dg_{f(p)} df$.

>[!Example]
>i) Consider a symmetric 3x3 matrix $A$, let 
>$$
>f:S_0^2(1)\mapsto \mathbb{R}\\
>p\leadsto \langle Ap,p\rangle
>$$
>A critical point of a function is a point $p\in S_0^2$ such that $df_p=0$.  Take $v\in T_pS_0^2(1)$, then
>$$
>df_p(v)=\frac{d}{dt}\bigg|_{t=0}(f\circ\alpha)(0) = \frac{d}{dt}\bigg|_{t=0}\langle A\alpha(t),\alpha(t)\rangle\\
>=\langle Av,p\rangle + \langle Ap,v\rangle=2\langle Ap,v\rangle
>$$
>Hence, for a point $p$ to be critical, $\langle Ap,v\rangle=0$, so $Ap$ has to be orthogonal to $v$. But then $Ap=\lambda p$ since $Ap$ has to be orthogonal to any tangent vector $v\in T_pS^2_0(1)$ and this is only the case for $p$ up to rescaling by $\lambda$. Moreover, 
>$$
>\langle Ap,p\rangle = \langle \lambda p, p\rangle = \lambda \langle p, p\rangle = \lambda = f(p)
>$$
>Hence, $p$ is a critical point for $f$ iff $Ap=f(p)p$.
>ii) If $f$ is a constant function, then $A=\mu I_0$ for some scalar $\mu$.
>iii) If $f$ is not constant, since $S_0^2(1)$ is compact and $f$ is continuous, there exists $p_1,\,p_2\in S^2_0(1)$ which are maximum and minimum for $f$. Then, $p_1,\,p_2$ are automatically eigenvectors of norm $1$ for $A$ and are critical points for $f$.

>[!Claim]
>$p_1\perp p_2$.

>[!Proof]
>Notice that 
>$$
>\underbrace{(f(p_1)-f(p_2))}_{\neq0}\langle p_1,p_2\rangle
>= f(p_1)\langle p_1,p_2\rangle-f(p_2)\langle p_1,p_2\rangle = \langle f(p_1)p_1,p_2\rangle - \langle p_1,f(p_2)p_2\rangle\\
>\langle Ap_1,p_2\rangle - \langle p_1, Ap_2\rangle = A (\langle p_1,p_2\rangle-\langle p_1,p_2\rangle) = 0 \implies \langle p_1,p_2\rangle =0
>$$

>[!Example]
>Let $S\subset \mathbb{R}^3$, $p_0\in\mathbb{R}^3$, and let
>$$
>f:S\mapsto \mathbb{R}\\
>p\leadsto |p-p_0|^2
>$$ 
>Then, for some $v\in T_pS$, 
>$$
>df_p(v)=\frac{d}{dt}\bigg|_{t=0}(f\circ\alpha)(t)=\frac{d}{dt}\bigg|_{t=0}|\alpha(t)-p_0|^2=\frac{d}{dt}\bigg|_{t=0}\langle \alpha(t)-p_0,\alpha(t)-p_0\rangle\\
>= \langle v,p-p_0\rangle + \langle p-p_0,v\rangle=2\langle v, p-p_0\rangle
>$$
>So for $p$ to be a critical point of $f$, $v$ has to be orthogonal to $p-p_0$. Rewording this statement, we conclude that for $p$ to be a critical point, a normal passing through $p$ has to also pass through $p_0$. 

>[!Remark]
>If $S$ is compact then there are at least 2 critical points. Moreover, if $\exists p_0\in S$ such that each normal passes through $p_0$ then $S\simeq S_{p_0}^2(r)$.