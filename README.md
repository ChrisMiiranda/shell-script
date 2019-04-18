# shell-script
Comandos e estruturas do shell script


Indica qual o interpretador a ser utilizado. Deve estar na primeira linha do arquivo. Conhecido por *Shebang*
```shell
#!/usr/bash
```

Comentário

```shell
# Meu comentário
```

Criaçāo de variáveis. Não deve conter espaços entre o nome da variável, sinal de ```=``` e o valor.

```shell
x=0
```

Exibir o valor da variáveis no terminal

```shell
echo $x
```

Operação de Aritméticas

| Operação            |    | Exemplo |
|---------------------|----|---------|
| Adição              | +  |   ```x=$(($x+1)) ```      |
| Subtração           | -  |   ```x=$(($x-1)) ```       |
| Multiplicação       | *  |   ```x=$(($x*1)) ```       |
| Divisão             | /  |    ```x=$(($x/1)) ```      |
| Módulo              | %  |    ```x=$(($x%1)) ```      |
| Exponenciação       | ** |    ```x=$(($x**1)) ```      |

Deve-se utilizar ```$``` seguidos por ```(( ))```.
Outra maneira de representar um cálculo utilizando ```$[ ]```.

```shell
x=$[ $x * 10 ] 
```

Operação entre duas variáveis

```shell
z=$(($x*$y))
z=$[ $x * $y ]
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

Recebendo parâmetros. Na hora da execução do script shell, deve-se informar os parâmetros separados por espaços.

```shell
./shell_script.sh parametro1
```

No script, se acessa ao parâmetro através do ```$```. Por exemplo, o primeiro parâmetro é ```$1```, o segundo é ```$2```, assim por diante.

```shell
#!/bin/bash
echo "Valor do parametro= $1"
```
Operadores relacionais

| Comparação Numérica |     | Exemplo |
|---------------------|-----|---------|
| é menor que         | -lt |  ``` 10 -lt $z  ```    |
| é maior que         | -gt |  ``` 10 -gt $z  ```      |
| é menor igual       | -le |  ``` 10 -le $z  ```       |
| é maior igual       | -ge |  ``` 10 -ge $z  ```       |
| é igual             | -eq |  ``` 10 -eq $z  ```       |
| é diferente         | -ne |  ``` 10 -ne $z  ```       |

| Comparação de Strings |     | Exemplo |
|-----------------------|-----|---------|
| é igual               | = |  ``` $y = "texto"  ```    |
| é diferente           | != |  ``` $y != "texto"  ```      |

| Operadores lógicos    |     | Exemplo |
|-----------------------|-----|---------|
| não lógico (NOT)       | ! |  ``` ! $y -eq 1   ```    |
| E   lógico (AND)       | -a |  ``` $y -eq 1 -a $y -le $z  ```      |
| OU   lógico  (OR)      | -o |  ``` $y -eq 1 -o $y -le $z  ```      |


Estrutura de decisão

```shell
if COMANDO then
   ...
elif COMANDO then
   ...
else
   ...
fi
```

Exemplo

```shell
if [ $x -gt 0 ] then
   echo "dentro do if"
fi
```

Estrutura de repetição

```shell
while COMANDO do
  ...
done
```

Exemplo

```shell
y=2
while [  $y -le 10  ]; do
   echo "y = $y"
   y=$[ $y + 1 ]
done
```
