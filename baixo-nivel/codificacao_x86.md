
# 3.10 Encoding do x86


#### Próximo: [3.11 xxxxx](./xxxx.md)  
#### Anterior: [3.9 Modos de Endereçamento](./formas_enderecamento.md)  

---  
Ao escrever um código em assembly estamos usando operandos (mov, add, sub,...) para representar operações, porém a CPU opera sua lógica em cima de circuitos que decodificam os operandos para agir apropriadamente. Uma CPU típica utiliza um certo número de bits para definir cada um dos operandos. Alguns sistemas (por exemplo, CISC - Complex Instruction Set Computers) codificam estes campos de um modo muito complexo, gerando instruções muito compactas. Outros sistemas (por exemplo, RISC - Reduced Instruction Set Computers) codificam os operandos de uma maneira mais simples, mesmo que isso significa desperdiçar alguns bits no operando ou limitando o número de operações. A família 80x86 é definitivamente CISC e possui uma das mais complexas codificações decodificações.  
Em uma instrução típica da família x86 as instruções básicas são compostas por 1 ou 3 bytes. O operando é m byte individual que possui três campos: O primeiro, os primeiros 3 bits de alta ordem, definem a instrução. Com isso temos 8 combinações