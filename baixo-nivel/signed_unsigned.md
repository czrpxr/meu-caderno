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

Utilizando este padrão para definir números negativos e positivos, podemos facilmente realizar conversões entre eles. Para explicar melhor como ficariam os números, vou utilizar um número representado por 1 nibble (4 bits) e vou numerar suas 16 variações:  

|Binário|Decimal
|:---:|:---:|
|0000|0
|0001|1
|0010|2
|0011|3
|0100|4
|0101|5
|0110|6
|0111|7
|1000|8
|1001|9
|1010|10
|1011|11
|1100|12
|1101|13
|1110|14
|1111|15

Estas são as representações binárias quando os números não possuem sinal. Quando divididos em positivos e negativos, temos então de as variações de 0-7 para representar os números positivos e de 8-15 para os números negativos. Teremos então:  

|Binário|Decimal
|:---:|:---:|
|0000|0
|0001|1
|0010|2
|0011|3
|0100|4
|0101|5
|0110|6
|0111|7
|1000|8
|1001|-7
|1010|-6
|1011|-5
|1100|-4
|1101|-3
|1110|-2
|1111|-1

Perceba que os números negativos possuem **sentido contrário** aos positivos.  
Podemos perceber um padrão então para converter os números de positivos para negativos e vice-versa?  

Para este procedimento, pegamos o número binário, realizamos uma operação NOT (invertendo todos os bits) e adicionamos 1.

Exemplo com o número 3:

|Descrição|Resultado da operação
|:---:|:---:|
|Número atual|0011
|Invertendo os bits (NOT)|1100
|Adicionando 1|1101

Exemplo com o número 2:

|Descrição|Resultado da operação
|:---:|:---:|
|Número atual|0010
|Invertendo os bits (NOT)|1101
|Adicionando 1|1110

Você pode conferir os resultados na tabela apresentada anteriormente.  
Além disso, pode verificar que fazendo o caminho inverso, o resultado também será o esperado.  


## Mas por que utilizar esse sistema?  
Você deve estar se perguntando "mas não podemos só utilizar o bit de alta ordem para sinalizar o sinal e seguir numerando na sequencia? Por exemplo 0001 ser o 1 e o 1001 ser -1?  
A resposta é que o método complementar utilizado acima facilita as operações matemáticas para o hardware. Explicando melhor: temos um sistema que opera com 1 byte (8 bits) e queremos realizar a operação 1 + (-1) que obviamente resultará zero, como acontecerá essa operação?  

|Soma|
|---:|
|0000 0001  (1)|
|1111 1111 (-1)|
|**1** 0000 0000|

Como pode-se ver, ao realizar esta soma temos um bit sobrando, porém em nosso sistema estamos restritos a números representados por 1 byte, ou seja, este bit será ignorado e o resultado da operação será 0000 0000 (resultado esperado).  

Lembrando que em desenvolvimentos futuros, deve-se prestar atenção ao tipo de dado que se quer representar, pois um número binário poderá representar um número não assinalado (natural), um número sinalado (inteiro) ou um caractere.