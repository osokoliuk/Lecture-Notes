>[!Example] Torus of Revolution
>Take a circle $S^1(r)$ of radius $r$ in the plane $x=0$ with a center $(0,a,0)$. Rotate this circle around $z$ axis, $\{x=y=0\}$.
>
>![[Pasted image 20260301232712.png]]
>
>Let $p=(x,y,0)$. Then, $d=a-\sqrt{x^2+y^2}$. But, $d^2+z^2=r^2$, so 
>$$
>(a-\sqrt{x^2+y^2})^2+z^2=r^2
>$$
>Clearly, this is an equation that parametrises a torus. Thus, define a function
>$$
>f: \mathbb{R}^2\setminus {z\rm -axis}\mapsto \mathbb{R}\\
>(x,y,z)\leadsto (a-\sqrt{x^2+y^2})^2+z^2
>$$
>Clearly, a surface of a torus is defined by $S=f^{-1}(r^2)$. To show that torus is a regular surface, we must show that $r^2$ is a regular value for $f$. This is equivalent to demonstrating that $df_p\neq 0\;\forall p\in f^{-1}(r^2)$.  Notice that 
>$$
>\frac{\partial f}{\partial x} = \frac{2x(\sqrt{x^2+y^2}-a)}{\sqrt{x^2+y^2}}, \quad \frac{\partial f}{\partial y} = \frac{2y(\sqrt{x^2+y^2}-a)}{\sqrt{x^2+y^2}}, \quad \frac{\partial f}{\partial z} = 2z
>$$
>Notice that if $z\neq 0 $ then automatically $df_p\neq 0$. Hence, let us consider the case when $z=0$. But the torus touches $z$ axis only in the case when $r=a$, so assuming that $a>r$ (which is usually the case for a torus), $r^2$ is a regular value for $f$, hence $S$ is a regular surface. When $a=r$,  $\sqrt{x^2+y^2}-a$ vanishes and hence torus will not be a regular surface.

>[!Definition] 
>Let $S$ be a regular surface, $\mathcal{O}$ an open set of $\mathbb{R}^3$. 
>i)$F:S\mapsto \mathbb{R}^n$ is **differentiable**  if for any local chart $\overline{X}$ of  $S$, the composition $F\circ \overline{X}$ is differentiable. 
>ii) $f:\mathcal{O}\mapsto S$ is differentiable if a coextension $f:\mathcal{O}\mapsto \mathbb{R}^3$ is differentiable.
>iii) If $S_1$ is another surface, then $f:S\mapsto S_1$ is differentiable if $f:S\mapsto \mathbb{R}^3$. $f:S\mapsto\mathbb{R}^3$ is differentiable if for any local chart $\overline{X}$ of $S$, $f\circ \overline{X}$ is differentiable. 

>[!Example]
>i) Let $f,g:S\mapsto \mathbb{R}^n$, $f+g$. Then, $f+g$, $\lambda f$, $f-g$ are differentiable if $f$ and $g$ are. Moreover, $\langle f, g\rangle$ is also differentiable.  
>ii) Let $F:\mathcal{O}\mapsto \mathbb{R}^3$ be differentiable and $S\subset \mathcal{O}$. Then, $F|_S$ is differentiable. In particular, the inclusion $\iota: S\mathbb{R}^3$ and $\mathrm{id}:S\mapsto S$ are differentiable functions.
>iii) Let $P\subset \mathbb{R}^3$ be a plane, take $p_0\in P$. Suppose that $\overline{a}$ is a normal vector at $p$. Then, we can define a **height function**:
>$$
>h:S\mapsto \mathbb{R}\\
>p\leadsto \langle p-p_0,\overline{a}\rangle
>$$
>
>![[Pasted image 20260301235613.png|500]]
>$h$ is differentiable.
iv) Consider a distance function $f(p)=|p-p_0|$. This function is differentiable if $(x-x_0)^2+(y-y_0)^2+(z-z_0)^2\neq 0$. With $p\notin S$, define $f:\mathbb{R}^2\setminus\{p_0\}\mapsto \mathbb{R}$, it is clearly differentiable. 

>[!Proposition]
>Let $f:S\mapsto \mathbb{R}^n$. If $\forall p\in S$, $\exists \overline{X}_p:U_p\mapsto S$, namely a local chart around $p$ such that $f\circ \overline{X}_p:U_p\mapsto \mathbb{R}^n$ is differentiable, then $f$ is differentiable.

>[!Proof]
>$\boxed{\Longleftarrow}$ Trivial. If $f$ is differentiable, it is differentiable on all of the local charts of $S$.
>$\boxed{\Longleftarrow}$ Let $f\circ \overline{X}_p$ be differentiable $\forall p \in  S$.  Now, consider another local chart of $p$, $\overline{Y}_p:V\mapsto S$. We want to show that $f\circ \overline{Y}_p$ is also differentiable. To see that, firstly introduce a differentiable function $\phi = \overline{X}^{-1}_p\circ \overline{Y}_p$. It is differentiable since both $\overline{X}^{-1}_p$ and $\overline{Y}_p$ are. Then, notice that since all local charts are bijections, we can do the following
>$$
>f\circ \overline{Y}_p=\underbrace{(f\circ \overline{X}_p)}_{C^\infty}\circ\underbrace{(\overline{X}_p^{-1}\circ \overline{Y}_p)}_{C^\infty}
>$$
>One can clearly see that $f\circ \overline{Y}_p$ is indeed differentiable, as required.

