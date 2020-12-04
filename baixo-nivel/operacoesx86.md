
# 3.8 Conjunto de Operações dos x86

#### Próximo: [3.9 xxx](./xxx.md)  
#### Anterior: [3.7 Registradores](./registradores.md)  

---  

A família x86 de processadores oferecem 20 classes de instruções básicas:  
* Sete delas possuem dois operandos,  
* Oito delas possuem um operando,  
* Cinco não possuem nenhum operando.  

As inmstruções são **mov (duas formas), add, sub, cmp, and, or, not, je, jne, jb, jbe, ja, jae, jmp, brk, iret, halt, get, put**.  
Abaixo temos como cada uma delas funciona:  

## MOV  

A instrução MOV são na verdade duas classes de instruções mescladas na mesma instrução. As duas formas da instrução MOV o as seguintes:  

```
mov reg, reg/memory/constant  
mov memory, reg  
```

Onde _reg_ é qualquer um dos registradores ax, bx, cx, dx; _constant_ é um valor numérico (expresso em hexadecimal) e _memory_ é um operando que especifica uma localização na memória. O campo _reg/memory/constant_ mostra que para este operando em particular podemos utilizar um registrador, uma localização na memória ou uma constante.  

## INSTRUÇÕES ARITMÉTICAS E LÓGICAS  

```
add reg, reg/memory/constant  
sub reg, reg/memory/constant  
cmp reg, reg/memory/constant  
and reg, reg/memory/constant  
or  reg, reg/memory/constant  
not reg/memory  
```

A instrução _add_ adiciona o valor do segundo operando ao primeiro (registrador) operando, deixando o resultado no primeiro operando. a instrução _sub_ subtrai o valor do segundo operando do primeiro, deixando a diferença no primeiro operando. O _cmp_ compara o primeiro operando com o segundo e salva o resultado da comparação com uma instrução de jump. As instruções de _and_ e _or_ realiza a respectiva operação bitwise nos dois operandos e armazena o resultado no primeiro operando. A instrução _not_ inverte os bits em apenas uma posição na memória ou registrador.  