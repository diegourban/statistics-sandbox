Praticando: Pearson e Spearman
Vamos aplicar no R o que aprendemos sobre Correlação.

Primeiramente vamos ler os números do arquivo CSV:
```
> nums <- read.csv(files="[caminho do arquivo]/numeros.csv")
```

Para vermos os números:
```
> nums
  X1 X2
1  2  4
2  3  6
3  4  8
```

Agora, para calcularmos a correlação basta usar o comando "cor ( )":
```
> cor(nums$X1, nums$X2)
[1] 1
```

Como vimos a correlação é igual a 1, muito forte e positiva.

Um exemplo negativo:
```
> a <- c(2, 3, 4)
> b <- c(8, 6, 4)
> cor (a, b)
[1] -1
```

Esta correlação também é muito forte, porém negativa.

Da mesma forma que o Teste de Hipótese o Teste de Correlação também recebe duas listas.

Mudança de Método
Podemos escolher o tipo de método para um teste de correlação. Como vimos existem dois: Pearson e Spearman. Veja como usá-los: 

Pearson:
```
> cor(a, b, method="pearson")
```

Spearman:
```
> cor(a, b, method="spearman")
```
