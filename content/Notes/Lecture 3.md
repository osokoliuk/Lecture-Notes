As usual, consider $\alpha:I\mapsto \mathbb{R}^3$ p.a.l. with $k>0$, $s\mapsto\begin{pmatrix}T(s)\\ N(s)\\ B(s)\end{pmatrix}\in \mathbb{R}^3$. Then, 
$$
\begin{pmatrix}T'(s)\\ N'(s)\\ B'(s)\end{pmatrix}=\begin{pmatrix}k(s)N(S)\\ -k(s)T(s)-\tau(s)B(s)\\ \tau(s)N(s)\end{pmatrix}=\begin{pmatrix}O_3 & k(s)\mathrm{I}_3 & O_3\\ -k(s)\mathrm{I}_3 & O_3 & -\tau(s)\mathrm{I}_3\\ O_3 & \tau(s)\mathrm{I}_3 & O_3\end{pmatrix}\begin{pmatrix}T(s)\\ N(s)\\ B(s)\end{pmatrix}
$$

>[!Theorem] Fundamental theorem of the local theory of curves
>Given $k_0$, $\tau_0:I\mapsto\mathbb{R}$ which are $C^{\infty}(I)$ with $k_0>0$, there exists a curve $\alpha:I\mapsto \mathbb{R}^3$ p.a.l. such that $k(s)=k_0(s)$ and $\tau(s)=\tau_0(s)$. Moreover, $\alpha$ is unique up to direct isometries of $\mathbb{R}^3$.

>[!Proof]
>Firstly, look at $x(s):I\mapsto \mathbb{R}^3$, which obeys a system of first-order differential equation:
>$$
>x'(s)=A_0(s)x(s)\;\leftarrow \textcolor{red}{(*)}
>$$
>where 
>$$
>A_0(s)=\begin{pmatrix}O_3 & k_0(s)\mathrm{I}_3 & O_3 \\ -k_0(s)\mathrm{I}_3 & O_3 & -\tau_0(s)\mathrm{I}_3\\ O_3 & \tau_0(s)\mathrm{I}_3 &O_3\end{pmatrix}
>$$
>Choose $\overline{a}\in\mathbb{R}^3$ such that $\overline{t}_0=(a_1,a_2,a_3)$, $\overline{h}_0=(a_4,a_5,a_6)$, $\overline{b}_0=(a_7,a_8,a_9)$ form an oriented orthonormal basis of $\mathbb{R}^3$. Let $f:I\mapsto \mathbb{R}^9$ to be a solution to $\textcolor{red}{(*)}$ with an initial condition imposed by $\overline{a}$. Define $\overline{t}=(f_1,f_2,f_3)$, $\overline{h}=(f_4,f_5,f_6)$ and $\overline{b}=(f_7,f_8,f_9)$. We want to prove that $\{\overline{t},\overline{h},\overline{b}\}$ is a positive orthonormal basis on $\mathbb{R}^3$ for any $s\in I$. The dimension $\dim\mathbb{R}^3=3$, hence, if $\{\overline{t},\overline{h},\overline{b}\}$ is indeed a basis, they should be linearly independent: 
>$$
>M(s) =\begin{pmatrix}\langle \overline{t}, \overline{t}\rangle & \langle \overline{t},\overline{n}\rangle & \langle \overline{t} , \overline{b}\rangle\\ \langle \overline{n},\overline{t} \rangle & \langle\overline{n},\overline{n} \rangle & \langle \overline{n},\overline{b}\rangle\\ \langle \overline{b},\overline{t}\rangle & \langle \overline{b},\overline{n}\rangle & \langle \overline{b},\overline{b} \rangle\end{pmatrix} = \begin{pmatrix}1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{pmatrix} = \mathrm{I}_3
>$$
>As well as
>$$
>M'(s) =\begin{pmatrix}2\langle \overline{t}', \overline{t}\rangle & \langle \overline{t}',\overline{n}\rangle + \langle \overline{t},\overline{n}'\rangle & \langle \overline{t}' , \overline{b}\rangle + \langle \overline{t} , \overline{b}'\rangle \\ \langle \overline{n}',\overline{t} \rangle + \langle\overline{n},\overline{t}' \rangle & 2\langle\overline{n}',\overline{n}\rangle & \langle \overline{n}',\overline{b}\rangle + \langle \overline{n},\overline{b}'\rangle \\ \langle \overline{b}',\overline{t}\rangle + \langle \overline{b},\overline{t}'\rangle & \langle \overline{b}',\overline{n}\rangle + \langle \overline{b},\overline{n}'\rangle & 2\langle \overline{b}',\overline{b} \rangle\end{pmatrix} 
>$$
>Then, set $M(s)=ff^T$, which implies
>$$
>M'(s)=(ff^T)' = f'f^T+f(f^T)' = f'f^T+f(f')^T \\= Aff^T+f(Af)^T=Aff^T+ff^TA^T=AM(s)+M(s)A
>$$
>with
>$$
>A(s)=\begin{pmatrix}O_3 & k(s)\mathrm{I}_3 & O_3 \\ -k(s)\mathrm{I}_3 & O_3 & -\tau(s)\mathrm{I}_3\\ O_3 & \tau(s)\mathrm{I}_3 &O_3\end{pmatrix}, \; M(0)=\mathrm{I}_3
>$$
>But notice that $M(s)=\mathrm{I}_3$ is a solution to the above equation $\forall s \in I$. With the given initial condition $M(0)=\mathrm{I}_3$, the solution is unique by the uniqueness theorem for the first-order differential equations. Notice that $\det M(s)=\pm 1\;\forall s\in I$. Since $\det M(0)=1$ and $M(s)$ is a continuous function everywhere, $\det M(s)=1\;\forall s \in I$. Define $\alpha:I\mapsto \mathbb{R}^3$ by $\alpha(s)=p+\int^s_{s_0}t(u)du$. This is the curve we were looking for. Notice that the only choice in this proof that we have is the choice of initial oriented orthonormal basis and an initial point $p\in\mathbb{R}^3$, so any two curves constructed via the aforementioned approach will only differ by a direct isometry of $\mathbb{R}^3$, as required.

