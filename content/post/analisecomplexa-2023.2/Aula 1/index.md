---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Análise complexa - aula 1"
subtitle: "Notas por Pedro Igor"
summary: ""
authors: []
tags: []
categories: []
date: 2023-08-11T01:46:00-03:00
lastmod: 2023-08-11T01:46:00-03:00
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

### Apresentação do curso.

#### Conceitos Gerais
{{< math >}}
Nesse curso, vamos considerar $f: U \rightarrow \mathbb{C}$, onde U é um
conjunto aberto de C. Ou seja, a princípio, isto é o mesmo que uma função
definida em um aberto de $\mathbb{R}$, a diferença vem a seguir.

<br><br>
<strong>Definição:</strong>
$f$ é dita holomorfa em um ponto $z \in \mathbb{C}$ se o limite
$$\lim_{h\rightarrow 0}\dfrac{f(z+h)-f(z)}{h}$$ existe.
<br><br>

Em $\mathbb{R}^2$, $f$ é dita diferenciável em $(x_0,y_0)$ se existe $D_f \in M_{2\times 2}(\mathbb{R})$ tal que $$\lim_{(u,v)\rightarrow 0}\dfrac{|f(x+u,y+v)-f(x,y)-D_f.
\left[
\begin{array}{c}
u\\
v
\end{array}
\right]
|}{|(u,v)|}.$$
Note $D_f =$
$
\left[
\begin{array}{cc}
a&b \\
c&d
\end{array}
\right]
$,
$$\Rightarrow D_f.
\left[
\begin{array}{c}
u\\
v
\end{array}
\right]
=
\left[
\begin{array}{c}
au+bv\\
cu+dv
\end{array}
\right]
. $$
Além disso, lembre que $$L = m+ni, h = u+iv \Rightarrow Lh = (mu-nv)+i(mv+nu).$$

Veja que se tomarmos $$a=m,b=-n,c=n,d=m$$ os dois casos tornam-se equivalentes. Ou seja, f ser holomorfa é "equivalente" a f ser uma função definida em $\mathbb{R}^2$, diferenciável e sua matriz derivada ser da forma
$
\left[
\begin{array}{cc}
m&-n\\
n&m
\end{array}
\right].
$<br>
Também lembre que se $f:U \subset \mathbb{C} \rightarrow \mathbb{C}$
é dada por $f(x,y) = (f_1(x,y),f_2(x,y))$ temos $$D_f =
\left[
\begin{array}{cc}
\dfrac{\partial f_1}{\partial x}&\dfrac{\partial f_1}{\partial y}\\
\dfrac{\partial f_2}{\partial x}&\dfrac{\partial f_2}{\partial y}
\end{array}
\right]
$$
ou seja, pelo resultado anterior teríamos as equações de Cauchy - Riemann:$$\dfrac{\partial f_1}{\partial x}= \dfrac{\partial f_2}{\partial y}$$ e $$\dfrac{\partial f_1}{\partial y}= -\dfrac{\partial f_2}{\partial x}$$
{{< /math >}}
#### Divisão do curso
{{< math >}}
O estudo de funções holomorfas vai se dividir em 2 partes:
<ul>
<li> Estudar propriedades de funções holomorfas. Estas serão muito mais fortes
e mais impressionanetes que aquelas de funções diferenciáveis de $\mathbb{R}^2$
em $\mathbb{R}^2$.</li>
<li> Aplicar estes resultados para algumas funções particulares.Dentre essas funções esta a função $\Gamma (s)$ e a função $\zeta(s)$.
<ul>
<li> A função $\Gamma$ (Generalização do fatorial)</li>
$$\Gamma(s) = (n-1)!, \forall n \in \mathbb{N}$$
$\Gamma$ será holomorfa em quase todo ponto de $\mathbb{C}$.
<li>A função $\zeta$ de Riemann.
$$\zeta (n) = \sum _ {n \geqslant 1}\dfrac{1}{n^s},\forall s \in \mathbb{C},\mathbb{R}(s)>1.$$ $\zeta$ está conectado com a disdribuição dos números primos...<br>
Além disso $\zeta$ será holomorfa em quase todo ponto de $\mathbb{C}$.</li>
</ul>
</ul>
Dentre os resultados a serem demonstrados estão...
<ul>
<li> <strong>Integral de contorno.</strong> Se $f$ é holomorfa em um aberto $U$ e $\gamma$ é um contornofechado totalmente contido em $U$ então $$\int_{\gamma}f(z)dz=0.$$</li>
<li> <strong>Regularidade.</strong> Se $f$ é holomorfa em $U \subset \mathbb{C}$ um aberto, $f$ é infinitamente derivável em $U$.</li>
<li> <strong>Continuação analítica.</strong> Se $f$ e $g$ são holomorfas,e em $U \subset \mathbb{C}$ aberto e $f=g$ em um disco $B_{\delta}(z_0)=\{z \in \mathbb{C},|z-z_0|<\delta\}$ para algum $\delta$ e algum $z_0$, então $f=g$ em $U$.</li>
</ul>
{{< /math >}}
### Preliminares sobre números complexos.
#### Os número complexos.
{{< math >}}
$$z= x+iy , x,y \in \mathbb{R}$$
$$x = \operatorname{Re}(z) , y = \operatorname{Im}(z)$$
$$\mathbb{C} \leftrightarrow \mathbb{R}^2$$

