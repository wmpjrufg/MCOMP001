---
parent: Métodos numéricos
title: Integração numérica
layout: home
nav_order: 1
has_children: false
tas_toc: false
---

<!--Don't delete this script-->
<script src = "https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script id = "MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
<!--Don't delete this script-->

# A INTEGRAÇÃO NUMÉRICA


A integração numérica consiste na aplicação de métodos numéricos para determinação de integrais definidas.
Este método é utilizado por diversas áreas do conhecimento para resolução de problemas que envolvam o cálculo de uma integral, como por exemplo em elementos finitos na etapa do cálculo da matriz de rigidez.


Em suma determinaremos um número I(f) que corresponde à uma integral de uma função f(x) entre os limites a e b.


Os métodos mais conhecidos de integração numérica consistem na divisão do domínio [a, b] em retângulos como mostrado na Figura que apresenta o método do ponto central composto.

Figura 1 – Integração numérica empregando o método do ponto central [1].

![image](https://github.com/user-attachments/assets/674c54ee-6546-480b-a293-18263043e172)

# QUADRATURA DE GAUSS


A quadratura de Gauss é um dos métodos mais empregados para solução numérica de integrais. Tal método consiste em uma soma ponderada. Portanto a sua forma geral é dada como:

$$
\begin{aligned}
&\int_a^b f(x) d x \approx \sum_{i=1}^n C_i . f\left(x_i\right)\\
\end{aligned}
$$ 

Onde C_i representa o vetor de pesos e x_i os pontos de Gauss no intervalo [a, b]. Portanto na forma estendida temos:

$$
\begin{aligned}
&\int_a^b f(x) d x \approx C_1 \cdot f\left(x_1\right)+C_2 \cdot f\left(x_2\right)+\ldots+C_3 \cdot f\left(x_3\right)\\
\end{aligned}
$$ 

O conjunto de pesos C_i é dado por meio de tabelas encontradas em diversas fontes. Estes pesos são determinados fazendo com que a equação (1) seja exata quando f(x) = 1,x,x^2,x^3,etc e com intervalo de [-1, 1]. Portanto ao aplicar o método da Quadratura de Gauss é necessário transformar o domínio da integração. Para isso aplicaremos a equação (3):


$$
\begin{aligned}
&\int_a^b f(x) d x \approx \int_{-1}^1 f\left(\frac{(b-a) t+a+b}{2}\right) \frac{(b-a)}{2} d t
\end{aligned}
$$ 

Tabela 1 - Tabela dos pesos e pontos de Gauss [1]
                  
  ![image](https://github.com/user-attachments/assets/a2ade9b9-3a69-4ba2-a24c-f4afc4db60bd)

Vamos aplicar essa transformação de domínio na integral 

$$
\begin{aligned}
& \iint_0^3 e^{-x^2} d x \\
\end{aligned}
 $$ 



$$
\begin{aligned}
& x=\frac{1}{2}(t \cdot(b-a)+a+b)=\frac{1}{2}(t \cdot(3-0)+0+3)=\frac{3}{2}(t+1) \\
& d x=\frac{1}{2}(b-a) d t=\frac{1}{2}(3-0) d t=\frac{3}{2} d t \\
& \int_0^3 e^{-x^2} d x=\int_{-1}^1 \frac{3}{2} e^{-\left[\frac{3}{2}(t+1)\right]^2} d t
\end{aligned}
 $$ 


 Exemplo 1.1: Dada as funções f(x) apresentadas em a e b determinar o valor da integral nos intervalos informados.



 
$$
f(x) = e^{-x^2}
$$

 [1,1.5]   a)


f(x)=1/x [3,3.6] b)

Resolução do exemplo 1:


$$
\begin{aligned}
& x=12(t \cdot(b-a)+a+b)=12(t \cdot(1,5-1)+1,5+1)=12 x=\frac{1}{2}(t \cdot(b-a)+a+b)=\frac{1}{2}(0,50 \cdot t+2,50)= \\
& \frac{1}{4} \cdot t+\frac{5}{4}=\frac{1}{4}(t+5) \\
& d x=\frac{1}{2}(b-a) d t=\frac{1}{2}(1,5-1) d t=\frac{1}{4} d t \\
\end{aligned}
$$

Ponto 1 de Gauss (t_i = -0,57735027, w_i =1) 

$$
\begin{aligned}
& \frac{1}{4} \cdot e^{-t_1{ }^2}=\frac{1}{4} \cdot e^{-\left(\frac{1}{4}(-0,57735027+5)\right)^2}=\frac{1}{4} \cdot e^{-(1,1057)^2} \\
& \frac{1}{4} \cdot e^{-t_1{ }^2}=\frac{1}{4} \cdot e^{-\left(\frac{1}{4}(+0,57735027+5)\right)^2}=\frac{1}{4} \cdot e^{-(1,3943)^2}
\end{aligned}
$$
