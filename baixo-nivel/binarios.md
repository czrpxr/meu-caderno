<link rel="stylesheet" href="./css/style.css">

## Programação de Baixo Nível (Assembly)

O conteúdo é baseado na arquitetura intel x86 32-bits

### Conteúdo:

[Binários e Hexadecimais](#1. Binários e Hexadecimais)




---

# 1. Binários e Hexadecimais

* Sistema decimal:

No cotidiano utilizamos o sistema decimal (base dez) para representar grandezas. O número 1234 pode ser descrito das seguintes formas:

<img class="center" src="https://latex.codecogs.com/gif.latex?1000&space;&plus;&space;200&space;&plus;&space;30&space;&plus;&space;4" title="1000 + 200 + 30 + 4" />
<img class="center" src="https://latex.codecogs.com/gif.latex?1&space;*&space;10^{3}&space;&plus;&space;2&space;*&space;10^{2}&space;&plus;&space;3&space;*&space;10^{1}&space;&plus;&space;4&space;*&space;10^{0}" title="1 * 10^{3} + 2 * 10^{2} + 3 * 10^{1} + 4 * 10^{0}" />

Ou seja, cada digito representa um valor entre zero e nove multiplicado por uma potência de 10.

* Sistema binário:

Internamente os computadores representam valores em níveis de voltagem ALTA e BAIXA (geralmente 0 e 5V), ou seja, apenas dois valores. Convencionou-se então a utilização dos dois digitos utilizados no _sistema binário_ (base dois). Podemos conver qualquer número binário para o sistema decimal utilizando praticamente a mesma lógica para representação que no sistema decimal: as diferenças são que ao invés dos números de 0-9 os valores referência são 0 e 1 multiplicados por potências de 2.
Tomando como exemplo o número 1111011, temos:

<img class="center" src="https://latex.codecogs.com/gif.latex?1&space;*&space;2^{6}&space;&plus;&space;1&space;*&space;2^{5}&space;&plus;&space;1&space;*&space;2^{4}&space;&plus;&space;1&space;*&space;2^{3}&space;&plus;&space;0&space;*&space;2^{2}&space;&plus;&space;1&space;*&space;2^{1}&space;&plus;&space;1&space;*&space;2^{0}" title="1 * 2^{6} + 1 * 2^{5} + 1 * 2^{4} + 1 * 2^{3} + 0 * 2^{2} + 1 * 2^{1} + 1 * 2^{0}" />
<img class="center" src="https://latex.codecogs.com/gif.latex?=&space;64&space;&plus;&space;32&space;&plus;&space;16&space;&plus;&space;8&space;&plus;&space;0&space;&plus;&space;2&space;&plus;&space;1" title="= 64 + 32 + 16 + 8 + 0 + 2 + 1" />
<img class="center" src="https://latex.codecogs.com/gif.latex?=&space;123_{10}" title="= 123_{10}" />

(OBS: o número 10 na parte inferior do resultado mostra que ele está escrito na base 10)