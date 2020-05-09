# Praticando: Teste do Estudante e Wilcoxon

Agora que você já sabe o que é um Teste de Hipótese, está na hora de colocar isso em prática no R. Vamos utilizar o mesmo exemplo da aula passada: o remédio que abaixa a febre.

Nós temos as temperaturas dos pacientes antes e depois do remédio distribuídas em duas listas. Para isso vamos rodar um comando cuja função é gerar lista de números aleatórios, o "runif(a, b, c)", onde: - a: quantidade de elementos da lista - b: valor máximo - c: valor mínimo

Gerando as listas x1 e x2:

```
> x1 <- runif(30, 37.9, 38.8)
> x1
 [1] 38.74792 38.22167 38.56094 38.22982 38.05435 38.04450 38.44803 38.38801
 [9] 38.34245 38.68356 38.46291 38.16700 38.74269 37.93675 38.34229 38.54316
[17] 38.65470 38.54693 38.70671 38.26695 38.52493 38.61315 37.93684 38.31222
[25] 38.62993 37.90442 38.43821 38.30228 38.46592 38.18555
```

```
> x2 <- runif(30, 36.0, 38.2)
> x2
 [1] 37.33031 36.16080 36.21709 37.20106 36.12353 36.56028 36.02856 37.70127
 [9] 36.16858 36.87020 36.41650 37.70985 36.22291 36.63952 37.32194 38.17058
[17] 36.58636 36.07406 37.86259 37.59871 36.29155 36.17606 36.52225 37.52026
[25] 36.06786 38.10855 37.55266 38.17772 36.48584 37.57940
```

A nossa H0 é aquela hipótese que queremos anular, ou seja, de que o remédio não faz efeito. A Halt é que o remédio faz a diferença na temperatura do corpo da pessoa.

### Teste do Estudante
Vamos, enfim, rodar o Teste do Estudante, utilizando o comando "t.test( )":

```
> t.test(x1, x2)

        Welch Two Sample t-test

data:  x1 and x2
t = 10.3637, df = 35.542, p-value = 2.757e-12
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 1.178394 1.752133
sample estimates:
mean of x mean of y 
 38.38016  36.91490
```

Perceba que o p-value é muito pequeno, então podemos facilmente descartar nossa Hipótese Nula e aceitar a Hipótese Alternativa.

Se lermos o manual do "t-test" veremos que é possível rodá-lo como pareado, ou seja, comparar a mesma pessoa antes e depois. Outra ferramenta importante é a alternative, na qual você pode escolher se quer rodar o teste como Two Tailed ou como One-sided.

### Teste de Wilcoxon
Podemos utilizar as mesmas listas e rodar o Teste de Wilcoxon, para distribuições não Normais, com o comando "wilcoxon.test ( )":

```
> wilcox.test(x1, x2)

        Wilcoxon rank sum test

data:  x1 and x2
W = 883, p-value = 2.05e-14
alternative hypothesis: true location shift is not equal to 0
```
Aqui o p-value também deu muito pequeno. Mas lembre-se: primeiro precisamos ter certeza se a distribuição é Normal ou não.
