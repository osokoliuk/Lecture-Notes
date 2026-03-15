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

>[!Example]
>i) $S^2_{p_0}(r)$
>
>![[Pasted image 20260302205718.png]]
>$$
>N:S_{p_0}^2(r)\mapsto \mathbb{R}^3\\
>p\leadsto \frac{p-p_0}{r}
>$$
>ii) $S=\Gamma_f$. A graph can then be covered by only one local chart $\overline{X}=(u,v,f(u,v))$. Then, construct
>$$
>N^{\overline{X}}=\frac{(1,0,f_u)\wedge (0,1,f_v)}{|(1,0,f_u)\wedge (0,1,f_v)|}=\frac{(-f_u,-f_v,1)}{\sqrt{1+f_u^2+f_v^2}}\implies N(p)=N^{\overline{X}}\circ \overline{X}^{-1}(p)
>$$
>iii) If $S=f^{-1}(a)$, $p\in S$, $T_pS=\mathrm{ker}(df_p)=\{v\in\mathbb{R}^3:\langle \nabla f(p),v\rangle=0\}$. Thus, $N(p)=\dfrac{\nabla f(p)}{|\nabla f(p)|}$.

>[!Claim]
>If $N:S\mapsto \mathbb{R}^3$ is unitary normal, then we call a corestriction $N:S\mapsto S_0^2(1)$ a **Gauss map**. Then, $dN_p:T_pS\mapsto T_{N(p)}S_0^2(1)\simeq \{N(p))\}^\perp\simeq T_pS$. Hence, $dN_p\in\mathrm{End}(T_pS)$ and it is symmetric, such that $\langle dN_p(v),w\rangle = \langle v, dN_p(w)\rangle\;\forall v,w\in T_pS$.

>[!Proof]
>It is enough to prove that the claim holds for a basis of $T_pS$.  Let $\alpha(t)=\overline{X}(u(t),v(t))$, $\alpha(0)=p$. Then, using the chain rule,
>$$
>dN_p(\alpha'(0))=dN_p(u'(0)\overline{X}_u+v'(0)\overline{X}_v)=u'(0)dN_p(X_u)+v'(0)dN_p(X_v)
>$$
>Note now that $\langle N, \overline{X}_u\rangle=\langle N, \overline{X}_v\rangle=0$ because $\{\overline{X}_{u},\overline{X}_{u}\}$ form a basis of $T_pS$ and $N$ is normal to the tangent space. Then,
>$$
>\frac{d}{dv}\langle N, \overline{X}_u\rangle =\langle N_v,\overline{X}_u\rangle + \langle N, \overline{X}_{uv}\rangle =0\\
>\frac{d}{du}\langle N, \overline{X}_u\rangle =\langle N_u,\overline{X}_u\rangle + \langle N, \overline{X}_{vu}\rangle =0\\
>\implies \langle N_{v},\overline{X}_u\rangle = \langle N_u,\overline{X}_v\rangle
>$$
>So it is indeed symmetric.

>[!Definition]
>Let
>$$
>\mathrm{II}_p:T_pS\times T_pS\mapsto \mathbb{R}\\
>(u,w)\leadsto -\langle dN_p(v),w\rangle
>$$
>We call $\mathrm{II}_p$ **second fundamental form** of $S$ at $p$. Moreover, introduce
>$$
>\mathrm{I}_p:T_pS\times T_pS\mapsto \mathbb{R}\\
>(u,w)\leadsto \langle u,w\rangle
>$$
>It is a **first fundamental form** of $S$ at $p$. Notice that since $dN_p$ is symmetric, it is diagonalisable. We can define $k_1(p),\;k_2(p)$ to be the eigenvalues of $-dN_p$ with $k_1(p)\leq k_2(p)$. Eigenvalues are called **principal curvatures** of $S$ at $p$.  Additionally, we define $K(p)=k_1(p)k_2(p)=\det(dN_p)$ to be a **Gaussian curvature** and $H(p)=(k_1(p)+k_2(p))/2$ to be the **mean curvature** of $S$ at $p$. The directions associated to the eigenvectors $v_1$ and $v_2$, which in turn have eigenvalues $k_1$ and $k_2$, are called **principal directions**. Finally, a curve $\alpha:I\mapsto S$ is called a **line of curvature** if its tangent vector $\alpha'(t)$ is the principal direction of $S$ at $\alpha(t)\;\forall t\in I$.

>[!Example]
>i) Let $S$ be a plane in $\mathbb{R}^3$. Then, the Gauss map is $N:S\mapsto S^2$ with
>$$
>dN_p(v)=\frac{d}{dt}\bigg|_{t=0}(N\circ\alpha(t))=0
>$$
>as $N$ is constant.
>ii) Let $S=S^2_{p_0}(r)$. Then, $N:S_{p_0}^2(r)\mapsto S^2$ is defined by $p\leadsto \frac{1}{r}(p-p_0)$. Subsequently,
>$$
>dN_p(v)=\frac{d}{dt}\bigg|_{t=0}(N\circ\alpha)=\frac{d}{dt}\bigg|_{t=0}\frac{1}{r}(\alpha(t)-p_0)=\frac{v}{r}
>$$
>Moreover, 
>$$
>\mathrm{II}_p(v,w)=-\langle dN_p(v),w\rangle = -\langle \frac{v}{r},w\rangle = -\frac{1}{r}\langle v,w\rangle = -\frac{\mathrm{I}_p(v,w)}{r}
>$$
>And finally, $k_1(p)=k_2(p)=-\frac{1}{r}\;\forall p \in I$, leading to $K(p)=\frac{1}{r^2}$ and $H(p)=-\frac{1}{r}$ with eigenvalues having any tangent vector $v\in T_pS$ as a principal direction.