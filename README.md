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

# Desenvolvimento

Para começar o programa o usuário deve definir três parâmetros:

![image](https://user-images.githubusercontent.com/85235525/147489383-85b5ec25-f4ab-4973-874e-9ca5a60a0521.png)

* Quantidade de sucesso desejada *(P)*.
* Número de ensaios *(n)*.
* Probabilidade de sucesso *(k)*.

## Tratamento de erro
Supondo que o usuário esqueça de algum dos dados (vamos considerar que ele esquece alguma informação quando essa informação foi igual a *0*) então o programa irá avisar qual informação ele esquece e não irá rodar!<br>
Utilizei _**try**_ e _**except**_ para previnir os erros.

### Exemplo 1:

![image](https://user-images.githubusercontent.com/85235525/147494548-2a6cd569-0e28-4b1f-89a4-f1d2e47a50a8.png)

### Exemplo 2:

![image](https://user-images.githubusercontent.com/85235525/147495281-0040f031-6eae-42e6-a282-e3901394d14e.png)

## Rodando sem erros:

Quando não temos erros, podemos ver expresso o resultado do cálculo!

![image](https://user-images.githubusercontent.com/85235525/147495952-c9a056f1-082d-4cf9-a5d3-1c940eff385a.png)

![image](https://user-images.githubusercontent.com/85235525/147496028-cb515e17-fbb8-4ab9-9b83-d59b47607d75.png)

## Utilizando um exemplo prático:

Extrai um exemplo de questão de probabilidade binomial de um [caderno de questões](https://www.ime.usp.br/~salles/fatec/estatistica/material_apoio/ExerciciosResolvidosBinomial.pdf) do [Instituto de matmática e estatística da USP](https://www.ime.usp.br/) para solucionarmos e compararmos a resposta

![image](https://user-images.githubusercontent.com/85235525/147496339-89bc0428-8e2e-4fe9-8ec0-fc145e4d7127.png)

Temos que:
* _p_ é 1/4 ou 0.25
* _k_ é 3
* _n_ é 6

### Resultado obtido:
![image](https://user-images.githubusercontent.com/85235525/147496603-711bb4a3-455c-4326-badd-a173a182d11c.png)
### Resolução do professor:
![image](https://user-images.githubusercontent.com/85235525/147496627-716c756d-aeb8-4a98-b6a3-7dff0966882c.png)

Nossa reposta bateu perfeitamente com o execício proposto pelo professor.

# Projetos futuros:

Em projetos futuros pretendo incluir os eventos binomiais cumulativos.




