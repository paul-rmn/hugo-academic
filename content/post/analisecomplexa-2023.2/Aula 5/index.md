---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Análise complexa - aula 5"
subtitle: "Notas por Pedro Igor"
summary: ""
authors: []
tags: []
categories: []
date: 2023-09-12T10:36:00-03:00
lastmod: 2023-09-12T10:36:00-03:00
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

<p>Na aula passada, vimos que se <span class="math inline">\(f\)</span>
é holomorfa em um dimínio contendo um triângulo T em seu interior, então
<span class="math display">\[\int_{T}f(z)dz = 0.\]</span> Agora, vamos
usar esse resultado para provar o teorema seguinte.</p>
<h2 id="existência-da-primitiva">Existência da primitiva</h2>
<div class="theorem">
<p><strong>Teorema 1</strong>. <em>Seja <span class="math inline">\(D =
D_R(z_0)\)</span> um disco aberto e seja <span class="math inline">\(f:
D \rightarrow \mathbb{C}\)</span> uma fração holomorfa. Então <span
class="math inline">\(f\)</span> possui uma primitiva em <span
class="math inline">\(D\)</span>.</em></p>
</div>
<p>Prova: Dado <span class="math inline">\(z \in D\)</span>, defina
<span class="math display">\[F(z) = \int_{\gamma}f(w)dw ,\]</span> onde
<span class="math inline">\(\gamma\)</span> é o segmento ligando <span
class="math inline">\(z_0\)</span> a <span
class="math inline">\(z\)</span>. Tome <span class="math inline">\(h \in
\mathbb{C}\)</span> pequeno suficiente de modo que <span
class="math inline">\(z+h \in D\)</span>.<br />
</p>
<div class="center">

</div>
<p>Olhando para o triângulo cujos vértices são <span
class="math inline">\(z_0,z,z+h\)</span> e usando o Teorema de
Goursat,temos: <span class="math display">\[F(z)+\int_{\gamma_{h}}f(w)dw
- F(z+h) = 0,\]</span> onde <span
class="math inline">\(\gamma_{h}\)</span> é o segmento de reta ligando
<span class="math inline">\(z\)</span> a <span
class="math inline">\(z+h\)</span>.Note que assumimos que os pontos não
são colineares. O caso que eles são colineares é trivial.Ou seja, <span
class="math inline">\(F(z+h)-F(z) = \int_{\gamma_h}f(w)dw\)</span>. Como
<span class="math inline">\(f\)</span> é contínua e <span
class="math inline">\(|z-w|&lt;|h|, \forall w \in \gamma_h\)</span>,
dado <span class="math inline">\(\epsilon &gt;0\)</span>, existe <span
class="math inline">\(\delta\)</span> tal que se <span
class="math inline">\(|h|&lt; \delta\)</span>, então <span
class="math inline">\(|f(w)-f(z)|&lt; \epsilon .\)</span>
Consequentemente, <span
class="math display">\[\int_{\gamma_h}f(w)dw=\int_{\gamma_h}f(z)dw+\int_{\gamma}(f(w)-f(z))dw\]</span>
<span class="math display">\[= f(z)\cdot [(z+h)-z]+I,\]</span> onde
<span class="math inline">\(|I| \leqslant \epsilon |h|.\)</span>Logo,
<span class="math display">\[\left| \dfrac{F(z+h)-F(z)}{h}-f(z)
\right|&lt; \epsilon.\]</span></p>
<div class="corollary">
<p><strong>Corolário 1</strong>. <em>Se f é holomorfa em um disco <span
class="math inline">\(D\)</span> e <span
class="math inline">\(\gamma\)</span> é um caminho fechado contido em D.
Então , <span class="math display">\[\int_{\gamma}f(z)dz =
0.\]</span></em></p>
</div>
<p>Prova: Como <span class="math inline">\(f\)</span> possui primitiva,
segue de <span class="math inline">\((Referencia)\)</span> teorema da
aula passada.</p>
<h2 id="interior">Interior</h2>
<p>Ainda não definimos o que significa o <span
class="math inline">\(\textbf{interior}\)</span> de uma curva,
entretanto, para algumas curvas, essa noção é clara. Por exemplo:</p>
<div class="center">
<p><img src="./contornos.png" alt="image" /></p>
</div>
<p>Assuma por hoje que para as regioes acima, vale o seguinte:</p>
<ol>
<li><p>O interior está bem definido;</p></li>
<li><p><span class="math inline">\(\int_{\gamma}f(w)dw\)</span>
independe do caminho poligonal <span
class="math inline">\(\gamma\)</span> escolhido.</p></li>
</ol>
<p>Com estas hipóteses podemos repetir a prova de teorema do começo da
aula e deduzir que <span class="math inline">\(F\)</span> é uma
primitiva de <span class="math inline">\(f\)</span>.Em particular, dado
qualquer caminho fechado no interior de um dos exemplos acima, temos que
<span class="math display">\[\int_{\gamma}f(z)dz = 0.\]</span></p>
<h2 id="aplicações-ao-cálculo-de-integrais">Aplicações ao cálculo de
integrais</h2>
<p>Exemplos:</p>
<ol>
<li><p><span class="math display">\[\int_{-\infty}^{+\infty} e^{-\pi
x^2} \cdot e^{-2\pi xy}dx = e^{-\pi y^2}.\]</span><br />
Como a funcão <span class="math inline">\(z \rightarrow e^{-\pi
z^2}\)</span> é holomorfa em todo o plano complexo <span
class="math inline">\(\mathbb{C}\)</span>, temos que <span
class="math display">\[\int_{\gamma}f(z)dz = 0\]</span> para toda curva
fechada <span class="math inline">\(\gamma\)</span>. Considere o caso em
que <span class="math inline">\(\gamma\)</span> é o retângulo cujos
vértives são <span class="math inline">\(-R,R,R+iy,-R+iy\)</span>. Sejam
<span class="math inline">\(\gamma_1, \gamma_2,\gamma_3\)</span> e <span
class="math inline">\(\gamma_4\)</span> os segmentos <span
class="math inline">\([-R,R],[R,R+iy],[R+iy,-R+iy],[-R+iy,-R]\)</span>,
nesta ordem.</p>
<div class="center">

