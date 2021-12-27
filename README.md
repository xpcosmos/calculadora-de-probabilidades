# Introdução:

Um dos principais ramos da estatística é o calculo da probabilidade. Para leigos o que se torna difícil é interpretar o problema e assimilar os elementos na equação, por tanto, esse projeto tem a proposta de facilitar o cálculo de probabilidades através do desenvolvimento de um pequeno programa que calculará a probabilidade de eventos binomiais.

# Desenvolvimento teórico:

## Pressupostos:

* O acontecimento dos eventos devem ser aleatórios;
* Os experimentos podem exprimir apenas dois possíveis resultados (sim ou não, por exemplo);
* Os eventos devem ser independentes, o que significa que o acontecimento de um determinado evento não influencia no acontecimento ou não de outro.

## Definições matemáticas:

Temos por definição que:

<img src="https://github.com/xpcosmos/calculadora-de-probabilidades/blob/main/assets/funcao_prob.png" title="\bg_white P(k) = \binom{n}{k}p^kq^{n-k}" width = 200 />

Onde:

> _p_ = Probabilidade de determinado evento acontecer <br>
> _q_ = Probabilidade de determinado **NÃO** acontecer (1 - p) <br>
> _k_ = Quantidade de resultados desejados <br>
> _n_ = Números de ensaios realizados <br><br>

Para a resolução de um problema precisa se conhecer quantos eventos ocorrerão. Por exemplo, caso uma pessoa decida jogar um dado, o número de eventos será determinado pela quantidade de vezes que o dado será jogado.<br><br>
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
Utilizei _**try**_ e _**except**_ para prevenir os erros.

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
  
  # Autor

<a href="https://www.linkedin.com/in/mikeias-o-5a4b2a184/"><img src="https://camo.githubusercontent.com/4754d9b981ccaa192658e293fa6ab42b543520e7ad39756929edc7e95fca43aa/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d4c696e6b6564696e2d3065373661383f7374796c653d666c61742d737175617265266c6f676f3d4c696e6b6564696e266c6f676f436f6c6f723d7768697465266c696e6b3d4c494e4b2d444f2d5345552d4c494e4b4544494e" alt="linkedin" width="100"></a> <a href="mailto:mikeias.d.s.o@gmail.com"><img src="https://camo.githubusercontent.com/0137b0e6dbd05bb3986fa835806ca7b044f5cdaab7e4c8af8829ceec61195346/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d476d61696c2d4646303030303f7374796c653d666c61742d737175617265266c6162656c436f6c6f723d464630303030266c6f676f3d676d61696c266c6f676f436f6c6f723d7768697465266c696e6b3d4c494e4b2d444f2d5345552d454d41494c" alt="gmail" width="85">

# Licença

MIT License

Copyright (c) 2021 xpcosmos

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
