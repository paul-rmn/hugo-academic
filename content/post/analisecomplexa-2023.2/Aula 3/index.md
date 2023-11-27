---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Análise complexa - aula 3"
subtitle: "Notas por Pedro Igor"
summary: ""
authors: []
tags: []
categories: []
date: 2023-08-29T20:05:00-03:00
lastmod: 2023-08-29T20:05:00-03:00
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


<p><strong>Aula de hoje:</strong> série de potências.</p>
<p><strong>Exemplo:</strong> <span class="math display">
\[e^x =1+x+\dfrac{x^2}{2!}+\dfrac{x^3}{3!}+...\]</span>
converge para todo <span class="math inline">\(x\)</span>
real e define uma função(infinitamente) diferenciável.</p>
<p>Hoje vamos ver, dentre outras coisas que <span
class="math inline">\(e^z = 1+z+\frac{z^2}{2!}+
\frac{z^3}{3!}+\cdots\)</span> converge para todo <span
class="math inline">\(z\in \mathbb{C}\)</span> e define uma função
holomorfa.</p>
<h2 id="convergência-de-séries">Convergência de séries</h2>
<div class="Def">
<p><strong>Definição 1</strong>. <em>Uma série de números complexos
<span class="math inline">\(\sum_{n=1}^{\infty}z_n\)</span> converge
para um número complexo <span class="math inline">\(z\)</span> se para
todo <span class="math inline">\(\epsilon &gt;0\)</span>, existe <span
class="math inline">\(N&gt;0,\)</span> tal que se <span
class="math inline">\(m_1&gt;m&gt;M\)</span> então <span
class="math display">\[\left|\sum_{n=m}^{m_1}z_n\right|&lt;\epsilon.\]</span>
Note que isso é equivalente a dizer que a sequência das somas parciais
<span class="math inline">\(S_m = \sum_{n=1}^mz_n\)</span> é uma
sequência de Cauchy.</em></p>
</div>
<div class="Def">
<p><strong>Definição 2</strong>. <em>A séire <span
class="math inline">\(\sum_{n=1}^{\infty}z_n\)</span> convege
absolutamente se <span
class="math inline">\(\sum_{n=1}^{\infty}|z_n|\)</span>
converge.</em></p>
</div>
<p>Assim como em análise Real, vale que se <span
class="math inline">\(\sum_{n=1}^{\infty}z_n\)</span> converge
absolutamente, então se <span class="math inline">\(f :
\mathbb{N}\rightarrow \mathbb{N}\)</span> é uma bijeção, então <span
class="math inline">\(\sum_{n=1}^{\infty}z_{f(n)}\)</span> também
converge para o mesmo valor. Além disso valem os testes:</p>
<ol>
<li><p>Teste da razão: se <span
class="math inline">\(\limsup|\dfrac{z_n}{z_{n+1}}|&lt;1\)</span>. Então
a série converge absolutamente.</p></li>
<li><p>Teste da raiz: se <span class="math inline">\(\limsup
|\sqrt[n]{|z_n|}|&lt;1\)</span> então a série converge
absolutamente.<br />
Lembrete: <span class="math inline">\(\limsup_{n \rightarrow \infty}z_n
= \sup\{L; \exists\)</span> subsequência <span
class="math inline">\(z_{n_k}\)</span> tal que <span
class="math inline">\(z_{n_k}\rightarrow L \}.\)</span></p>
<p>Usando qualquer um dos dois testes, vemos que a série <span
class="math inline">\(\sum_{n=1}^{\infty}\dfrac{z_n}{n!}\)</span>
converge <span class="math inline">\(\forall z.\)</span></p></li>
</ol>
<div class="Def">
<p><strong>Definição 3</strong>. <em>Uma série de potências é uma
expansão da forma <span
class="math inline">\(\sum_{n=1}^{\infty}a_nz^n\)</span> onde <span
class="math inline">\(\{a_n\}_{n \geqslant 0}\)</span> é uma sequência
de números complexos.<br />
</em></p>
</div>
<p>A idéia é estudar quando a série converge absolutamente.</p>
<div class="prop">
<p><strong>Proposição 1</strong>. <em>Dado umma série de potências <span
class="math inline">\(\sum_{n=1}^{\infty}a_nz^n\)</span>, existe <span
class="math inline">\(0 \leqslant R \leqslant \infty\)</span> tal
que</em></p>
<ul>
<li><p><em>Se <span class="math inline">\(|z|&lt;R\)</span>, a série
converge absolutamente;</em></p></li>
<li><p><em>se <span class="math inline">\(|z|&gt;R\)</span>, a série
diverge.<br />
</em></p></li>
</ul>
</div>
<div class="proof">
<p><em>Proof.</em> Seja <span class="math inline">\(L = \limsup_{n
\rightarrow \infty} \sqrt[n]{|a_n|}\)</span>, onde <span
class="math inline">\(L \in [0,\infty]\)</span>. Suponha inicialmente
que <span class="math inline">\(L \neq 0,\infty\)</span>. Neste caso,
note que <span class="math inline">\(\limsup_{n \rightarrow
\infty}\sqrt[n]{|a_n||z^n|} = L\cdot |z|\)</span>. Pelo teste da raíz,
se <span class="math inline">\(L|z|&lt;1\)</span>, a série converge
absolutamente e se <span class="math inline">\(L|z_n|&gt;1\)</span> a
série diverge. Logo, o resultado segue com <span class="math inline">\(R
= \dfrac{1}{L}\)</span>. Caso contrário, quando <span
class="math inline">\(L = 0\)</span> ou <span
class="math inline">\(\infty\)</span>, temos que <span
class="math inline">\(\limsup \sqrt[n]{|a_n|\cdot |z|^n}=0\)</span> ou
<span class="math inline">\(\infty\)</span>, respectivamente. Logo, no
primeiro caso a série converge <span class="math inline">\(\forall z
\neq 0\)</span> e no segundo caso a série diverge <span
class="math inline">\(\forall z \neq 0.\)</span> Finalmente, quando
<span class="math inline">\(z = 0\)</span> a série converge
trivialmente. ◻</p>
</div>
<p>OBS: Quando <span class="math inline">\(|z| = R\)</span> a proposição
nada diz sobre a série e, de fato, nada se pode dizer. Depende de cada
caso. Outros exemplos de séries convergentes são <span
class="math display">\[\cos(z) = \sum_{n=0}^{\infty} (-1)^n
\dfrac{z^{2n}}{(2n)!},\quad\operatorname{sen}(z) =
\sum_{n=0}^{+\infty}(-1)^n\dfrac{z^{2n+1}}{(2n+1)!}\]</span> e elas
coincidem com a definição usual quando <span class="math inline">\(z \in
\mathbb{R}\)</span>. Como essas séries convergem uniformemente, podemos
somar termo a termo e chegar em <span class="math display">\[\cos(z) =
\frac{e^{iz}+e^{-iz}}{2},\quad \operatorname{sen}(z) =
\frac{e^{iz}-e^{-iz}}{2i}.\]</span></p>
<p>Em particular, <span class="math display">\[e^{iz} = \cos (z) + i
\operatorname{sen}(z),\]</span> o que justifica a notação da aula 1.</p>
<div class="Def">
<p><strong>Definição 4</strong>. <em>Dada uma série de potências, o
número <span class="math inline">\(R\)</span> da proprosição acima é
chamado de raio de convergência.</em></p>
</div>
<p>Com isso, toda série de potências <span
class="math inline">\(\sum_{n=1}^{\infty}a_nz^n\)</span> define unma
função <span class="math inline">\(f: D_R(0) \rightarrow
\mathbb{C}\)</span>, dada por <span class="math inline">\(f(z)=
\sum_{n=1}^{\infty}a_nz^n\)</span>.</p>
<div class="theorem">
<p><strong>Teorema 1</strong>. <em>Uma série de potências <span
class="math inline">\(f(z)=\sum_{n=1}^{\infty}a_nz^n\)</span> define uma
função holomorfa em seu disco de convergência <span
class="math inline">\(D_R(0) = \{z \in \mathbb{C}; |z|&lt;R\}.\)</span>
A derivada de <span class="math inline">\(f\)</span> também é dada por
uma série de potências e é obtida diferenciando termo a dermo. Isto é
<span class="math display">\[f&#39;(z) = \sum_{n=0}^{\infty}na_nz^{n-1}
= \sum_{n=0}^{\infty}(n+1)a_{n+1}z^n.\]</span> Além disso, o raio de
convergência de <span class="math inline">\(f&#39;\)</span> é o mesmo de
<span class="math inline">\(f\)</span>.</em></p>
</div>
<ul>
<li><p><span class="math inline">\(R_{f&#39;} = R_f\)</span>. De fato,
<span class="math display">\[R_{f&#39;} = \limsup_{n \rightarrow
\infty}\sqrt[n]{na_n}\]</span> <span class="math display">\[\Rightarrow
R_{f&#39;} = \limsup_{n \rightarrow
\infty}\sqrt[n]{n}\sqrt[n]{|a_n|}\]</span> <span
class="math display">\[\Rightarrow R_{f&#39;} = \lim_{n \rightarrow
\infty}\sqrt[n]{n} \cdot \limsup_{n \rightarrow
\infty}\sqrt[n]{|a_n|}\]</span> <span class="math display">\[\Rightarrow
R_{f&#39;} = 1 \cdot R_f .\]</span> Note que essa prova usa o seguinte
resultado de análise real: se <span class="math inline">\(\lim_{n
\rightarrow \infty}x_n = x&gt;0\)</span> e <span
class="math inline">\(\limsup_{n \rightarrow \infty}y_n = y\)</span>,
então <span class="math inline">\(\limsup_{n\rightarrow \infty}x_n\cdot
y_n = x\cdot y\)</span>.</p></li>
<li><p>Seja <span class="math inline">\(g(z) =
\sum_{n=0}^{+\infty}na_nz^{n+1}\)</span> definida em <span
class="math inline">\(D_R(0)\)</span>. Seja <span
class="math inline">\(z_0 \in D_R(0)\)</span> e <span
class="math inline">\(r\)</span> tal que <span
class="math inline">\(|z_0|&lt;r&lt;R\)</span>. Seja <span
class="math inline">\(N \in \mathbb{N}\)</span>, façamos <span
class="math display">\[f(z) = S_N(z)+E_N(z),\]</span> onde <span
class="math display">\[S_N(z) = \sum_{n=1}^Na_nz^n,\quad E_N(z) =
\sum_{n = N+1}^{+\infty}a_nz^n.\]</span> Dado <span
class="math inline">\(h\)</span> com <span
class="math inline">\(|h|\)</span> suficientemente pequeno <span
class="math inline">\((|z_0+h|&lt;r)\)</span>, uma vez que <span
class="math inline">\(S_N(z)\)</span> é polinômio, podemos escrever
<span class="math display">\[\begin{gathered}
\frac{f(z_0+h)-f(z_0)}{h}-g(z_0) =
\frac{S_N(z_0+h)-S_N(z_0)}{h}-S_N&#39;(z_0) \\
+\frac{E_N(z_0+h)-E_N(z_0)}{h}-(g(z_0) -  S_N&#39;(z_0)).
\end{gathered}\]</span> Em particular, <span
class="math display">\[\begin{gathered}
\left|\frac{f(z_0+h)-f(z_0)}{h}-g(z_0)\right| \le
\left|\frac{S_N(z_0+h)-S_N(z_0)}{h}-S_N&#39;(z_0)\right| \\
+\left|\frac{E_N(z_0+h)-E_N(z_0)}{h}\right|
+\Big|(g(z_0)-S_N&#39;(z_0))\Big|.
\end{gathered}\]</span> Agora, vamos estimar cada uma das parcelas do
lado direito.</p>
<p>Observe que: <span class="math display">\[\left|
\dfrac{E_N(z_0+h)-E_N(z_0)}{h} \right| \leqslant \sum_{n =
N+1}^{\infty}|a_n|\left| \dfrac{(z_0+h)^n-z_0^n}{h}\right|.\]</span>
Mas, <span
class="math display">\[(z_0+h)^n-z_0^n=h((z_0+h)^{n-1}+(z_0+h)^{n-2}h+...+z_0^{n-1})\]</span>
<span class="math display">\[\Rightarrow |(z_0+h)^n-z_0^n| \leqslant
|h|(r^{n-1}+r^{n-1}+...r^{n-1}) = n|h|r^{n-1}\]</span></p>
<p><span class="math display">\[\Rightarrow \left|
\dfrac{E_N(z_0+h)-E_N(z_0)}{h} \right| \leqslant \sum_{n =
N+1}^{+\infty}n|a_n|R^{n-1}.\]</span> Uma vez que <span
class="math inline">\(r&lt;R\)</span> e <span class="math inline">\(g(z)
= \sum_{n=0}^{+\infty}na_nz^{n-1}\)</span> converge absolutamente em
<span class="math inline">\(D_R(0)\)</span>,<span
class="math inline">\(G_N(r)\)</span> é o rabo de uma série convergente
e, portanto, se N for suficientemente grande, temos <span
class="math inline">\(G_N(r)&lt;\epsilon\)</span>.<br />
Por outro lado, pela definição de <span
class="math inline">\(g(z)\)</span>, <span class="math inline">\(\lim_{N
\rightarrow \infty}S_N&#39;(z_0) = g(z_0)\)</span>. Logo, mais uma vez,
para N suficientemente grande , <span
class="math inline">\(|g(z_0)-S_N&#39;(z_0)|&lt;\epsilon
.\)</span><br />
Conclusão: se N é suficientemente grande, <span
class="math display">\[\left| \dfrac{f(z_0+h)-f(z_0)}{h} - g(z_0)
\right| \leqslant \left| \dfrac{S_N(z_0+h)-S_N(z_0)}{h}-S_N&#39;(z_0)
\right| +2\epsilon.\]</span> Agora, fizemos N e tomamos h
suficientemente pequeno, tal que <span class="math display">\[\left|
\dfrac{S_N(z_0+h)-S_N(z_0)}{h}-S_N&#39;(z_0) \right| &lt;
\epsilon\]</span> Ou seja, para h suficientemente pequeno, <span
class="math display">\[\left| \dfrac{f(z_0+h)-f(z_0)}{h} - g(z_0)
\right| &lt; 2 \epsilon.\]</span> Como <span
class="math inline">\(\epsilon &gt; 0\)</span> é arbitrário, o resultado
segue.</p></li>
</ul>
<div class="corollary">
<p><strong>Corolário 1</strong>. <em>Uma série de potências define uma
função infinitamente derivável e todas as suas derivadas são dadas por
séries de potências com o mesmo raio de convergência.</em></p>
</div>
<div class="Def">
<p><strong>Definição 5</strong>. <em>Dado <span
class="math inline">\(z_0 \in \mathbb{C}\)</span>, uma série de
potências centrada em <span class="math inline">\(z_0\)</span> é uma
série da forma <span
class="math inline">\(\sum_{n=0}^{+\infty}a_n(z-z_0)^n\)</span> onde
<span class="math inline">\(\{a_n\}_{n\geqslant 0}\)</span> é uma
sequência de números complexos.<br />
</em></p>
</div>
<p>Todos os resultados sobre séries da forma <span
class="math inline">\(\sum a_nz^n\)</span> continuam válidos trocando
<span class="math inline">\(|z|&lt;R\)</span> por <span
class="math inline">\(|z-z_0|&lt;R\)</span>, etc.</p>
<div class="Def">
<p><strong>Definição 6</strong>. <em>Seja <span
class="math inline">\(\Omega\)</span> um domínio e <span
class="math inline">\(f: \Omega \rightarrow \mathbb{C}\)</span>. Dizemos
que <span class="math inline">\(f\)</span> é analítica se <span
class="math inline">\(\forall z_0 \in \Omega\)</span>, existe <span
class="math inline">\(\delta &gt; 0\)</span> tal que se <span
class="math inline">\(|z-z_0|&lt;\delta\)</span>, <span
class="math inline">\(f(z)\)</span> é dado por uma série de potências
centrada em <span class="math inline">\(z_0\)</span>. Isto é, existe
umma sequência <span class="math inline">\(\{a_n\}\)</span> dependendo
de <span class="math inline">\(z_0\)</span> tal que <span
class="math display">\[\sum_{n=0}^{+\infty}a_n(z-z_0)^n,\quad
|z-z_0|&lt;\delta.\]</span></em></p>
</div>
<p>OBS: Assim como em <span class="math inline">\(\mathbb{R}\)</span>,
valem as formulas <span class="math inline">\(a_n =
\dfrac{f^{(n)}(z_0)}{n!}\)</span>.</p>
<h2 id="caminhos-em-mathbbc">Caminhos em <span
class="math inline">\(\mathbb{C}\)</span></h2>
<div class="Def">
<p><strong>Definição 7</strong>. <em>TO BE CONTINUED...</em></p>
</div>