<ul>
<li> Quando $y=0 \Rightarrow z = x $, $z$ é um n'úmero real. Logo, o eixo $x(y=0)$ será chamado de eixo real.$\mathbb{R} \leftrightarrow$ eixo $x$. </li>
<li> Quando $x=0 \Rightarrow z = iy, y \in \mathbb{R}$.Dizemos que z é totalmente imaginário, chamamos o eixo y de eixo imaginário.</li>
</ul>

<h4> Regras de adição e multiplicação. </h4>

Sejam $z_1 = x_1+iy_1$, $z_2 = x_2+iy_2$ $\in \mathbb{C}$, então
<ul>
<li> $z_1+z_2 = (x_1+x_2)+i(y_1+y_2)$</li>
<li> $z_1\cdot z_2 = (x_1x_2-y_1y_2)+i(x_1y_2+x_2y_1)$</li>
</ul>
Em particular $i^2=-1$. É fácil mostrar que vale: comutatividade,
associatividade e distributividade.

Note que a soma nos complexos é análoga a soma dos vetores em $\mathbb{R}$, entretanto o produto não é dado de forma tão simples, o produto entre complexos está associado a rotomotetia , ou seja, uma rotação seguida de rotação. Exemplo:
$$i(x+iy) = -y+ix$$
$$\langle (x,y), (-y,x)\rangle = 0$$
{{< /math >}}
#### Distância e Conjugado
{{< math >}}
Seja $z = x+iy, x,y \in \mathbb{R}$, definimos $|z| = \sqrt{x^2+y^2}$, vale
então a desigualdade triangular, $|z+w| \leqslant |z|+|w|$, cuja demonstração
virá em outro momento. Outras relações um pouco mais imediatas são que $|x|
\leqslant |z|$ e $|y| \leqslant |z|$.<br>

Será interessante tambéma a definicão do conjulgado de $z = x+iy$, dado por $\overline{z} = x-iy$.Note que a representação no $\mathbb{R}$, $\overline{z}$ é a reflexão de $z$ em relação ao eixo real. Essa definicão é conveniente para escrevermos:
<ul>
<li> $z+\overline{z} = 2x \Rightarrow x = \dfrac{z+\overline{z}}{2}$</li>
<li> $z-\overline{z} = 2y \Rightarrow y = \dfrac{z-\overline{z}}{2}$</li>
<li> $z.\overline{z} = |z|^2$</li>
</ul>
<h4> Forma polar</h4>
$$(x,y) = (rcos(\theta),rsen(\theta))$$
Todo número complexo se escreve como $z = rcos\theta + ir sen\theta = r(cos\theta + i sen \theta )=:r cis \theta$. Ou seja, por enquanto $e^x$ é a função exponencial do calculo quando $x \in \mathbb{R}$ e será da forma $cis\theta$ quando $x$ for da forma $i\theta$ com $\theta \in \mathbb{R}$. Mais pra frente definiremos $e^z ,\forall z \in \mathbb{C}$ de modo a contemplar as duas definições acima. <br>
Para justificar um pouco a notação, vale a pena verificar as seguintes propriedades

