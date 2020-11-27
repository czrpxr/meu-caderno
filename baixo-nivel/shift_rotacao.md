<link rel="stylesheet" href="css/style.css">

# 1.4 Shift (deslocamento) e Rotação



#### Anterior: [1.3 Sobre os Números Positivos e Negativos](./signed_unsigned.md)
#### Próximo: [1.5]()

---  

O shift e a rotação são operações muito comuns e úteis na operação de bits como veremos a seguir.


**SHIFT**  
<br />
A operação de shift consiste em mover os bits para a esquerda ou direita, conforme vemos abaixo  


![](./imgs/left_shift.png)  
- Shift para Esquerda -  


No shift para esquerda os bits são movimentados para o lado esquerdo. Vamos tomar como exemplo a movimentação de cada bit em uma posição. Após o deslocamento dos bits, o bit que estava presente na posição 7 é automaticamente descartado e a posição 0 será reposta com o valor zero. Quando realizamos esta operação, estamos automaticamente multiplicando este número  binário por 2 (sua base). Se movermos novamente a multiplicação total será 2 x 2 = 4.  
Ou seja, ao deslocar bits para esquerda **n** vezes, significa que estamos multiplicando aquele número por *2 elevado a n*.  


![](./imgs/right_shift.png)  
- Shift para Direita -  

No caso do shift para a direita acontece exatamente o que imaginamos: o inverso da operação  para esquerda. Ou seja, ao invés de termos uma multiplicação teremos uma divisão por *2 elevado a n* posições em que os bits foram movidos.
