
# 3.7 Registradores

#### Próximo: [3.8 xxx](./xxx.md)  
#### Anterior: [3.6 Memória Cache](./cache.md)  

---  

Os Registradores são locais **muito especiais** de memória construidos com flip-flops. Não são parte da memória principal; eles são implementados no processador (on-chip). Vários membros da família 80x86 possuem diferentes tamanhos de registradores. No caso dos 886, 8286, 8486 e 8686 (apenas x86 daqui em diante) possuem exatamente 4 registradores, todos de 16 bits. **Todas as operações aritméticas e de localização ocorrem nos registradores da CPU.**  

Devido ao fato do processador ter tão poucos registradores, damos a cada registrador seu próprio nome e utilizamos eles ao invés de seu endereço. Os nomes são:  
* **AX** - O registrador _acumulador_  
* **BX** - O registrador _base_  
* **CX** - O registrador _contador_ de dados  
* **DX** - O registrador de _dados_  

Além dos registradores citados, que são visíveis ao programador, os x86 também possuem um ponteiro de instrução que contém o endereço da próxima instrução a ser executada. Também existe um registrador _flag_ que segura o resultado de uma comparação. A flag grava se um valor é menor que, igual ou maior que outro valor.  

Como os registradores existem on-chip e são manipulados especialmente pela CPU, eles são muito mais rápidos que a memória. Acessar o dado em um registrador geralmente leva zero ciclos de clock. Sendo assim, você deve tentar manter as variáveis nos registradores, mas eles continuam sendo lugares excelentes para armazenar dados temporários.  

## A Unidade de Controle e o Conjunto de Instruções  
Uma boa pergunta seria "Como exatamente uma CPU realiza tarefas programadas?" Isso acontece dando-se a CPU um conjunto fixo de comandos, ou instruções. Tenha em mente que os designers de CPU criam estes processadores utilizando portas lógicas para executar estas instruções. Para manter o número de portas lógicas para um conjunto pequeno, os designers devem  restringir o número e complexidade dos comandos que a CPU reconhece.  

Os programas da época anterior as máquinas de Von Neumann eram trabalhados através de circuitos, ou seja, as conexões dos computadores que determinaval qual tipo de problema ele poderia resolver. Caso necessário, deveria se alterar o circuito para alterar a programação. O próximo avanço nessa linha foram os sistemas _programáveis_. Estes sistemas permitiam que a máquina fosse pudesse ter seus circuitos facilmente alterados, utilizando uma sequência de sockets e cabos. Um programa de computador consistia em um conjunto de linhas com buracos (sockets) cada um representando uma operação durante a execução do programa. O programador podia selecionar uma de várias instruções