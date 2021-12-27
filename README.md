# Introdução:

Um dos principais ramos da estatística é o calculo da probabilidade. Para leigos o que se torna difícil é interpretar o problema e assimilar os elemenos na equação, por tanto, esse projeto tem a proposta de facilitar o cálculo de probabilidades atavés do desenvolvimento de um pequeno programa que calculará a probabilidade de eventos binomiais.

# Desenvolvimento teórico:

## Pressupostos:

* O acontecimento dos eventos devem ser aletórios;
* Os experimentos podem exprimir apenas dois possíveis resultados (sim ou não, por exemplo);
* Os eventos devem ser indepentes, o que significa que o acontecimento de um determinado evento não influencia no acontecimento ou não de outro.

## Definições matemáticas:

Temos por definição que:

<img src="https://github.com/xpcosmos/calculadora-de-probabilidades/blob/main/assets/funcao_prob.png" title="\bg_white P(k) = \binom{n}{k}p^kq^{n-k}" width = 200 />

Onde:

> _p_ = Probabilidade de determinado evento acontecer <br>
> _q_ = Probabilidade de determinado **NÃO** acontecer (1 - p) <br>
> _k_ = Quantidade de resultados desejados <br>
> _n_ = Números de ensaios realizados <br><br>

Para a resolução de um problema precisa se conhecer quantos eventos irão ocorrer. Por exemplo, caso uma pessoa decida jogar um dados, o número de eventos será determinado pela quantidade de vezes que o dado será jogado.<br><br>
Precisamos conhecer também a chance de cada evento individual ocorrer. Reutilizando o exemplo dos dados, vamos supor que desejamos descobri a chance estatística de obter o número _6_ ao jogar o dado. Considerando temos chances iguais de tirarmos qualquer um dos 6 números, teremos que as chances de tirarmos 6 é de 1 em 6, ou de 16,66%.<br><br>
A chance de determinado evento não ocorrer pode ser dado pela expressão de (1 - p), pois o evento q (em que p não ocorre) é determinado pela não ocorrência de p.<br><br>
Resgatando nosso exemplo anterior do lançamento de dados, caso joguemos o dado 3 vezes e queiramos saber qual a probabilidade de tirarmos o número _6_ 2 vezes, teremos que a quantidade de resultados desejamos é de 2.

# Tecnologias utilizadas.

Para esse projeto vamos utilizar o as funções binomiais da biblioteca [Scipy](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.binom.html). <br>
Utilizaremos também a biblioteca [IPyWidgets](https://ipywidgets.readthedocs.io/en/latest/examples/Widget%20Basics.html) que irá nos possibilitar a criação de um formulário através de _notebooks_.

# Projeto


Vamos ao que interessa, o projeto.
