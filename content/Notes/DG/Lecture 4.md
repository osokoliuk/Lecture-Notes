---
id: "DG4"
tags:
  - DiffGeom
---
>[!Definition]
>A subset $S$ of $\mathbb{R}^3$ is a **regular surface** if $\forall p \in S$, $\exists$ an open set $V\subset\mathbb{R}^3$ such that $p\in V$ and $\exists \overline{X}:U\mapsto V$ where $U$ is an open set of $\mathbb{R}^2$, $\overline{X}$ is surjective and
>1. $\overline{X}$ is a $C^\infty$ map.
>2. $\overline{X}$ is a homeomorphism between open sets $U$ and $V$.
>3. $\forall q \in U$, $d\overline{X}_q:\mathbb{R}^2\mapsto \mathbb{R}^3$ is injective.
>
>We call $\overline{X}$ a *local chart* around $p$ while $V\cap S$ is called a *coordinate chart* of $S$ around $p$.
>

>[!Remark] 
>$d\overline{X}_q(v)$ is the differential of $\overline{X}$ around a point $q$ and is defined as:
>$$
>d\overline{X}_q(v)=\frac{d}{dt}\bigg|_{t=0}(\overline{X}\circ \alpha)(t)
>$$
>with $\alpha:\{-\epsilon,\epsilon\}\mapsto \mathbb{R}^2$, $\epsilon>0$, defined by $\alpha(0)=q$ and $\alpha'(0)=v$.

>[!Proposition]
>$f:U\mapsto \mathbb{R}$ is a $C^\infty$ function. The **graph** of this function, $\Gamma_f=\{u,v,f(u,v):(u,v)\in U\}$ is a regular surface.

>[!Proof]
>Take $\overline{X}(u,v)=(u,v,f(u,v))$. By construction, this function is one-to-one. It is also $C^\infty$ and surjective, by the definition of $f$, Hence, $\overline{X}^{-1}$ exists. Moreover, $\overline{X}^{-1}$ is $C^\infty$ as it is a restriction of $\Gamma_f$ to $(x,y,z)\to (x,y)$. Now, note that $d\overline{X}_q$ is injective iff
>$$
>\frac{\partial \overline{X}}{\partial u}\wedge \frac{\partial \overline{X}}{\partial v} \neq 0
>$$
>Hence, those two partial derivatives must be linearly independent. But
>$$
>\frac{\partial \overline{X}}{\partial u} = \left(1,0,\frac{\partial f}{\partial u}\right)\\
>\frac{\partial \overline{X}}{\partial v} = \left(0,1,\frac{\partial f}{\partial v}\right)
>$$
>which proves the linear independence of those two vectors, making $d\overline{X}_q$ injective.

>[!Example]
>Consider a unit sphere at the origin $S^2=\{(x,y,z):x^2+y^2+z^2=1\}$.
>![[Pasted image 20260301011733.png|400]]
>Let 
>$$
>\overline{X}_1(x,y)=\{x,y,\sqrt{1-x^2-y^2}:x,y\in U_1\}\\
>\overline{X}_2(x,y)=\{x,y,-\sqrt{1-x^2-y^2}:x,y\in U_2\}\\
>\overline{X}_3(x,z)=\{x,\sqrt{1-x^2-z^2},z:x,z\in U_3\}\\
>\overline{X}_4(x,z)=\{x,-\sqrt{1-x^2-z^2},z:x,z\in U_4\}\\
>\overline{X}_5(y,z)=\{\sqrt{1-y^2-z^2},y,z:y,z\in U_5\}\\
>\overline{X}_6(y,z)=\{-\sqrt{1-y^2-z^2},y,z:y,z\in U_6\}
>$$
>Those charts now cover the whole of $S^2$, hence a sphere is a regular surface.

