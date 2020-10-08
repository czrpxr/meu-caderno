<link rel="stylesheet" href="css/style.css">

# 1.3 Sobre os Números Positivos e Negativos



#### Anterior: [1.2 Operações Lógicas](./operacoes_logicas.md)
#### Próximo: [1.4]()

---

O conceitos de números binários foi introduzido apenas tratando de números positivos. Por exemplo, para o número 1 decimal utilizamos 0001, para o 2 o 0010 e assim por diante. Mas e quando temos que representar números tanto positivos quanto negativos? O que fazemos?  

Primeiramente temos que ter em mente que será um número finito e fixo de valores. Utilizando 1 byte como exemplo, neste caso podemos representar apenas 256 valores no total (2 elevado à 8). Ou seja, vamos ter que utilizar metade desses valores para representar números negativos *0 - 127* e *128-255*. Mas como fazer isso?  
Uma regra muito comum é que o bit de de maior ordem seja um bit de sinal. Quando o número possui o bit de maior ordem é zero ele é positivo, quando 1 ele é negativo. No caso de 1 byte (8 bits) podemos representar então de -128 até -1 e de 0 até 127.

*Exemplos com 16-bits:*

|Hexadecimal|Binário|Sinal|
|:---:|:---:|:---:|
|8000|**1**000 0000 0000 0000|Negativo|
|100|**0**000 0001 0000 0000|Positivo|
|7FFF|**0**111 1111 1111 1111|Positivo|
|0FFFF|**1**111 1111 1111 1111|Negativo|
|0FFF|**0**000 1111 1111 1111|Positivo|

## Convertendo números de positivo para negativo e vice-versa  

