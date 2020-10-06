<link rel="stylesheet" href="css/style.css">

# 1.1 Bit, Nibble, Byte, Word



#### Anterior: [1.Binários e Hexadecimais](./binarios.md)

---

## Bit:  
A menor unidade binária que temos é o bit. Ele representa apenas um dígito, podendo ser 0 ou 1. Pensando em lógica de programação, estes dois estados podem representar uma infinidade de situações: ligado/desligado, verdadeiro/falso, alto/baixo, etc.  
  
## Nibble:  
O Nibble é um conjunto de quatro bits. O Nibble é importante porque como pudemos ver na tabela de conversão entre binários e hexadecimais, com 4 bits podemos representar todos os dígitos hexadecimais.  
  
## Byte:  
Um byte é composto de 8 bits. É de longe a estrutura binária mais conhecida e geralmente o menor item que pode ser acessado individualmente (quando falamos de microprocessadores e microcontroladores, por exemplo). Até podemos manipular bits individualmente, porém devemos utilizar operações que "mascaram" os bits que não queremos alterar em um byte.  
Outra coisa que podemos observar é que um Byte é composto de dois Nibbles.