---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Análise complexa - aula 2"
subtitle: "Notas por Pedro Igor"
summary: ""
authors: []
tags: []
categories: []
date: 2023-08-22T01:26:00-03:00
lastmod: 2023-08-22T01:26:00-03:00
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


<body>
<h2 id="sequências-sobre-compactos">Sequências sobre compactos</h2>
<div class="Def">
<p><strong>Definição 1</strong>. <em>Seja <span
class="math inline">\(\Omega \subset \mathbb{C}\)</span>,<span
class="math display">\[\operatorname{diam}(\Omega) = \sup_{z,w \in
\Omega}|z-w|.\]</span></em></p>
</div>
<div class="prop">
<p><strong>Proposição 1</strong>. <em><span
class="math inline">\(\Omega\)</span> é limidado <span
class="math inline">\(\Leftrightarrow \operatorname{diam}(\Omega)&lt;
\infty.\)</span></em></p>
</div>
<div class="theorem">
<p><strong>Teorema 1</strong>. <em><span class="math inline">\(\Omega
\subset \mathbb{C}\)</span> é compacto se, e somente se, toda sequência
<span class="math inline">\(\{z_n\}\subset \mathbb{C}\)</span> possui
uma subsequência que converge oara um ponto <span
class="math inline">\(z \in \Omega\)</span>.<br />
</em></p>
</div>
<div class="proof">
<p><em>Proof.</em> (<span class="math inline">\(\Rightarrow\)</span>):
Seja <span class="math inline">\(\{z_n\}\)</span> uma sequência nos
complexos. Como <span class="math inline">\(\Omega\)</span> é compacto,
existe <span class="math inline">\(M\)</span> tal que <span
class="math inline">\(|z_n|&lt;M\)</span> para todo <span
class="math inline">\(n\)</span>. Como vimos na aula passada, <span
class="math inline">\(|\operatorname{Re}(z_n)|,|\operatorname{Im}(z_n)|&lt;M\)</span>.
Logo, as sequências reais <span
class="math inline">\(\operatorname{Re}(z_n)\}\)</span> e <span
class="math inline">\(\{\operatorname{Im}(z_n)\}\)</span> são
,respectivamente, sequências de um conjunto compacto da reta, a saber
<span class="math inline">\([-M,M]\)</span>. Logo, usando o resultado
analogo ao que estamos provando, sobre <span
class="math inline">\(\mathbb{R}\)</span>, obtemos uma subsequência
<span class="math inline">\(\{\operatorname{Re}(z_{n_k})\}\)</span> tal
que <span class="math inline">\(\operatorname{Re}(z_{n_k}) \rightarrow
x\)</span>. Aplicando o mesmo resultado à subsequência <span
class="math inline">\(\{\operatorname{Im}(z_{n_k})\}\)</span>, obtemos
uma subsubsequência tal que <span
class="math inline">\(\operatorname{Im}(z_{n_{k_l}})\rightarrow
y\)</span>. Ou seja, encontramos (sub)subsequência <span
class="math inline">\(\{z_{n_k}\}\)</span>tal que <span
class="math inline">\(\operatorname{Re}(z_{n_k})\rightarrow z\)</span> e
<span class="math inline">\(\operatorname{Im}(z_{n_k}) \rightarrow
y\)</span>. Donde <span class="math inline">\(z_{n_k} \rightarrow
x+iy\)</span>. Para concluir, basta ver que <span
class="math inline">\(z \in \Omega\)</span>. Como <span
class="math inline">\(z\)</span> é limite de uma sequência de pontos em
<span class="math inline">\(\Omega\)</span> e <span
class="math inline">\(\Omega\)</span> é fechado, isto segue.<br />
(<span class="math inline">\(\Leftarrow\)</span>): Suponha agora que
<span class="math inline">\(\Omega\)</span> é al que toda sequüencia
possui subsequëncia possui subseqüencia convergente em <span
class="math inline">\(\Omega\)</span>. Suponha, por absurdo que <span
class="math inline">\(\Omega\)</span> não é limitado. Isto significa que
existe uma sequüencia <span class="math inline">\(\{z_n\}\subset
\Omega\)</span> tal que que <span class="math inline">\(\lim_n
|z_n|=+\infty\)</span> e isto valera também para qualquer subsequüencia.
Logo nenhuma susequüencia poderá convergir, o que é um absurdo.</p>
<p>De modo análogo, suponha que <span
class="math inline">\(\Omega\)</span> não é fechado e seja <span
class="math inline">\(a\)</span> um ponto limite de <span
class="math inline">\(\Omega\)</span> que não pertence a <span
class="math inline">\(\Omega\)</span>. Isso garante que existe uma
sequüencia <span class="math inline">\(\{z_n\}\subset \Omega\)</span>
tal que <span class="math inline">\(\lim_n z_n =a\)</span>. Mais uma vez
isto ocorrerá também para toda subseqëncia. Como <span
class="math inline">\(a\not\in\Omega\)</span> isto contradiz a hipótese
sobre <span class="math inline">\(\Omega\)</span>. ◻</p>
</div>
<div class="theorem">
<p><strong>Teorema 2</strong>. <em><span
class="math inline">\(\Omega\)</span> é compacto se, e somente se, toda
cobertura por abertos posssui subcobertura finita.<br />
(Demo como exercício).</em></p>
</div>
<div class="obs">
<p><strong>OBS 1</strong>. <em>Uma cobertura por abertos do <span
class="math inline">\(\Omega\)</span> é uma família de abertos <span
class="math inline">\(\{U_{\alpha}\}\)</span>, não necessáriamente
enumerável tal que <span
class="math inline">\(\bigcup_{\alpha}U_{\alpha} \supseteq
\Omega.\)</span></em></p>
</div>
<div class="prop">
<p><strong>Proposição 2</strong>. <em>Seja <span
class="math inline">\(\Omega_1 \supseteq \Omega_2 \supseteq \Omega_3
\supseteq \cdots\)</span> uma sequência de compactos não -vazios de
<span class="math inline">\(\mathbb{C}\)</span> tal que <span
class="math inline">\(\operatorname{diam}(\Omega_n) \rightarrow
0\)</span> quando <span class="math inline">\(n \rightarrow
\infty\)</span>. Então existe, um único ponto <span
class="math inline">\(w\)</span> tal que <span class="math inline">\(w
\in \bigcap_{n}\Omega_n\)</span>.</em></p>
</div>
<div class="proof">
<p><em>Proof.</em> Para cada <span class="math inline">\(n\)</span>,
tome <span class="math inline">\(z_n \in \Omega_n\)</span>. Dado <span
class="math inline">\(\epsilon&gt;0\)</span>, existe <span
class="math inline">\(N&gt;0\)</span> tal que se <span
class="math inline">\(n&gt;N\)</span>, <span
class="math inline">\(diam(\Omega)&lt; \epsilon\)</span>. Logo, dados
<span class="math inline">\(m,n &gt; N\)</span>, <span
class="math inline">\(z_m \in \Omega_{N+1}\)</span> e <span
class="math inline">\(z_n \in \Omega_{N+1} \Rightarrow |z_n-z_m|
\leqslant \operatorname{diam}
(\Omega_{N+1})&lt;\epsilon\)</span>. Ou seja, <span
class="math inline">\(\{z_n\}\)</span> é sequência de Cauchy. Logo, a
sequência possui limite <span class="math inline">\(w\)</span>. Como
<span class="math inline">\(z_n \in \Omega_{m} \forall n&gt;m\)</span>,
temos que <span class="math inline">\(w \in \Omega_{m} ,\forall
m\)</span> Portanto, <span class="math inline">\(w \in
\bigcap_{n}\Omega_{n}\)</span>. Para ver que <span
class="math inline">\(w\)</span> é único, se <span
class="math inline">\(z\)</span> é outro ponto de <span
class="math inline">\(\bigcap_n\Omega_n\)</span>, <span
class="math display">\[|z-w|\leqslant \operatorname{diam}(\Omega_n),
\forall n
\Rightarrow |z-w|\leqslant 0 \Rightarrow z=w,\]</span> o que é um
absurdo. ◻</p>
</div>
<h2 id="conectividade">Conectividade</h2>
<div class="Def">
<p><strong>Definição 2</strong>. <em>Um conjunto aberto <span
class="math inline">\(\Omega\)</span> é conexo se não existem abertos
disjuntos tais que <span class="math display">\[\Omega = \Omega_1 \cup
\Omega_2.\]</span></em></p>
</div>
<div class="Def">
<p><strong>Definição 3</strong>. <em><span
class="math inline">\(\Omega\)</span> é um domínio se <span
class="math inline">\(\Omega\)</span> é aberto e conexo.<br />
</em></p>
</div>
<p>Exercício: <span class="math inline">\(\Omega\)</span> aberto é
conexo se, e somente se, é conexo por caminhos. Ou seja, se para todos
<span class="math inline">\(z, w \in \Omega\)</span>, existe um caminho
<span class="math inline">\(\gamma\)</span>, ligando <span
class="math inline">\(z\)</span> a <span
class="math inline">\(w\)</span> (ver exercício 5 do cap. 1 do livro do
Stein para a definição de caminho).</p>
<h1 id="funções-holomorfas">Funções Holomorfas</h1>
<h2 id="continuidade">Continuidade</h2>
<ul>
<li><p>Sejam <span class="math inline">\(f: \Omega \rightarrow
\mathbb{C}\)</span> e <span class="math inline">\(z_0 \in
\Omega\)</span>. Dizemos que <span class="math inline">\(f\)</span> é
contínua em <span class="math inline">\(z_0\)</span> se para todo <span
class="math inline">\(\epsilon&gt;0\)</span>, existe <span
class="math inline">\(\delta&gt;0\)</span> tal que se <span
class="math inline">\(z \in \Omega, |z-z_0|&lt;\delta\)</span> então
<span class="math inline">\(|f(z)-f(z_0)|&lt;\epsilon\)</span>.</p>
<p>Equivalentement: Se <span class="math inline">\(\lim_{n \rightarrow
\infty}z_n = z_0\)</span> com <span class="math inline">\(z_n \in
\Omega\)</span> para todo <span class="math inline">\(n\)</span>, então
<span class="math inline">\(\lim_{n \rightarrow
\infty}f(z_n)=f(z_0)\)</span>.</p></li>
<li><p><span class="math inline">\(f\)</span> é contínua em <span
class="math inline">\(\Omega\)</span> se <span
class="math inline">\(f\)</span> é contínua em todos os pontos de <span
class="math inline">\(\Omega\)</span>.</p></li>
<li><p><span class="math inline">\(z_0 \in \Omega\)</span> é um ponto de
máximo (respectivamente mínimo) se <span class="math inline">\(|f(z)|
\leqslant |f(z_0)|,\forall n.\)</span></p></li>
</ul>
<div class="theorem">
<p><strong>Teorema 3</strong>. <em>Se <span class="math inline">\(f:
\Omega \Rightarrow \mathbb{C}\)</span> é contínua e <span
class="math inline">\(\Omega\)</span> é compacto então existem <span
class="math inline">\(z_{min}\)</span> e <span
class="math inline">\(z_{max} \in \Omega\)</span> pontos de mínimo e de
máximo, respectivamente. (Exercício)</em></p>
</div>
<h2 id="holomorfas">Holomorfas</h2>
<ul>
<li><p><span class="math inline">\(f:\Omega \rightarrow
\mathbb{C}\)</span> (<span class="math inline">\(\Omega\)</span>
aberto), <span class="math inline">\(z_0 \in \Omega.\)</span> <span
class="math inline">\(f\)</span> é holomorfa em <span
class="math inline">\(z_0\)</span> se <span
class="math display">\[\lim_{h \rightarrow
0}\dfrac{f(z_0+h)-f(z_0)}{h}\]</span> existe. Neste caso, denotamos o
limite acima por <span
class="math inline">\(f&#39;(z_0)\)</span>.</p></li>
<li><p><span class="math inline">\(f\)</span> é holomorfa em <span
class="math inline">\(\Omega\)</span>, se <span
class="math inline">\(f\)</span> é holomorfa em todo ponto <span
class="math inline">\(z_0 \in \Omega.\)</span></p></li>
<li><p>Se <span class="math inline">\(C\)</span> é fechado, dizemos que
<span class="math inline">\(f\)</span> é holomorfa em <span
class="math inline">\(C\)</span> se existe <span
class="math inline">\(\Omega \supseteq C\)</span> aberto tal que <span
class="math inline">\(f\)</span> está definida e é holomorfa em <span
class="math inline">\(\Omega.\)</span></p></li>
</ul>
<p>Exemplos:</p>
<ol>
<li><p>Polinômios: <span class="math display">\[f(z) =
a_nz^n+a_{n-1}z^{n-1}+...+a_1+a_0;\]</span> <span
class="math display">\[f&#39;(z) =
na_nz^{n-1}+(n-1)a_{n-1}z^{n-2}+\cdots+2a_2z+a_1\]</span></p></li>
<li><p><span class="math inline">\(f(z) = \dfrac{1}{z}\)</span> é
holomorfa em <span class="math inline">\(z \neq 0\)</span> com <span
class="math inline">\(f&#39;(z) = \dfrac{-1}{z^2}.\)</span><br />
</p></li>
</ol>
<p>Não-Exemplo: <span class="math inline">\(f(z) =
\overline{z}\)</span>. <span
class="math display">\[\frac{f(z+h)-f(z)}{h}=\dfrac{\overline{h}}{h},\]</span>
Logo, <span class="math inline">\(\frac{f(z+h)-f(z)}{h}\)</span> tende a
<span class="math inline">\(1\)</span> quando <span
class="math inline">\(h\rightarrow 0\)</span> por números reais e tende
a <span class="math inline">\(-1\)</span> quando <span
class="math inline">\(h \rightarrow 0\)</span> por números imaginários
puros. Logo, o limite não existe.</p>
<div class="obs">
<p><strong>OBS 2</strong>. <em>Isto marca um grande contraste entre
funções holomorfas e funções diferenciáveis em <span
class="math inline">\(\mathbb{R}\)</span>. De fato, identificando <span
class="math inline">\(\mathbb{C}\)</span> e <span
class="math inline">\(\mathbb{R}^2\)</span>, a função acima é
identificada com a função <span class="math inline">\(f(x,y) =
(x,-y)\)</span>.</em></p>
</div>
<p>Propriedades das funções holomorfas:<br />
Sejam <span class="math inline">\(f,g: \Omega \rightarrow
\mathbb{C}\)</span>, <span class="math inline">\(\Omega\)</span> aberto
e <span class="math inline">\(z_0 \in \Omega\)</span>. Suponha que <span
class="math inline">\(f\)</span> e <span
class="math inline">\(g\)</span> são holomorfas em <span
class="math inline">\(z_0\)</span>. Então,</p>
<ol>
<li><p><span class="math inline">\(f+g\)</span> é holomorfa em <span
class="math inline">\(z_0\)</span> e <span
class="math inline">\((f+g)&#39;(z_0) =
f&#39;(z_0)+g&#39;(z_0)\)</span>;</p></li>
<li><p><span class="math inline">\(f \cdot g\)</span> é holomorfa e
<span class="math inline">\((f \cdot g)&#39;(z_0) =
f&#39;(z_0)g(z_0)+f(z_0)g&#39;(z_0)\)</span>;</p></li>
<li><p>Se <span class="math inline">\(g(z_0) \neq 0\)</span>, <span
class="math inline">\(\dfrac{f}{g}\)</span> é holomorfa em <span
class="math inline">\(z_0\)</span> e <span
class="math inline">\(\left(\dfrac{f}{g}\right)&#39;(z_0)
=\dfrac{f&#39;(z_0)g(z_0)-f(z_0)g&#39;(z_0)}{g(z_0)^2}\)</span>;</p></li>
<li><p>Sejam agora <span class="math inline">\(f: \Omega \rightarrow
\mathbb{C}\)</span>, <span class="math inline">\(g:\Omega&#39;
\rightarrow \mathbb{C}\)</span> e <span class="math inline">\(z_0 \in
\Omega&#39;\)</span> tal que <span class="math inline">\(g(z_0) \in
\Omega\)</span>. Suponha que <span class="math inline">\(g\)</span> é
holomorfa em <span class="math inline">\(z_0\)</span> e <span
class="math inline">\(f\)</span> é holomorfa em <span
class="math inline">\(g(z_0)\)</span>. Então <span
class="math inline">\(f \circ g\)</span> é holomorfa em <span
class="math inline">\(z_0\)</span> e <span
class="math display">\[(f\circ g)&#39;(z_0) = f&#39;(g(z_0))\cdot
g&#39;(z_0).\]</span></p>
<h2 id="equações-de-cauchy---riemann">Equações de Cauchy - Riemann</h2>
<p>Já sabemos que se <span class="math inline">\(f\)</span> é holomorfa
em <span class="math inline">\(z\)</span> então existe <span
class="math inline">\(\alpha \in \mathbb{C}\)</span> tal que <span
class="math display">\[\lim_{h \rightarrow
0}\dfrac{f(z+h)-f(z)}{h}=\alpha,\]</span> o que é o mesmo que <span
class="math display">\[\lim_{h \rightarrow 0}\dfrac{f(z+h)-f(z)-\alpha
h}{h}=0.\]</span></p>
<p>Por outro lado, <span class="math inline">\(f: \Omega \subseteq
\mathbb{R}^2 \rightarrow \mathbb{R}^2\)</span> é diferenciável em <span
class="math inline">\((x,y)\)</span> se <span
class="math display">\[\lim_{(h_1,h_2)\rightarrow
0}\dfrac{|F(x+h_1,y+h_2)-F(x,y)-T(h_1,h_2)|}
{|(h_1,h_2)|}\]</span> para alguma transformação linear <span
class="math inline">\(T\)</span>. Note que:</p>
<ul>
<li><p><span class="math inline">\(T(h_1,h_2) =
(ah_1+bh_2,ch_1+dh_2)\)</span>;</p></li>
<li><p><span class="math inline">\(\alpha \cdot h =
(\alpha_1+i\alpha_2)\cdot (h_1+ih_2)=
  \alpha_1h_1-\alpha_2 h_2+i(\alpha_1h_2+\alpha_2h_1).\)</span></p></li>
</ul>
<p>Logo, escrevendo <span
class="math inline">\(f(x,y)=(u(x,y),v(x,y))\)</span>, temos <span
class="math display">\[\dfrac{\partial f}{\partial x} = (\dfrac{\partial
u}{\partial x},
\dfrac{\partial v}{\partial x})=\lim_{t \rightarrow
0}\dfrac{f(x+t,y)-f(x,y)}{t}\]</span> Usando a transformação <span
class="math inline">\(T\)</span>, temos então que <span
class="math inline">\(T(1,0)=(a,c)\)</span>. De maneira analoga temos
que <span class="math inline">\(T(0,1)=(b,d)\)</span>. Assim, para que a
transformação linear <span class="math inline">\(T\)</span> corresponda
à multiplicação por <span class="math inline">\(\alpha\)</span> devemos
ter</p>
<p><span class="math display">\[\begin{aligned}
  T(h_1,h_2)&amp;= (\alpha_1h_1-\alpha_2 h_2,\alpha_2h_1+\alpha_1h_2)\\
  &amp;\Leftrightarrow a = d =\alpha_1, -b = c=\alpha_2\\
  &amp;\Leftrightarrow \frac{\partial u}{\partial x}=\frac{\partial
v}{\partial y}
  \text{ and }\frac{\partial v}{\partial x}=\frac{\partial u}{\partial
y}.
\end{aligned}\]</span></p>
<p>Conclusão: Se <span class="math inline">\(f=u+iv\)</span> é uma
função holomorfa. Então, escrevendo <span
class="math inline">\(u(x,y)=u(x+iy)\)</span>, <span
class="math inline">\(v(x,y)=v(x+iy)\)</span>, valem as relações <span
class="math display">\[\dfrac{\partial u}{\partial x} = \dfrac{\partial
v}{\partial y},
  \dfrac{\partial v}{\partial x} = -\dfrac{\partial u}{\partial
y},\]</span> chamadas de <strong>Equações de
Cauchy-Riemann</strong>.</p></li>
</ol>
<p>Seja <span class="math inline">\(f: \Omega \rightarrow
\mathbb{C}\)</span> tal que ao fazer a identificação usual entre <span
class="math inline">\(\mathbb{C}\)</span> e <span
class="math inline">\(\mathbb{R}^2\)</span>, <span
class="math inline">\(f\)</span> esteja associado a uma função
diferenciável, que também denotamos por <span
class="math inline">\(f\)</span>. Observe que <span
class="math display">\[\dfrac{\partial f}{\partial x}(z) =
\lim_{\substack{t \rightarrow 0\\t\in \mathbb{R}}}
\dfrac{f(z+t)-f(z)}{t}\]</span> <span
class="math display">\[\dfrac{\partial f}{\partial y}(z) =
\lim_{\substack{t \rightarrow 0\\t\in \mathbb{R}}}
\dfrac{f(z+it)-f(z)}{t}\]</span></p>
<div class="obs">
<p><strong>OBS 3</strong>. <em>Se <span class="math inline">\(f\)</span>
for holomorfa temos <span class="math inline">\(\dfrac{\partial
f}{\partial x}(z_0)= f&#39;(z_0)\)</span> e <span
class="math inline">\(\dfrac{\partial f}{\partial y}(z_0) = i
f&#39;(z_0)\)</span>.</em></p>
</div>
<div class="Def">
<p><strong>Definição 4</strong>. <em>Seja <span class="math inline">\(f:
\Omega \rightarrow \mathbb{C}\)</span> tal que ao fazer a identificação
com <span class="math inline">\(\mathbb{R}^2\)</span>, <span
class="math inline">\(f\)</span> seja diferenciável. Defina <span
class="math display">\[\dfrac{\partial f}{\partial
\overline{z}}=\dfrac{1}{2} \left(
  \dfrac{\partial f}{\partial x}-\dfrac{1}{i}\dfrac{\partial f}{\partial
y}\right),
  \quad \dfrac{\partial f}{\partial z}=\dfrac{1}{2}\left(
\dfrac{\partial f}{\partial x}
  +\dfrac{1}{i}\dfrac{\partial f}{\partial y}\right).\]</span></em></p>
</div>
<div class="prop">
<p><strong>Proposição 3</strong>. <em>Seja <span class="math inline">\(f
: \Omega \rightarrow \mathbb{C}\)</span> e <span
class="math inline">\(z_0 \in \Omega\)</span> com <span
class="math inline">\(f\)</span> holomorfa em <span
class="math inline">\(z_0\)</span>. Então <span
class="math display">\[\dfrac{\partial f}{\partial
\overline{z}}(z_0)=0,\quad
  f&#39;(z_0) = \dfrac{\partial f}{\partial z}(z_0).\]</span> Além
disso, escrevendo <span class="math inline">\(f: \Omega \subseteq
\mathbb{R}^2 \rightarrow \mathbb{R}^2\)</span>, <span
class="math inline">\(f(x,y)=(u(x,y),v(x,y))\)</span>. Então <span
class="math inline">\(f\)</span> é diferenciável no sentido usual e
<span class="math inline">\(det(\operatorname{Jac}_f) =
|f&#39;(z_0)|^2\)</span>, onde <span
class="math inline">\(\operatorname{Jac}_f\)</span> é o Jacobiano de
<span class="math inline">\(f\)</span>, dado por <span
class="math display">\[\operatorname{Jac}_f=\begin{pmatrix}
  \frac{\partial u}{\partial x}&amp;\frac{\partial u}{\partial y}\\
  \frac{\partial v}{\partial x}&amp;\frac{\partial v}{\partial y}
\end{pmatrix}.\]</span> .</em></p>
</div>
<div class="theorem">
<p><strong>Teorema 4</strong>. <em>Seja <span class="math inline">\(f =
u+iv\)</span> uma função definida em um aberto <span
class="math inline">\(\Omega\)</span>. Se <span
class="math inline">\(u\)</span> e <span
class="math inline">\(v\)</span> são diferenciáveis com derivadas
contínuas e satisfazem as equações de Cauchy-Riemann, então <span
class="math inline">\(f\)</span> é holomorfa e <span
class="math inline">\(f&#39;(z) = \dfrac{\partial f}{\partial
z}\)</span>.</em></p>
</div>
</body>
