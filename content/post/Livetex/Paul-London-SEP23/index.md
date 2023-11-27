---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Results concerning automorphic forms and L-functions of higher rank"
subtitle: "Talk by Paul Nelson"
summary: ""
authors: []
tags: []
categories: []
date: 2023-09-14T21:22:00+01:00
lastmod: 2023-09-14T21:22:00+01:00
featured: false
draft: false
math: mathjax
# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---


<h1 class="unnumbered"
id="motivating-goal-subconvexity-for-twists">Motivating goal:
Subconvexity for twists</h1>
<p><span class="math inline">\(F\)</span> is a number field. <span
class="math inline">\(\pi:\mathrm{GL}_n\)</span>, <span
class="math inline">\(\chi:\mathrm{GL}_1\)</span> <span
class="math display">\[\begin{align}
\label{subconvex-twists}
  L(\pi\times\chi,&amp;1/2)\ll_\pi C(\chi)^{n/4-\delta}\tag{$\star$} \\
                  &amp;\Bigg\updownarrow
                   \substack{\text{(Lapid-Mao) $n$ is even,
                    $\pi$ comes from $\mathrm{SO}(n+1)$},\\
                       \text{$\chi$ quadratic,
$C_\mathrm{fin}(\chi)\approx\square$-free}}\notag\\
    \text{Fourier} &amp; \text{ coefficients on $Mp_n$}\notag
\end{align}\]</span></p>
<div class="thm">
<p><strong>Theorem 1</strong> (N., 2021). <em><span
class="math inline">\(\eqref{subconvex-twists}\)</span> for <span
class="math inline">\(\chi=|\cdot|^{it}\)</span>, <span
class="math inline">\(F=\mathbb{Q}\)</span></em></p>
</div>
<div class="thm">
<p><strong>Theorem 2</strong> (Yueke Hu, PN, today). <em>variant of
<span class="math inline">\(\eqref{subconvex-twists}\)</span> for <span
class="math inline">\(C_\mathrm{fin}(\chi)=\square\)</span>,
<em>e.g.</em> <span class="math inline">\(p^2\rightarrow
\infty\)</span></em></p>
</div>
<p>Subconvexity for <span
class="math inline">\(L(\pi\times\check{\sigma},1/2)\)</span>, where
<span class="math inline">\(\pi:\mathrm{GL}_{n+1}\)</span>, <span
class="math inline">\(\sigma:\mathrm{GL}_n\)</span>, <span
class="math inline">\(|F|\ni \mathfrak{p}\)</span><br />
Assuming:</p>
<ol>
<li><p>bounded ramification outside <span
class="math inline">\(\mathfrak{p}\)</span></p></li>
<li><p><span class="math inline">\(\mathfrak{p}\)</span> finite of norm
<span class="math inline">\(\mathfrak{q}\)</span>.</p></li>
<li><p>principal series: <span
class="math inline">\(\pi_\mathfrak{p}=\chi_1\boxplus\ldots\boxplus\chi_{n+1}\)</span>,
<span
class="math inline">\(\sigma_\mathfrak{p}=\eta_1\boxplus\ldots\boxplus\eta_n\)</span></p></li>
<li><p>uniform growth: <span
class="math inline">\(C(\chi_i/\eta_j)=T\)</span> (<span
class="math inline">\(\Leftrightarrow\mathrm{Cond}(\pi\times\check{\sigma})=T^{n(n+1)}\)</span>),
where</p>
<div class="center">
<p><span class="math inline">\(T=\)</span> max analytic conductor of
<span class="math inline">\(\chi_i\)</span>, <span
class="math inline">\(\eta_j\)</span> <span
class="math inline">\(=\)</span> power of <span
class="math inline">\(q\)</span>.</p>
</div></li>
<li><p>Even depth <span
class="math inline">\(T=\mathfrak{q}^{2m}\)</span></p></li>
<li><p>comes from <span class="math inline">\(U(n+1)\times U(n)\)</span>
(something about anisotropic)</p></li>
</ol>
<div class="thm*">
<p><strong>Theorem 1</strong> (N., 2020-2023). <em><span
class="math inline">\(\mathfrak{p}\)</span> archimedean, remove (3),
(5)</em></p>
</div>
<div class="thm*">
<p><strong>Theorem 2</strong> (N., 2021). <em>remove (6), <span
class="math inline">\(\sigma\)</span> Eisenstein.</em></p>
</div>
<p><strong>Marshall:</strong> <span
class="math inline">\(\mathfrak{p}\)</span> fixed, <span
class="math inline">\(C(\chi_i/\chi_j)=C(\eta_i/\eta)=T\)</span>, for
<span class="math inline">\(i\neq j\)</span> (wall-avoidance)</p>
<h1 class="unnumbered" id="proof-scheme">Proof scheme</h1>
<p><span class="math inline">\(\pi:G=\mathrm{GL}(n+1)\)</span>, <span
class="math inline">\(\sigma:H=\mathrm{GL}(n)\)</span></p>
<p>Choose <span class="math inline">\(u\in\sigma\)</span> Estimate both
sides: <span class="math inline">\(\omega\in
C_c^\infty(G(\mathbb{A}))\)</span></p>
<p><span
class="math display">\[\sum_\pi|L^{(\mathfrak{p})}(\pi\times\check{\sigma},1/2)|^2\sum_{v\in\mathcal{B}(\pi_\mathfrak{p})}
\int_{h\in H(F_\mathfrak{p})}\langle h\pi(\omega)v,v\rangle\langle
u,hu\rangle\mathrm{d}h=(\ldots)\]</span> This is called the spectral
side</p>
<p><span class="math display">\[(\ldots)=\int_{x,y\in H(F)\backslash
H(\mathbb{A})}u(x)\overline{u(y)}\sum_{\gamma\in G(F)}
  \omega(x^{-1}\gamma y)\mathrm{d}x\mathrm{d}y\]</span></p>
