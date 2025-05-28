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

Empregando dois termos e um resíduo é possível chegar a:

$$ f^{\prime}\left(x_i\right)=\frac{f\left(x_{i+1}\right)-f\left(x_i\right)}{h}-f^{\prime \prime}\left(x_i\right) \frac{h}{2!}  (5) $$

Onde $$f^{\prime \prime}\left(x_i\right) \frac{h}{2!}$$ É dado como o erro de truncamento da série.


Vamos empregar esta aproximação para cálculo da derivada de f(x)=ln x no ponto x = 1,80.
Para isso vamos considerar o parâmetro h = 0,10, 0,01 e 0,001.



Aplicando a equação (5) chegamos em:


$$
f^{\prime}(1,80) \cong \frac{\ln (1,80+0,10)-\ln (1,80)}{0,10}=0,540672 
$$

$$
f^{\prime}(1,80) \cong \frac{\ln (1,80+0,010)-\ln (1,80)}{0,010}=0,554018 
$$

$$
 f^{\prime}(1,80) \cong \frac{\ln (1,80+0,0010)-\ln (1,80)}{0,0010}=0,555401
$$ 

Exemplo 1.1: Dada as funções f(x) apresentadas em a  e  b determinar o valor da derivada numérica nos pontos informados.


f(x)= $$\( x^3 \)$$ ,x = 3  a) 


f(x)=sen x,x=π⁄3  b)



Solução a)


$$
f(x) = x^3 \Rightarrow f(3) = 27
$$

Com h=0,1:

$$
f(3,1)=(3,1)^3=29,791 
f^{\prime}(3) \approx \frac{29,791-27}{0,1}=27,91
$$

Com h=0,01:


$$
f(3,01)=(3,01)^3=27,270901 
f^{\prime}(3) \approx \frac{27,270901-27}{0,01}=27,0901
$$

Com h=0,001:

$$
f(3,001)=(3,001)^3=27,027009 
f^{\prime}(3) \approx \frac{27,027009-27}{0,001}=27,009
$$


Solução b)

$$
\[
f(x)=sen(x) \Rightarrow f\left(\frac{\pi}{3}\right)=sen \left(\frac{\pi}{3}\right)=\frac{\sqrt{3}}{2} \approx 0,8660
\]
$$

Com h=0,1:

$$
x=\frac{\pi}{3}+0,1 \approx 1,1472, \quad sen (1,1472) \approx 0,9096 
$$


$$
f^{\prime} \approx \frac{0,9096-0,8660}{0,1}=0,436
$$

Com h=0,01:

$$
x = 1{,}0572, \quad sen(1{,}0572) \approx 0{,}8699 \\
f'(x) \approx \frac{0{,}8699 - 0{,}8660}{0{,}01} = 0{,}39
$$

Com h=0,001:


$$
x = 1{,}0482, \quad sen(1{,}0482) \approx 0{,}8662 \\
f'(x) \approx \frac{0{,}8662 - 0{,}8660}{0{,}001} = 0{,}2
$$





REFERÊNCIAS

[1]	Gilat A, Suramanian V. Métodos numéricos para engenheiros e cientistas: uma introdução com aplicações usando o MATLAB. 2008.



