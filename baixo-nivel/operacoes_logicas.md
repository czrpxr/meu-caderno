<link rel="stylesheet" href="css/style.css">

# 1.2 Operações Lógicas 



#### Anterior: [1.1 Bit, Nibble, Byte, Word](./estruturas.md)
#### Próximo: []()

---

## Operações Lógicas com Bits

As operaçõrs lógicas com Bits definidas são AND, OR, XOR e NOT. Estas operações serão exemplificadas com suas respectivas tabelas verdade considerando duas entradas e sua respectiva saída.

### AND
Na operação AND ("e") quando inseridos os valores ambos devem ser 1 para que a saída também seja 1, ou seja o primeiro **E** o segundo devem ser 1:  
  
|AND|0|1|
|:---:|:---:|:---:|
|**0**|0|0|
|**1**|0|1|

### OR
Na operação OR ("ou") quando inseridos os valores, pelo menos um deles deve ser 1 para que a saída também seja 1. Ou seja o primeiro **OU** o segundo devem ser 1:  
  
|AND|0|1|
|:---:|:---:|:---:|
|**0**|0|1|
|**1**|1|1|


### XOR
Na operação XOR ("ou exclusivo ou exclusive-or") quando inseridos os valores, pelo menos um deles deve ser 1 para que a saída também seja 1 e somente 1 deles. Ou seja o primeiro **OU** o segundo devem ser 1, porém não é incluído o caso onde os dois valores são 1:  
  
|AND|0|1|
|:---:|:---:|:---:|
|**0**|0|1|
|**1**|1|0|

### NOT
Na operação NOT ("não" ou "negação") quando um valor é inserido, a saída é o oposto da entrada, ou seja, "negando" a entrada.
  
|NOT|0|1|
|:---:|:---:|:---:|
||1|0|