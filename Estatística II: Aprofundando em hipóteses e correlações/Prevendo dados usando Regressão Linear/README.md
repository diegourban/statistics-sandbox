# Prevendo dados usando Regressão Linear

Na aula passada vimos Correlação, ou seja, quando uma variável influencia a outra, elas têm alguma relação. Nesta aula veremos como prever valores utilizando a correlação como ferramenta.

Imagine que queremos saber o valor de um apartamento, sabendo de antemão que quanto maior ele for, mais caro ele é, segundo o gráfico abaixo:

![est2_5_1](./est2_5_1.png)


Um apartamento de 63 metros quadrados, qual será o valor dele seguindo a proporção mostrada no gráfico?

Nós traçamos aquela melhor reta pelos pontos já obtidos e calculamos sua função f(x). Sabendo essa função, basta calcularmos f(63) para prever o valor do apartamento, esse será o melhor chute.

![est2_5_2](./est2_5_2.png)


Chamamos isso de Regressão Linear, que tem esse nome pois toda função que acharemos será linear, ou seja, de primeiro grau:

f(x) = ax + b

Onde: b é uma constante, o coeficiente linear da reta a é o coeficiente angular da reta
