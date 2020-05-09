Praticando: Regressão Linear
Na aula passada aprendemos sobre o conceito de Regressão Linear. VAmos agora aplicá-lo no R.

Primeiro vamos criar duas variáveis quaisquer:
```
> x1 <- c(1, 2, 3)
> x2 <- c(2, 4, 6)
```

Para aplicarmos a Regressão linear utilizamos o comando "lm(formula = x2 ~ x1 )". Estamos buscando o modelo linear (lm) com uma fórmula onde x2 depende de x1 (x2 ~ x1):
```
> lm(formula = x2 ~ x1)

Call:
lm(formula = x2 ~ x1)

Coefficients:
(Intercept)           x1
          0            2
```

A constante é zero e o multiplicador de x1 é 2, como podemos ver na última linha. Logo a função f é:

f(x) = 2x + 0

Vamos criar uma outra lista x3 e ver sua dependência com x1:
```
> x3 <- c(3, 5, 7)
> lm(formula = x3 ~ x1)

Call:
lm(formula = x3 ~ x1)

Coefficients:
(Intercept)           x1
          1            2
```

Aqui a função f fica:

f(x) = 2x + 1
