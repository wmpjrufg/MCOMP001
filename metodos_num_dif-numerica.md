---
parent: Métodos numéricos
title: Diferenciação numérica
layout: home
nav_order: 1
has_children: false
tas_toc: false
---

<!--Don't delete this script-->
<script src = "https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id = "MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<!--Don't delete this script-->

# A DIFERENCIAÇÃO NUMÉRICA 

Nesta seção falaremos sobre um modelo de diferenciação numérica. Onde nosso objetivo é dado uma função $y = f(x)$ precisamos determinar a derivada no ponto $x=x_k$. Ou seja, vamos construir uma aproximação da derivada da função na vizinhança de $x_k$.

A derivada é uma ferramenta importante e com grande frequência aparece na solução de problemas em ciências exatas e tecnológicas. Muitos destes modelos são expressos em termos de taxa. São exemplos destes tipos de problemas: (a) condução de calor, (b) corrente em um capacitor, (c) energia de um sistema mecânico [1].

# DIFERENÇAS FINITAS

A aproximação de uma derivada pode ser dada por:

$$
\left.\frac{d f(x)}{d x}\right|_{x=a}=f^{\prime}(a)=\lim _{x \rightarrow a} \frac{f(x)-f(a)}{x-a}              (1)
$$


À medida que x se aproxima de a a precisão da derivação aumenta. Para então escrever modelos de aproximação vamos empregar a expansão da série de Taylor.

$$
f(x)=\sum_{n=0}^{\infty} a_n \cdot(x-a)^n              (2) 
$$ 

$$
a_n=f^{(n)}(a) / n!                                    (3)
$$

Portanto para obter a aproximação de f^' (x_(i+1)) como o polinômio de Taylor. Para isso considere que $$h=x_{i+1}-x_i$$

$$ f\left(x_{i+1}\right) \approx f\left(x_i\right)+f^{\prime}\left(x_i\right) \frac{h^1}{1!}+f^{\prime \prime}\left(x_i\right) \frac{h^2}{2!}+f^{\prime \prime \prime}\left(x_i\right) \frac{h^3}{3!}+f^{\prime \prime \prime \prime}\left(x_i\right) \frac{h^4}{4!}+\ldots                         (4) $$