</div>
<p><span class="math display">\[\int_{\gamma_1}f(z)dz =
\int_{-R}^{R}e^{-\pi x^2}dx\]</span> <span
class="math display">\[\int_{\gamma_2}f(z)dz = \int_0^y e^{-\pi
(R+ix)^2}dx\]</span> <span class="math display">\[\int_{\gamma_3}f(z)dz
= \int_{-R}^R e^{-\pi (x^2+2ixy -y^2)}dx\]</span> <span
class="math display">\[\int_{\gamma_4}f(z)dz = \int_0^y e^{-\pi
(-R+ix)^2}dx\]</span> Observe que <span class="math display">\[\left|
\int_{\gamma_2}f(z)dz \right|\leqslant \int_0^y e^{-\pi (R^2-x^2)}dx
\leqslant \int_0^y e^{-\pi(R^2-y^2)}dx = ye^{\pi y^2} \cdot e^{-\pi
R^2}\]</span> Em particular, <span
class="math inline">\(\int_{\gamma_2}f(z)dz \rightarrow 0\)</span>
quando <span class="math inline">\(R \rightarrow +\infty\)</span>. De
maneira análoga, <span class="math inline">\(\int_{\gamma_4}f(z)dz
\rightarrow 0\)</span> quando <span class="math inline">\(R \rightarrow
+\infty .\)</span> Por fim , <span
class="math display">\[\int_{\gamma_3}f(z)dz = -
\int_{-R}^{R}e^{-\pi(x+iy)^2}dx = -e^{\pi y^2}
\int_{-R}^Re^{-\pi(x^2+2ixy)}dx\]</span> Fazendo <span
class="math inline">\(R \rightarrow 0:\)</span> <span
class="math display">\[\int_{-\infty}^{\infty}e^{-\pi x^2}dx - e^{\pi
y^2} \int_{-\infty}^{\infty}e^{-\pi(x^2+2xyi)}dx = 0\]</span> <span
class="math display">\[\Rightarrow \int_{-\infty}^{+\infty}e^{-\pi
(x^2+2ixy)}= e^{-\pi y^2} \int_{-\infty}^{+\infty}e^{-\pi x^2}dx =
e^{-\pi y^2}.\]</span> Para ver que <span
class="math inline">\(\int_{-\infty}^{+\infty}e^{-\pi x^2}dx =
1\)</span>, podemos, por exemplo, utilizar o teorema de Fubini: <span
class="math display">\[I = \int e^{-\pi x^2}dx \Rightarrow I^2 = \int
\int e^{-\pi (x^2+y^2)}dx dy ,\]</span> usando coordenadas polares,
<span class="math display">\[I^2 = \int_0^{2\pi} \int_0^{+\infty} r dr d
\theta = 2\pi \left[ \dfrac{e^{-\pi x^2}}{-2\pi} \right]_0^{+\infty} =
1\]</span></p></li>
<li><p><span
class="math display">\[\int_0^{+\infty}\frac{1-\cos(x)}{x^2}dx =
\frac{\pi}{2}.\]</span> Note que <span class="math inline">\(\cos (x) =
\frac{e^{ix}+e^{-ix}}{2}\)</span>, então basta mostrar que <span
class="math display">\[\int_{-\infty}^{+\infty}\dfrac{1-e^{-ix}}{x^2} =
\pi .\]</span></p>
<p>Seja <span class="math inline">\(\gamma\)</span> o contorno do
semi-anel superior (<span
class="math inline">\(\mathrm{Im}(z)&gt;0\)</span>) de raio interior
<span class="math inline">\(\epsilon\)</span> e exterior R.</p>
<div class="center">