<ol>
<li> $e^{i\theta}.e^{i\beta} = e^{i(\theta+\beta)}$,</li>
<li> $(e^{i\theta})^m = e^{im\theta},m \in \mathbb{Z}$.</li>
</ol>
As demonstrações ficam como exercício para o leitor.<br>
De todo modo, se $z = r.e^{i\theta}$ e $w = s .e^{i\beta}$,$$zw = rse^{i(\theta+\beta)}$$
<h4> Sequências</h4>
<ul>
<li>Sequências

Seja $\{z_n\}_{n\in \mathbb{N}}$ uma sequência de números complexos e $w \in \mathbb{C}$.
Dizemos que $z_n$ converge para $w$ e escrevemos
$\lim_{n \rightarrow \infty} = w$ se $\lim_{n \rightarrow \infty}|z_n-w| = 0.$<br>

Esta noção é a mesma noção de convergência de vetores em $\mathbb{R}^2$. Em particular $\lim_{n \rightarrow \infty} = w$ se, e somente se,
$$
\begin{cases}
  \lim_{n \rightarrow \infty}\operatorname{R}(z_n) = \operatorname{Re}(w)\\
  \lim_{n \rightarrow \infty}\operatorname{Im}(z_n) = \operatorname{Im}(w).
\end{cases}
$$
Demonstração fica como exercício para o leitor.</li>
<li> Sequências de Cauchy <br>
Uma sequência $\{z_n\}_{n \in \mathbb{N}}$ é dita de Cauchy se para todo $\varepsilon>0$,
existe $N \in \mathbb{N}$ tal que se $m,n \geqslant N$ então $|z_n-z_m|< \varepsilon.$</li>
</ul>
Pela desigualdade triângular, toda sequência convergente é de Cauchy. Ademais, lembre que $\mathbb{R}$ é completo, isto é, toda sequência de Cauchy de números reais possui limite real.Logo temos o teorema:

<br><br>
<strong>Teorema:</strong> $\mathbb{C}$ é completo.
<br><br>

PV:Seja $\{z_n\}_{n \in \mathbb{N}}$ uma sequência de Cauchy, então as partes reais e imaginárias de $z_n$ são de Cauchy e devido a completude de $\mathbb{R}$, essas sequências convergem pra $a$ e $b$, respectivamente. Logo, temos que $\lim_{n \rightarrow \infty}z_n = a+ib$, por tanto $\{z_n\}$ converge.

<h4> Conjuntos de $\mathbb{C}$.</h4>
<br><br>
<strong>Definição (Disco Aberto):</strong>
Seja $z_0 \in \mathbb{C},\delta >0$, definimos $$D_{\delta}(z_0) = \{z\in \mathbb{C}:|z-z_0|<\delta \}$$ como disco aberto de centro $z_0$ e raio $\delta.$
<br><br>

<strong>Definição (Disco Fechado):</strong>
Seja $z_0 \in \mathbb{C},\delta >0$, definimos $$\overline{D_{\delta}}(z_0) = \{z\in \mathbb{C}:|z-z_0|\leqslant \delta \}$$ como disco fechado de centro $z_0$ e raio $\delta.$
<br><br>

<strong>Definição (Círculo):</strong> $$C_{\delta}(z_0) = \{z \in \mathbb{C}; |z-z_0|= \delta\}$$ é o círculo de centro $z_0$ e raio $\delta$.
<br><br>

Notação especial: $$\mathbb{D} = D_1(0) = \{ z \in \mathbb{C} ; |z|<1\}.$$

Seja $\Omega \subset \mathbb{C}$ um conjunto, o interior de $\Omega$, denotado por
$\Omega^\circ$ ou $\operatorname{int}(\Omega)$
 é o conjunto
 $$\{z \in \Omega; \text{ existe } \delta = \delta(z) : D_{\delta}(z) \subset \Omega \}.$$


<br><br>
<strong>Definição (Conjunto Aberto):</strong>
$\Omega$ é aberto se $\Omega = \operatorname{int}(\Omega)$
<br><br>

<strong>Definição (Conjunto Fechado):</strong>
$\Omega$ é fechado se $\Omega^c$ é aberto.
<br><br>

<strong>Definição:</strong>
Seja $\Omega \subset \mathbb{C}$ um conjunto e $z \in \mathbb{C}$. Dizemos que $z$ é um ponto limite de $\Omega$ se existe uma sequência $\{z_n\}$ de pontos em $\Omega$ tal que $\lim_{n \rightarrow \infty}z_n=z.$
<br><br>

{{< /math >}}
