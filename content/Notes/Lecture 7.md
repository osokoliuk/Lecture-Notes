---
id: "DG7"
tags:
  - DiffGeom
---
>[!Definition]
>Let $S$ be a regular surface. Then, a **vector field** $V$ on $S$ is a differentiable function $V:S\mapsto \mathbb{R}^3$. $V$ is called *normal* (*unitary*) if $\forall p \in S$, $V(p)\perp T_pS$ ($|V(p)|=1$)

>[!Example]
>Let $S=\{2z=x^2+y^2\}$ with $S=\Gamma_f$, 
>$$
>f:\mathbb{R}^2\mapsto \mathbb{R}\\
>(x,y)\leadsto \frac{x^2+y^2}{2}
>$$
>Then, we have a local chart 
>$$
>\overline{X}:\mathbb{R}^2\mapsto \mathbb{R}^3\\
>(u,v)\mapsto (u,v,\frac{u^2+v^2}{2})
>$$
>which implies
>$$
>\left\{\frac{\partial \overline{X}}{\partial u},\frac{\partial\overline{X}}{\partial v}\right\}=\left\{(1,0,u),(0,1,v)\right\}
>$$
>Note that $\forall p\in S,\;p=\overline{X}(u_0,v_0)$ for some $(u_0,v_0)\in U$. Then,
>$$
>T_pS=\mathrm{span}\left(\frac{\partial \overline{X}}{\partial u}(u_0,v_0),\frac{\partial \overline{X}}{\partial v}(u_0,v_0)\right)
>$$
>Recall that $T_pS$ is a vector space and $T_pS=d\overline{X}_{\overline{X}^{-1}(p)}(\mathbb{R}^2)$, partial derivatives of $\overline{X}$ are linearly independent so form a basis of $T_pS$.

>[!Lemma]
>If $\overline{X}:U\mapsto S$ is a local chart then there exists at least one unitary normal vector field on $\overline{X}(U)$.

>[!Notation]
>$\dfrac{\partial \overline{X}}{\partial u}=\overline{X}_u$, $\dfrac{\partial \overline{X}}{\partial v}=\overline{X}_v$.

>[!Proof]
>As it was previously mentioned, $\{\overline{X}_u,\overline{X}_v \}$ is a basis of $T_{\overline{X}(q)}$ whenever $q\in U$. Let $N^{\overline{X}}:U\mapsto \mathbb{R}$ be defined by
>$$
>N^{\overline{X}}(q)=\frac{\overline{X}_u(q)\wedge\overline{X}_v(q)}{|\overline{X}_u(q)\wedge\overline{X}_v(q)|}
>$$
>Clearly, $N^{\overline{X}}\perp T_{\overline{X}}(q)S$ and $|N^{\overline{X}}|=1$. Define a normal, unitary vector field $N:S\mapsto \mathbb{R}$ on local chart $\overline{X}$ as $N(p)=N^{\overline{X}}\circ \overline{X}^{-1}(p)$.

>[!Lemma] 
>If $S$ is connected, $N_1$ and $N_2$ are unitary, normal vector fields on $S$ then either $N_1=N_2$ or $N_1=-N_2$.

>[!Proof]
>$\forall p\in S$, $N_1(p)$, $N_2(p)$ are unitary normal vector fields and $N_1(p)=N_2(p)$ or $N_1(p)=-N_2(p)$  (as there are only two normal directions). Let 
>$$
>S=A\cup B, \quad A=\{p\in S: N_1(p)=N_2(p)\}, \quad B=\{p\in S: N_1(p)=-N_2(p)\}
>$$
>$A$ and $B$ are clearly disjoint and closed, since $f_\pm(p)=N_1(p)\pm N_2(p)$ is a continuous function and a set of solutions $f_\pm(p)=0$ thus forms a closed set (since $\{0\}$ is closed in $\mathbb{R}$, as in the standard topology, $\mathbb{R}$ is Hausdorff and hence $f_\pm^{-1}(0)$ is closed whenever $f_\pm$ is). Notice that we have now expressed $S$ as a disjoint union of two closed sets. This is a contradiction due to our initial assumption that $S$ is connected. So, either $A=\{\emptyset\}$ or $B=\{\emptyset\}$ which is analogous to the statement that either $N_1=N_2$ or $N_1=-N_2$.

>[!Definition]
>A regular surface $S$ for which $\exists$ a unitary normal $N:S\mapsto \mathbb{R}^3$ is called **orientable**.