</div>
<p>Sejam <span class="math inline">\(\gamma_R\)</span> o semicírculo de
raio <span class="math inline">\(R\)</span> partindo de <span
class="math inline">\(R\)</span> e terminando em <span
class="math inline">\(-R\)</span>, <span
class="math inline">\(\gamma_{\epsilon}\)</span> o semicírculo de raio
<span class="math inline">\(\epsilon\)</span> partindo de <span
class="math inline">\(\epsilon\)</span> e terminando em <span
class="math inline">\(-\epsilon\)</span>, <span
class="math inline">\(\gamma^-\)</span> o segmento <span
class="math inline">\([-R,-\epsilon]\)</span> e <span
class="math inline">\(\gamma^+\)</span> o segmento <span
class="math inline">\([\epsilon,R]\)</span>. Observe que o integrando é
dado por uma função holomorfa no interior da curva <span
class="math inline">\(\gamma\)</span>. Logo, temos</p>
<p><span class="math display">\[\int_{\gamma}\frac{1-\cos
z}{z^2}dz=0.\]</span></p>
<p>Note que para todo <span class="math inline">\(z=x+iy\in
\gamma_R\)</span>, tem-se <span class="math inline">\(y&gt;0\)</span> e,
portanto, vale a desigualdade <span
class="math display">\[\left|\frac{1-e^{iz}}{z^2}\right|\leq
\frac{1+|e^{iz}|}{z^2}=\frac{1+e^{-y}}{z^2}\leq \frac{2}{z^2}.\]</span>
E, portanto, <span class="math display">\[\begin{aligned}
\left|\int_{\gamma_R}\frac{1-\cos z}{z^2}dz \right|&amp;\leq \sup_{z\in
\gamma_R}\left(\frac{2}{|z|^2} \right)\cdot \pi R\\
&amp;=\frac{2\pi R}{R^2}=\frac{2\pi}{R}\xrightarrow[R\rightarrow
+\infty]{} 0.
\end{aligned}\]</span> Lembre que <span
class="math display">\[e^{iz}=1+iz+\frac{(iz)^2}{2}+\frac{(iz)^3}{3!}+\ldots.\]</span>
Logo, <span class="math inline">\(e^{iz}=1+iz+z^2g(z)\)</span>, onde
<span class="math inline">\(g(z)\)</span> é uma função holomorfa. Com
isso, conclu ’imos que <span
class="math display">\[\frac{1-e^{iz}}{z^2}=\frac{-i}{z}-g(z).\]</span>
Já que <span class="math inline">\(g\)</span> é holomorfa, existe uma
constante positiva <span class="math inline">\(C\)</span> tal que <span
class="math inline">\(|g(z)|&lt;C\)</span> sempre que <span
class="math inline">\(|z|&lt;1\)</span>. Isto nos permite escrever <span
class="math display">\[\int_{\gamma_\epsilon}\frac{1-\cos
z}{z^2}dz=-I_1-I_2,\]</span> onde <span
class="math inline">\(I_1=\int_{\gamma_\epsilon}\frac{dz}{z}\)</span> e
<span class="math inline">\(I_2=\int{\gamma_\epsilon}g(z)dz\)</span>.
Note que para todo <span class="math inline">\(\epsilon\)</span>
suficientemente pequeno, <span class="math display">\[|I_2|\leq C\cdot
\pi \epsilon.\]</span> Por outro lado, <span
class="math display">\[I_1=\int_0^\pi\frac{\epsilon i e^{it}}{\epsilon
e^{it}}dt=i\int_0^\pi dt=i\pi.\]</span></p>
<p>Fazendo <span class="math inline">\(R\rightarrow\infty\)</span> e
<span class="math inline">\(\epsilon\rightarrow 0\)</span>, temos</p>
<p><span class="math display">\[\int_{-\infty}^\infty\frac{1-\cos
x}{x^2}dz=-\pi\]</span></p>
<p>Na próxima aula, provaremos o seguinte resultado:</p>
<div class="theorem">
<p><strong>Teorema 2</strong> (Fórmula integral de Cauchy). <em>Seja
<span class="math inline">\(f\)</span> uma função holomorfa em um aberto
contendo o feixo de um disco aberto <span
class="math inline">\(D=D_R(z_0)\)</span>. Seja <span
class="math inline">\(C\)</span> o contorno do disco <span
class="math inline">\(D\)</span> com orientação positiva. Então <span
class="math display">\[f(z)=\int_{C}\frac{f(w)}{w-z}dw,\quad z\in
D\]</span></em></p>
</div></li>
</ol>