>[!Theorem] Implicit Function Theorem
>Let $\mathcal{O}$ be an open set of $\mathbb{R}^3$, $p=(x_0,y_0,z_0)\in\mathbb{R}^3$, $a\in \mathbb{R}$ and $f:\mathcal{O}\mapsto \mathbb{R}$ is a $C^\infty$ function. Suppose that $f(p)=a$, $\frac{\partial f}{\partial z}(p)\neq 0$. Then, $\exists$ an open set $U\subset \mathbb{R}^2$ such that $(x_0,y_0)\in U$ and an open set $V\subset \mathbb{R}$ such that $z_0 \in V$, a function $g:U\mapsto V$ defined by $g(x_0,y_0)=z_0$ with $U\times V\subset \mathcal{O}$ and $\{p\in U\times V: f(p)=a\}=\{(x,y,g(x,y)):(x,y)\in U\}$.

>[!Corollary]
>Let $a\in\mathbb{R}$ be a regular value for a $C^\infty$ function (i.e. $df_p\neq 0\;\forall p\in f^{-1}(a))$), then $f^{-1}(a)$ is either empty or a regular surface.

>[!Proof]
>Let $p=(x_0,y_0,z_0)\in f^{-1}(a)$.  By assumption, $a$ is a regular value and hence $df_p\neq 0$. Assume without the loss of generality that $\frac{\partial f}{\partial z}(p)\neq 0$. Implicit function theorem implies that for $S=f^{-1}(a)$, $S\cap (U\times V)$ is a regular surface. Since we have a freedom to choose any point $p$ and $a$ is a regular value, we can construct as many charts as we need to cover the whole $f^{-1}(a)$, hence it is a regular surface.

>[!Example]
>Consider a quadrics. Let $A$ be a 4x4 symmetric matrix, let
>$$
>S = \{r\in\mathbb{R}^3:\begin{pmatrix}1&v^T\end{pmatrix}A\begin{pmatrix}1 \\ v\end{pmatrix}=0\}
>$$
>Look at the function $f(v)=\begin{pmatrix}1&v^T\end{pmatrix}A\begin{pmatrix}1 \\ v\end{pmatrix}$. Clearly, $S=f^{-1}(0)$. We want to show that $0$ is a regular value for $f$, which would then imply that $S$ is indeed a regular surface. Pick $v\in f^{-1}(0)$ and compute
>$$
>df_p(v) = \frac{d}{dt}\bigg |_{t=0}(f\circ \alpha) = \frac{d}{dt}\bigg |_{t=0}\begin{pmatrix}1&\alpha(t)^T\end{pmatrix}A\begin{pmatrix}1 \\ \alpha(t)\end{pmatrix} = \begin{pmatrix}0&v^T\end{pmatrix}A\begin{pmatrix}1 \\ p\end{pmatrix}+\begin{pmatrix}1&p^T\end{pmatrix}A\begin{pmatrix}0 \\ v\end{pmatrix}\\
>=2\begin{pmatrix}1&p^T\end{pmatrix}A\begin{pmatrix}0 \\ v\end{pmatrix}
>$$
>We want to see if that's possible for $df_p(v)=0\;\forall v$. This is equivalent to stating that 
>$$
>\begin{pmatrix}1 & p^T\end{pmatrix}A\begin{pmatrix}0 \\ v\end{pmatrix}=\begin{pmatrix}a_1 & a_2 & a_3 & a_4\end{pmatrix}\begin{pmatrix}0 \\ v\end{pmatrix} =0\implies a_2,a_3,a_4=0
>$$ 
>We set $\lambda=a_1$. Note that since $v\in f^{-1})(0)$, then
>$$
>\begin{pmatrix}1&v^T\end{pmatrix}A\begin{pmatrix}1 \\ v\end{pmatrix} = 0\implies \begin{pmatrix}\lambda & 0\end{pmatrix}\begin{pmatrix}0\\v\end{pmatrix}=\lambda v = 0
>$$
>So as long as $\lambda\neq 0$ and $v\neq 0$, $df_p(v)\neq 0$ making 0 a regular value for $f$, hence making $S$ a regular surface, as required.