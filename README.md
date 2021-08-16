# Repositório de Comandos em Bash

## Tipos de Shell

### Bourne Shell
```
Bourne Shell é o shell padrão para Unix, ou seja, a matriz dos outros shells. É
representado por "sh". Foi desenvolvido por Stephen Bourne, por isso Bourne Shell.
```
### Korn Shell
```
Korn Shell este shell é o Bourne Shell evoluído, portando todos os comandos que
funcionavam no Bourne Shell funcionarão neste com a vantagem de ter mais opções. É
representado por "ksh".
```
### C Shell
```
C Shell é o shell mais utilizado em BSD, e possui uma sintaxe muito parecida com a
linguagem C. Este tipo de shell já se distancia mais do Bourne Shell, portanto quem
programa para ele terá problemas quanto a portabilidade em outros tipos. É
representado por "csh".
```
### Bourne Again Shell
```
é o shell desenvolvido para o projeto GNU usado pelo GNU/Linux,
é muito usado pois o sistema que o porta evolui e é adotado rapidamente. Possui uma
boa portabilidade, pois possui características do Korn Shell e C Shell. É representado
por "bash". 
```
## Verificando o tipo de shell
```
Para verificar qual SHELL estamos usando, basta digitar o comando abaixo, ele irá imprimir
na tela o caminho do shell bash “/bin/bash”: $ echo $SHELL
```

# Comandos

## Echo
```
O comando serve para imprimir informações na tela. Em conjunto com o símbolo de
redirecionamento de saída >>, estudado mais à frente, também é utilizado para concatenar
informações para dentro de um arquivo. 