# shell-script
Comandos e estruturas do shell script

Comentário

```shell
# Meu comentário
```

Criaçāo de variáveis

```shell
x=0
```

Exibir o valor da variáveis no terminal

```shell
echo $x
```

Operação de Matemáticas

```shell
# Adição
x=$(($x+1)) 
# Subtração
x=$(($x-1)) 
# Divisão
x=$(($x/2)) 
# Multiplicação
x=$(($x*1)) 
```

Operação entre duas variáveis

```shell
z=$(($x*$y))
```

Imprimir um texto com o valor de uma variável

```shell
z=10
echo "Valor de Z=$z"
```

Entrada de dados. ```z``` é a variavel que será armazenada o conteúdo digitado pelo usuário.

```shell
read z
```
