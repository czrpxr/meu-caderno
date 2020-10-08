<link rel="stylesheet" href="css/style.css">

# 1.3 Sobre os Números Positivos e Negativos



#### Anterior: [1.2 Operações Lógicas](./operacoes_logicas.md)
#### Próximo: []()

---

O conceitos de números binários foi introduzido apenas se tratando de números positivos. Por exemplo, para o número 1 decimal utilizamos 0001, para o 2 o 0010 e assim por diante. Mas e quando temos que representar números tanto positivos quanto negativos? O que fazemos?  

Primeiramente temos que ter em mente que será um número finito e fixo de valores. Utilizando 1 byte como exemplo, neste caso podemos representar apenas 256 valores no total (2 elevado à 8). Ou seja, vamos ter que utilizar  metade desses valores para representar números negativos *0 - 127* e *128-255*. Mas como fazer isso?  
Uma regra muito comum é que o bit de alta ordem 