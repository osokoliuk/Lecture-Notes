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