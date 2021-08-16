# 1. Repositório de Comandos em Bash

## 1.1 Tipos de Shell

### 1.1.1 Bourne Shell

Bourne Shell é o shell padrão para Unix, ou seja, a matriz dos outros shells. É
representado por "sh". Foi desenvolvido por Stephen Bourne, por isso Bourne Shell.

### 1.1.2 Korn Shell

Korn Shell este shell é o Bourne Shell evoluído, portando todos os comandos que
funcionavam no Bourne Shell funcionarão neste com a vantagem de ter mais opções. É
representado por "ksh".

### 1.1.3 C Shell

C Shell é o shell mais utilizado em BSD, e possui uma sintaxe muito parecida com a
linguagem C. Este tipo de shell já se distancia mais do Bourne Shell, portanto quem
programa para ele terá problemas quanto a portabilidade em outros tipos. É
representado por "csh".

### 1.1.4 Bourne Again Shell

é o shell desenvolvido para o projeto GNU usado pelo GNU/Linux,
é muito usado pois o sistema que o porta evolui e é adotado rapidamente. Possui uma
boa portabilidade, pois possui características do Korn Shell e C Shell. É representado
por "bash". 

## 1.2 erificando o tipo de shell

Para verificar qual SHELL estamos usando, basta digitar o comando abaixo, ele irá imprimir
na tela o caminho do shell bash “/bin/bash”.

Exemplo:
```
$ echo $SHELL
```


# 2. Comandos

## 2.1 Echo

O comando serve para imprimir informações na tela. Em conjunto com o símbolo de
redirecionamento de saída >>, estudado mais à frente, também é utilizado para concatenar
informações para dentro de um arquivo. 

Exemplo:
```
$ echo “Este é o curso de lpi-1” >> /home/lpi1/Documents/teste.txt
```
No exemplo acima, introduzimos a frase no arquivo teste.txt, mesmo o arquivo não
existindo no diretório, ele é criado automaticamente ao executarmos o comando.

## 2.2 Type

No Linux existem comandos que são internos do shell que já são embutidos no
programa SHELL e também comandos que são externos ou migrados de outras aplicações que
estão em nosso sistema. Para sabermos se um comando é de origem SHELL para usarmos o
comando `type`.

Exemplo: 
```
$ type echo
```
Após esse comando ele nos retornará uma mensagem nos dizendo se é ou não um
comando interno do shell, ou seja, já está em sua compilação de origem.