<h2 class="unnumbered" id="spectral-side">Spectral side</h2>
<p><span
class="math inline">\(\mathfrak{p}\subseteq\mathfrak{o}\)</span> (local)
<span class="math display">\[1\neq \psi:
\mathfrak{p}/\mathfrak{p}^2\rightarrow U(1)\]</span> <span
class="math display">\[\chi:\mathrm{GL}_1(\mathfrak{o}/\mathfrak{p}^2)\rightarrow\mathbb{C}^{\ast}\leadsto\xi_\chi\in\mathfrak{o}/\mathfrak{p}\]</span>
<span class="math display">\[\chi(1+x)=\psi(\xi_\chi x),\,\forall
x\in\mathfrak{p}\]</span></p>
<p><span
class="math display">\[G,H,M,M_H=\mathrm{GL}_{n+1},\mathrm{GL}_n,\operatorname{Mat}_{n+1},
\operatorname{Mat}_n\]</span> <span class="math display">\[\tau\in
M(\mathfrak{o}/\mathfrak{p}),\quad \pi=\text{representation of }
G(\mathfrak{o}/\mathfrak{p}^2)\]</span></p>
<p>Call <span class="math inline">\(v\in \pi\)</span> <em>localized</em>
at <span class="math inline">\(\tau\)</span> if <span
class="math inline">\(\forall x\in
M(\mathfrak{o}/\mathfrak{p}^2)\)</span>, <span
class="math inline">\(x\equiv 0 \pmod{\mathfrak{p}}\)</span></p>
<p><span
class="math display">\[\pi(1+x)v=\psi(\operatorname{trace}(x\tau))v\]</span></p>
<div class="fact">
<p><strong>Fact 1</strong>. <em>“Often” <span
class="math inline">\(\dim{|{v|}}=1\)</span>. <span
class="math inline">\(P_\pi:=P_\tau=\)</span> characteristic polynomial
depends only on <span class="math inline">\(\pi\)</span>.</em></p>
</div>
<div class="example">
<p><strong>Example 1</strong>. <em><span
class="math inline">\(P_{\chi}=t-\xi_t,\quad  P_{\boxplus
\pi_i}=\prod_iP_{\pi_i}\)</span></em></p>
</div>
<h2 class="unnumbered" id="method-of-nelson-venkatesh">Method of
Nelson-Venkatesh:</h2>
<p><span class="math inline">\(\forall (\pi,\sigma)\)</span> of <span
class="math inline">\((\mathrm{GL}_{n+1}(\mathfrak{o}/\mathfrak{p}^2),
\mathrm{GL}_n(\mathfrak{o}/\mathfrak{p}^2))\)</span> with <span
class="math inline">\((P_\pi,P_\sigma)=(1)\)</span>, there exists <span
class="math display">\[\begin{pmatrix}\tau_H&amp;\ast\\\ast&amp;\ast\end{pmatrix}=\tau\in
M(\mathfrak{o}/\mathfrak{p}),\quad  \tau_H\in  M_H(\mathfrak{o}/\mathfrak{p})\]</span>
such that <span class="math inline">\(P_\tau=P_\pi\)</span> and <span
class="math inline">\(P_{\tau_H}=P_\sigma\)</span></p>
<p>There exists unit vectors <span class="math inline">\(v\in\pi,\,u\in
\sigma\)</span> localized at <span
class="math inline">\(\tau,\tau_H\)</span>, respectively, such that for
<span class="math inline">\(h\in
H(\mathfrak{o}/\mathfrak{p}^2)\)</span></p>
<p><span class="math display">\[\langle hv,v\rangle\langle u,hu\rangle=
  \begin{cases}
    1\text{ if }h\equiv 1\pmod{\mathfrak{p}},\\
    0\text{ else}.
  \end{cases}\]</span> (+ something similar over local fields)</p>
