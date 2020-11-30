
# 3.2 A Memória


#### Próximo: [3.2 A Memória](./a_memoria.md)  
#### Anterior: [3 Organização de um sistema x86](./sistemax86.md)  

Um processador 80x86 endereça no máximo 2 elevado a n diferentes localizações. com _n_ sendo o número de bits do barramento de endereço. A unidade mais básica de memória é um byte. Portanto, com 20, 24 e 32 linhas de endereços, o processador 80x86 pode endereçar 1Mb, 16 Mb e 4Gb de memória respectivamente.  
O que acontece então quando o processador acessa uma palavra binária ou palavra binária dupla. Se a memória é um array de bytes, como podemos lidar com valores maiores que 8 bytes?  

Cada sistema lida com este problema de uma maneira. Na família 80x86 o problema é resolvido armazenando o  byte de baixa ordem em um endereço especificado e o byte  de alta ordem na próxima localização (sendo assim, uma palavra consome dois endereços de memória consecutivos).

![](./imgs/escrita.gif)

Podemos notar que um byte, uma palavra e uma palavra dupla podem acabar sobrescrevendo dados. Tomando como exemplo a próxima imagem,  temos uma palavra iniciando no endereço 193, um byte no endereço 194 e uma palavra dupla no endereço 192. Essas variáveis podem todas se sobrescreverem.  

![](./imgs/organizacao_memoria.gif)