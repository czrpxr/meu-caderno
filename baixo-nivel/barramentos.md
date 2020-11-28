
# 3.1 Os Barramentos


#### Próximo: [3.2 A Memória](./memoria.md)  
#### Anterior: [3. O Sistema x86 e sua Arquitetura](./sistemax86.md)  

Os barramentos do sistema são utilizados para conectar vários componentes em uma máquina Von Neumann. A família 80x86 possui 3 barramentos principais: endereço, dados e controle. Um barramento é simplesmente uma conjunto de fios que transferem sinais elétricos entre os componentes de um sistema. Eles variam de processador para processador, mas todos desempenham a mesma função entre sistemas.  

Um systema 80x86 padrão utiliza níveis lógicos TTL (Transistor-Transistor Logic). Isso significa que cada fio do barramento utiliza voltagens padrões para representar 0 e 1 (No caso do TTL, 0.0 - 0.8V representam 0 e 2.4 - 5V representa 1).  

## Barramento de Dados  

É utilizado para troca de dados entre vários componentes em um sistema. O tamanho desse barramento varia e é ele quem define o "tamanho" do processador. Em um sistema típico 80x86 o barramento de  dados possui 8, 16, 32 ou 64 linhas. Possuir um barramento de dados de 8 bits não significa que o processador está limitado a dados de 8 bits, mas sim que o processador poderá acessar apenas 1 byte na memória, por ciclo. Contudo um barramento de 8 bits com um processador 8088 pode apenas transmitir metade da informação por unidade de tempo (ciclo de memória) que um processador 8086 de 16 bits.  
Sendo assim, sabemos que processadores com barramentos de 16 bits são naturalmente mais rápidos que processadores de 8 bits e que processadores de 32 bits são mais rápidos que de  16 bits.  
O tamanho do barramento de dados afeta o desempenho de um sistema mais do que o tamanho de qualquer outro barramento.