<h2 class="unnumbered"
id="geometric-side-after-cauchy-schwarz">Geometric side after
Cauchy-schwarz</h2>
<p><span
class="math inline">\(F=\mathfrak{o}/\mathfrak{p}=\mathbb{F}_q\)</span></p>
<p><span class="math display">\[G,H,M,M_H=\text{ points over
}F\]</span></p>
<p><span class="math display">\[\tau\in M,e=\begin{pmatrix}0\\
\vdots\\0\\1\end{pmatrix},
e^{\ast}=\begin{pmatrix}0\!&amp;\!\ldots\!&amp;\!0\!&amp;\!1\end{pmatrix}\]</span></p>
<div class="lem">
<p><strong>Lemma 1</strong>. <em><span
class="math display">\[(P_\tau,P_{\tau_H})=(1)\Leftrightarrow
  e,e^\ast:\tau-\text{cyclic}\]</span></em></p>
</div>
<div class="dfn">
<p><strong>Definition 1</strong>. <em>If any (hence both) of the above
holds, we say that <span class="math inline">\(\tau\)</span> is
<em>stable</em></em></p>
</div>
<p>For <span class="math inline">\(\tau\in M_{\text{stable}}, a\in
G_\tau\)</span>, then the set <span
class="math display">\[X_{\tau,a}=\{y=H_{\tau_H}:ay\in
HG_\tau\}\]</span> is a <em>closed subscheme</em>.</p>
<div class="thm">
<p><strong>Theorem 3</strong> (HN). <em>Assume <span
class="math inline">\(q\)</span> is odd, <span
class="math inline">\(n+1\neq 3\)</span>. Then <span
class="math display">\[\frac{X_{\tau,a}}{H_{\tau_H}}\ll \frac{1}{q}
\Leftarrow X_{\tau,a}\neq H_{\tau_H}\]</span></em></p>
</div>
<p><span class="math inline">\(\mu(y)\nu(y^{-1})=1\)</span>, where <span
class="math inline">\(\mu,\nu:M_{H,\tau_H}\rightarrow
M_{\tau}\Big|_{\substack{e^\ast\mu(x)=e^\ast
axa^{-1}\\\nu(x)e=axa^{-1}e}}\)</span></p>
<div class="lem">
<p><strong>Lemma 2</strong>. <em>If <span
class="math inline">\(X_{\tau,a}=H_{\tau_H}\)</span> then, <span
class="math display">\[\begin{align}
    \mu&amp;=\nu \label{lin}\tag{linear} \\
    \mu(xy)&amp;=\mu(x)\mu(y) \label{quad}\tag{quadratic}
\end{align}\]</span></em></p>
</div>
<div id="thm4" class="thm">
<p><strong>Theorem 4</strong>. <em><span
class="math inline">\(\eqref{lin} \Leftrightarrow a^2\in
Z\)</span></em></p>
</div>
<div id="thm5" class="thm">
<p><strong>Theorem 5</strong>. <em><span
class="math inline">\(\eqref{lin}+\eqref{quad}\)</span> <span
class="math inline">\(\Leftrightarrow a\in Z\)</span></em></p>
</div>
<div class="proof">
<p><em>Proof.</em> (of Theorem <a href="#thm4" data-reference-type="ref"
data-reference="thm4">4</a>) Let <span
class="math inline">\(A_j=e^{\ast}\tau^jae\)</span>, <span
class="math inline">\(B_j=e^{\ast}\tau^ja^{-1}e\)</span> <span
class="math display">\[\mu(\mathbf{1}_H)-v(\mathbf{1}_H)=B_0a-A_0a^{-1}\]</span>
If either <span class="math inline">\(B_0\neq 0\)</span> or <span
class="math inline">\(A_0\neq 0\)</span> then <span
class="math inline">\(a^2\in Z\)</span>. Else continue with <span
class="math inline">\(\tau_H,\tau_H^2,\tau_H^3,\ldots\)</span> ◻</p>
</div>
<p>For Theorem <a href="#thm5" data-reference-type="ref"
data-reference="thm5">5</a>, use that <span
class="math inline">\(\mu(\mathbf{1}_H)^2=\mu(\mathbf{1}_H)\)</span>,
<span class="math inline">\(\tau^2+c_1\tau+c_0=0\)</span>.</p>