>[!Definition]
>Let $S$ be a regular surface, $p\in S$. We say that $v\in \mathbb{R}^3$ is a **tangent vector** to $S$ at $p$ if $\exists \alpha:(-\epsilon,\epsilon)\mapsto S$ which is differentiable, $\epsilon>0$, such that $\alpha(0)=p$, $\alpha'(0)=v$. The set of tangent vectors to $S$ at $p$ is denoted by $T_pS$.

>[!Lemma]
>If $\overline{X}:U\mapsto S$ is a local chart of $S$ around $p$ then $T_pS=d\overline{X}_{\overline{X}^{-1}(p)}(\mathbb{R}^2)$.

>[!Proof]
>Let $w\in\mathbb{R}^2$ be any vector and introduce $\beta(t)=\overline{X}^{-1}(p)+tw$ with $\beta:(-\epsilon,\epsilon)\mapsto U$.
>
>![[Pasted image 20260302025915.png]]
>
>Now, define $\alpha:(-\epsilon,\epsilon)\mapsto S$ by $\alpha=\overline{X}_p\circ \beta$. Then, $\alpha(0)=\overline{X}\circ\overline{X}^{-1}(p)=p$. Moreover, from the definition of the differential,
>$$
>d\overline{X}_{\overline{X}^{-1}(p)}(w)=\frac{d}{dt}\bigg|_{t=0}(\overline{X}\circ \beta)=\frac{d}{dt}\bigg|_{t=0}\alpha(t)=\alpha'(0)\in T_pS
>$$
>Now, let $v\in T_pS$. Then, $\exists \alpha:(-\epsilon,\epsilon)\mapsto S$ such that $\alpha(0)=p$ and $\alpha'(0)=v$. But then by choosing small enough $\epsilon$, $\alpha(-\epsilon,\epsilon)\subset \overline{X}(U)$. Put $\beta = \overline{X}^{-1}\circ\alpha$ defined as  $\beta:(-\epsilon,\epsilon)\mapsto U$. Notice that 
>$$
>\beta(0)=\overline{X}^{-1}(p), \alpha = \overline{X}\circ \beta\implies \alpha'(0)=(\overline{X}\circ\beta)'(0)=d\overline{X}_{\overline{X}^{-1}(p)}(\beta'(0))
>$$
>$\beta'(0)\in\mathbb{R}^2$ so this ends the proof.

>[!Corollary]
>i) $T_pS$ is a vector space
>ii) $T_pS$ is generated by $\left\{\dfrac{\partial \overline{X}}{\partial u},\dfrac{\partial \overline{X}}{\partial v}\right\}$

>[!Example]
>let $\mathcal{O}$ be an open set of $\mathbb{R}^3$, $f:\mathcal{O}\mapsto \mathbb{R}$ be a differentiable function, $a$ be a regular value of $f$. Then, $f^{-1}(a)$ is a regular surface.

>[!Claim]
>$T_pS=\ker (df_p:\mathbb{R}^3\mapsto\mathbb{R})$.

>[!Proof]
>$\boxed{\supset}$ Let $v\in T_pS$, hence $\exists \alpha:(-\epsilon,\epsilon)\mapsto S$ such that $\alpha(0)=p$ and $\alpha'(0)=v$. But $S=f^{-1}(a)$, thus $f(\alpha(t))=a\;\forall p\in(-\epsilon,\epsilon)$. Then,
>$$
>df_p(v)=\frac{d}{dt}\bigg|_{t=0}(f\circ\alpha)=0
>$$
>Hence, for an arbitrary choice of a tangent vector, $v\in \ker(df_p)$.
>$\boxed{\subset}$ The kernel is a two-dimensional vector space, as well as $T_p(S)$. Since we already have an inclusion from one of those vector spaces into another, the other inclusion follows naturally.

>[!Example]
>Consider $S^2(r)=\{p\in\mathbb{R}^2:|p-a|^2=r^2\}$. Then, let $f(p)=|p-a|^2$, leading to the fact that $f^{-1}(r^2)=S$. Observe
>$$
>T_pS^2(r)=\ker(df_p)=\ker\{v\in\mathbb{R^3}:\frac{d}{dt}\bigg|_{t=0}\langle\alpha(t)-a,\alpha(t)-a\rangle\}\\
>=\ker\{v\in\mathbb{R^3}:\langle v,p-a\rangle + \langle p-a, v\rangle\}\\
>=\ker\{v\in\mathbb{R^3}:2\langle v,p-a\rangle \}
>$$
>So if $v$ is a tangent vector, then $v$ is orthogonal to $p-a$.