>[!Definition] 
>A curve $\alpha:I\mapsto \mathbb{R}^3$ with $I=[a,b]$, $\alpha(a)=\alpha(b)$ and no intersections is called a **closed planar curve**.

>[!Theorem] Green's Theorem
>Let $f(x,y),g(x,y)\in C^1(\mathbb{R}^2)$ and let $R$ be a bounded region inside a curve $C\subset \mathbb{R}^2$. Then, 
>$$
>\int_R \bigg(\frac{\partial g}{\partial x} - \frac{\partial f}{\partial y}\bigg)dxdy = \int_C \bigg(f\frac{dx}{dt}+g\frac{dy}{dt}\bigg)dt
>$$
>Take $f=-y$, $g=x$. Then, 
>$$
>2\mathrm{Area}(R)=2\int_R2dxdy = \int_C\bigg(-y\frac{dx}{dt}+x\frac{dy}{dt}\bigg)dt = \int^b_a\bigg(-y\frac{dx}{dt}+x\frac{dy}{dt}\bigg)dt
>$$

>[!Theorem] 
>$L^2\geq 4\pi \mathrm{Area}(R)$. Moreover, equality holds if and only if $\alpha$ parameterises a circle.
>
>![[Pasted image 20260228020534.png|center|250]]

>[!Proof]
>If $C$ is described by a p.a.l. curve as $\alpha(s)=(x(x),y(s))$ then we can choose a parameterisation of $C'$ as $\beta(s)=(x(s),\tilde{y}(s))$ with $s\in [0,L]$. Then, using the Green's theorem,
>$$
>\mathrm{Area}(R)=\frac{1}{2}\int^L_0(xy'-yx')ds= \frac{1}{2}\int^L_0xy'ds - \frac{1}{2}\int^L_0 yx'ds
>$$
>Using integration by parts,
>$$
>\int^L_0xy'dx = \underbrace{[xy]^L_0}_{0}-\int^L_0yx'ds\implies \mathrm{Area}(R)=-\int^L_0xy'ds
>$$
>But, notice that
>$$
>\mathrm{Area(Interior\;of\;}C')=\pi r^2=-\int^L_0x'\tilde{y}ds
>$$
>Hence,
>$$
>\mathrm{Area}(R)+\pi r^2 = \int^L_0 (xy'-\tilde{y}x')ds\\
>\leq \int^L_0\bigg[(xy'-\tilde{y}x')^2\bigg]^{1/2}ds\\
>\leq \int^L_0\bigg[(x^2+\tilde{y}^2)\underbrace{((x')^2+(y')^2))}_{||\alpha'(t)||=1}\bigg]^{1/2}ds=\int^L_0 \bigg[\underbrace{x^2+\tilde{y}^2}_{r^2}\bigg]^{1/2}=Lr
>$$
>Hence, by the Hölder's inequality,
>$$
>\sqrt{\pi r^2\mathrm{Area}(R)}\leq \frac{1}{2}(\mathrm{Area}(R)+\pi r^2)\leq \frac{Lr}{2}\implies \mathrm{Area}(R)\leq \frac{L^2}{4\pi}
>$$