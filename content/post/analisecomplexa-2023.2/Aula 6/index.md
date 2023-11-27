---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Análise complexa - aula 6"
subtitle: "Notas por Pedro Igor"
summary: ""
authors: []
tags: []
categories: []
date:    2023-09-12T10:37:00-03:00
lastmod: 2023-09-12T10:37:00-03:00
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


<h2 id="fórmula-de-cauchy">Fórmula de Cauchy</h2>
<div class="theorem">
<p><strong>Teorema 1</strong>. <em>Seja <span class="math inline">\(f:
\Omega \rightarrow \mathbb{C}\)</span> uma função holomorfa e seja <span
class="math inline">\(D = D_{\delta}(z_0)\)</span> tal que <span
class="math inline">\(\overline{D} \subseteq \Omega\)</span>. Se <span
class="math inline">\(C\)</span> denota o bordo de D no sentindo
positivo. Então, <span class="math display">\[f(z) =
\dfrac{1}{2i\pi}\int_C \dfrac{f(z)}{w-z}dw , \forall z \in
D.\]</span></em></p>
</div>
<p>PV. Observe que a função <span class="math inline">\(f(w) =
\dfrac{f(w)}{w-z}\)</span> é holomorfa em <span
class="math inline">\(\Omega - \{z\}\)</span>. Em particular ela é
holomorfa no interior do contorno <span
class="math inline">\(\Gamma_{\delta , \epsilon}\)</span>. Logo, pelo
teorema de Cauchy, <span
class="math display">\[\int_{\Gamma_{\delta,\epsilon}}F(w)dw =
0.\]</span> Fazendo <span class="math inline">\(\epsilon \rightarrow
0\)</span>, obtemos que : <span class="math display">\[\lim_{\epsilon
\rightarrow 0} \int_{\Gamma_{\delta , \epsilon}}F(w) dw  =
\int_{C}F(w)dw - \int_{C_{\delta}}F(w)dw+\int_{\gamma_0}F(w)dw -
\int_{\gamma_0}F(w)dw\]</span></p>
<p><span class="math display">\[\Rightarrow \lim_{\epsilon \rightarrow
0} \int_{\Gamma_{\delta , \epsilon}}F(w) dw  = \int_C
\dfrac{f(w)}{w-z}dw - \int_{C_{\delta}}\dfrac{f(w)}{w-z},\]</span> onde
<span class="math inline">\(\gamma_0\)</span> é o segmento do raio que
passa por <span class="math inline">\(z\)</span> e liga <span
class="math inline">\(C_{\delta}\)</span> a <span
class="math inline">\(C\)</span>. Como a igualdade acima é independente
de <span class="math inline">\(\delta\)</span> temos que <span
class="math display">\[\int_{C}\dfrac{f(w)}{w-z}dw = \lim_{\delta
\rightarrow 0} \int_{C_{\delta}} \dfrac{f(w)}{w-z}dw.\]</span> Como
<span class="math inline">\(f\)</span> é holomorfa em <span
class="math inline">\(z\)</span>, dado <span
class="math inline">\(\epsilon &gt;0, \exists \delta &gt; 0\)</span> tal
que se <span class="math inline">\(|w-z| \leqslant \delta,\)</span>
então <span class="math display">\[\left| \dfrac{f(w)-f(z)}{w-z} -
f&#39;(z) \right| &lt; \epsilon .\]</span> Isto implica que <span
class="math display">\[\left| \int_{C_{\delta}} \left( \dfrac{f(w)}{w-z}
- \dfrac{f(z)}{w-z} - f&#39;(z) \right) dw \right| &lt; 2 \pi \epsilon
\delta .\]</span> Mas, observe que <span
class="math display">\[\int_{C_{\delta}}\dfrac{f(z)}{w-z}dw = f(z)
\int_{C_{\delta}} \dfrac{dw}{w-z} = f(z) \int_0^{2 \pi} \dfrac{i \delta
e^{i \theta}}{\delta e^{i \theta}}d \theta = 2 \pi i f(z)\]</span>. Além
disso, sabemos que <span
class="math display">\[\int_{C_{\delta}}f&#39;(z) dw = 0\]</span> Logo,
podemos concluir que <span class="math display">\[\left|
\int_{C_{\delta}} \dfrac{f(w)}{w-z}dw - 2 \pi i f(z) \right| = \left|
\int_{C_{\delta}} \left( \dfrac{f(w) - f(z)}{w-z} - f&#39;(z) \right) dw
\right| &lt; 2 \pi \epsilon \delta &lt; 2 \pi \epsilon.\]</span> Note
que a última igualdade vem do fato que poderiamos ter tomado <span
class="math inline">\(\delta &lt; 1.\)</span> Portanto , <span
class="math display">\[\lim_{\delta \rightarrow 0}\int_{C_{\delta}}
\dfrac{f(z)}{w-z}dw = 2 \pi i f(z).\]</span> Concluímos a demonstração
lembrando que <span class="math inline">\(\int_C
\dfrac{f&#39;(z)}{w-z}dw =
\int_{C_{\delta}}\dfrac{f(w)}{w-z}dw\)</span>.</p>
<h2 id="corolários">Corolários</h2>
<div class="corollary">
<p><strong>Corolário 1</strong>. <em>Sob as mesmas hipóteses do teorema,
temos <span class="math display">\[f^{(n)}(z) = \dfrac{n!}{2i\pi}\int_C
\dfrac{f(z)}{(w-z)^{n+1}}dw , \forall z \in D.\]</span></em></p>
</div>
<p>PV. Seja <span class="math inline">\(z \in \Omega\)</span> e h
suficientemente pequeno de modo que <span class="math inline">\(z+h \in
D.\)</span> Então, <span class="math display">\[f(z+h)-f(z) =
\dfrac{1}{2 \pi i} \int_{C} \dfrac{f(z)}{w-z-h}dw - \dfrac{1}{2\pi
i}\int_C \dfrac{f(w)}{w-z}dw\]</span> <span
class="math display">\[\Rightarrow f(z+h)-f(z) = \dfrac{1}{2\pi i}
\int_C f(w) \left[ \dfrac{1}{w-z-h}- \dfrac{1}{w-z} \right] dw.\]</span>
Observe que <span class="math inline">\(\dfrac{1}{w-z-h}-
\dfrac{1}{w-z}  = \dfrac{h}{(w-z)(w-z-h)}\)</span>. Portanto, <span
class="math display">\[\dfrac{f(z+h)-f(z)}{h} =  \int_C
\dfrac{f(w)}{(w-z)(w-z-h)}dw\]</span> Queremos mostrar que <span
class="math inline">\(I_h \rightarrow I:= \int_C
\dfrac{f(w)}{(w-z)^2}dw\)</span> quando <span class="math inline">\(h
\rightarrow 0\)</span>. De fato, <span class="math display">\[I_h-I  =
\int_C \dfrac{f(w)}{w-z}\left( -\dfrac{1}{w-z-h}+ \dfrac{1}{w-z} \right)
dw = \int_C \dfrac{f(w)h}{(w-z)^2(w-z-h)}dw\]</span> Então, se <span
class="math inline">\(|h|&lt; \dfrac{|w-z|}{2},\)</span> temos: <span
class="math display">\[\left| \dfrac{f(w)h}{(w-z)^2(w-z-h)} \right|
\leqslant \dfrac{2 \sup_{w \in C}|f(w)| \cdot |h|}{|w-z|^3} \leqslant M
\cdot |h|\]</span> Onde M é uma constante. Lembre que <span
class="math inline">\(z\)</span> e <span
class="math inline">\(C\)</span> estão fixos. Portanto: <span
class="math inline">\(|I - I_h| \leqslant M \cdot |h| \cdot l(c)
\leqslant M&#39; |h|,\)</span> onde <span
class="math inline">\(M&#39;\)</span> é uma outra constante. Com isso
concluímos que <span class="math inline">\(I_h \rightarrow I\)</span>
quando <span class="math inline">\(h \rightarrow 0\)</span> e
completamos a prova para <span class="math inline">\(n = 1.\)</span>
Vamos agora considerar o caso geral. Ultilizaremos indução. O caso
inicial(<span class="math inline">\(n =0\)</span>) é a fórmula de Cauchy
(e o caso <span class="math inline">\(n = 1\)</span> foi demonstrado).
Suponha agora que a fórmula seja válida para um certo valor <span
class="math inline">\(n\)</span>, isto é: <span
class="math display">\[f^{(n)}(z) = \dfrac{n!}{2i\pi}\int_C
\dfrac{f(z)}{(w-z)^{n+1}}dw , \forall z \in D.\]</span> Seja, mais uma
vez, <span class="math inline">\(h\)</span> suficientemente pequeno,
temos</p>
<div class="corollary">
<p><strong>Corolário 2</strong>. <em>Seja f holomorfa em um aberto
contendo um disco <span class="math inline">\(D = D_R(z_0)\)</span> e
seja C o seu bordo. Então vale a desigualdade <span
class="math display">\[|f^{(n)}(z_0)| \leqslant \dfrac{n! \cdot \sup_{w
\in C}|f(w)|}{R^n}\]</span></em></p>
</div>
<p>PV. Pelo corolário acima, <span class="math display">\[f^{(n)}(z) =
\dfrac{n!}{2i\pi}\int_C \dfrac{f(z)}{(w-z)^{n+1}}dw\]</span> <span
class="math display">\[\Rightarrow |f^{(n)}(z_0)| \leqslant
\dfrac{n!}{2\pi} \cdot \dfrac{\sup_{w \in C}|f(w)|}{R^{n+1}} \cdot 2\pi
R\]</span></p>
<div class="corollary">
<p><strong>Corolário 3</strong>. <em>Seja <span class="math inline">\(f:
\Omega \rightarrow \mathbb{C}\)</span> uma função holomorfa definida em
um aberto <span class="math inline">\(\Omega\)</span>. Se D é um disco
aberto do centro <span class="math inline">\(z_0\)</span>, contido em
<span class="math inline">\(\Omega\)</span> então f possui uma
representação em série de potências em torno de <span
class="math inline">\(z_0\)</span> no disco D, dada por <span
class="math display">\[f(z) = \sum_{n=0}^{\infty}a_n(z-z_0)^n\]</span>
Além disso, os coeficientes são dados pela seguinte fórmula: <span
class="math display">\[a_n = \dfrac{f^{(n)}(z_0)}{n!} ,(n \geqslant
0).\]</span></em></p>
</div>
<p>PV. Observe que <span class="math display">\[\dfrac{1}{w-z} =
\dfrac{1}{(w-z_0)-(z-z_0)} = \dfrac{1}{w-z}\left( \dfrac{1}{1-
\dfrac{z-z_0}{w-z_0}} \right).\]</span> Como <span
class="math inline">\(z \in D\)</span>, existe <span
class="math inline">\(r &lt; 1\)</span> tal que <span
class="math display">\[\dfrac{|z-z_0|}{w-z_0}&lt;r&lt;1.\]</span> Em
particular, temos pela série geométrica que <span
class="math display">\[\dfrac{1}{1- \dfrac{z-z_0}{w-z_0}} =
\sum_{n=0}^{\infty} \left( \dfrac{z-z_0}{w-z_0} \right) ^n ,\]</span>
com convergência uniforme em relação a w. Portanto, pela fórnula de
Cauchy, temos : <span class="math display">\[f(z) = \dfrac{1}{2\pi i}
\int_{C}\dfrac{f(z)}{w-z}dw\]</span> <span class="math display">\[f(z) =
\dfrac{1}{2\pi i}\int_{C} \dfrac{f(w)}{w-z_0}\sum_{n=0}^{+\infty} \left(
\dfrac{z-z_0}{w-z_0} \right)^n dw\]</span> <span
class="math display">\[f(z) = \sum_{n=0}^{+\infty}(z-z_0)^n \cdot
\dfrac{1}{2\pi i } \int_C \dfrac{f(w)}{(w-z_0)^{n+1}}dw\]</span> <span
class="math display">\[f(z) = \sum_{n=0}^{+\infty}\dfrac{f^(n)(z_0)}{n!}
\cdot (z-z_0)^n ,\]</span> onde, no último passo, utilizaremos o
primeiro corolário decorrente das fórmulas de Cauchy.  </p>