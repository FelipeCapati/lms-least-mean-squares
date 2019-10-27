# LMS - Least Mean Squares #

## I.	 INTRODUÇÃO ##
Esse projeto tem como objetivo exemplificar a aplicação do algorítimo LMS, tambem chamado de MMQ (Método dos 
Mínimos Quadrados) utilizado para regressão multivariada.

## II.	FUNDAMENTAÇÃO TEÓRICA ##

### A.	METODO DOS MÍNIMOS QUADRADOS ###
O Método dos Mínimos Quadrados é um dos métodos utilizado para tratamento estatistico de dados experimentais (frequentemente
utilizado em Física e outras ciencias), utilizado para obter estimativas com base em dados.[1]<br>
A ideia basica é aproximar o sistema de equações a funções de reta, tomando com base um vetor de entrada X, como:

![Alt text](images/lms-eq1.png?)

Se a uma função de reta é dado por "Y = ax + b", na qual temos o termo independente e o termo que multiplica a variavel,
podemos transpor isso a um vetor de "p" estados, da seguinte maneira:

![Alt text](images/lms-eq2.png?)

Beta0 é o termo independente da função, tambem conhecido em Machine Learning como BIAS e cada outro termo do vetor Beta,
ou seja, Beta1 ... BetaP referece a como a variavel se relaciona a função Y de estudo. Podendo ser de tres maneiras:

<b>Relação positiva e Linear:</b>
 ![Alt text](images/lms-graph-01.png?)

<b>Relação negativa e Linear:</b> 
 ![Alt text](images/lms-graph-02.png?)
 
 <b>Sem Relacionamento:</b>
 ![Alt text](images/lms-graph-03.png?)
 
Na qual Beta é obtido calculando o mínimo erro quadratico, dada pela função:
![Alt text](images/lms-eq3.png?)

Ao fim podemos inferir que o vetor de Beta pode ser calculado da seguinte maneira:

![Alt text](images/lms-eq4.png?)

## III.	METODOLOGIA ##
Para o projeto vigente foi utilizado python juntamente com o Notebook Jupyter para prototipar o modelo do
algoritimo. Toda a base do algoritimo foi desenvolvido, ou seja, a multiplicação de matrizes, cálculo de 
matriz inversa, determinante, entre outras operações base que pode ser analisada em detalhes no path
<b>"./utilities/matrix.py"</b>.<br>
Tendo como base a fundamentação teorica abordada em II, o modelo do algorítimo esta proposto em <b>"./lms.py"</b>
na qual utiliza a função <b>"Matrix()"</b> para o calculo da regressão abordando dois modelos: Linear e Quadrático,
na qual, é possível passar a matriz w de pesos ou não dentro do argumento da função fit.<br>
Para o teste e análise do algorítimo foram propostos tres datasets para executar a regressão, sendo eles:
Alps Water Dataset, Books x Grades Dataset (Análise multivariada) e o US Census Dataset. Todos os dataset
foram fornecidos pelo professor Reinaldo Bianchi.

## IV. RESULTADOS ##
Os detalhes das implementações dos problemas propostos na metodologia pode ser analisados em <b>"./LMS.ipynb"</b> 
ou <b>"LMS.html"</b>.<br>
Para o problema AlpsWater temos o seguinte dataset.

![Alt text](images/alpswater-dataset.png?)

Utilizando o método dos mínimos quadrados Linear e Quadratico chegamos ao seguinte gráfico.

![Alt text](images/alpswater-graph-lms.png?)

Para o problema Books Attend Grade, temos o seguinte dataset

![Alt text](images/books-attend-grade-dataset.png?)

Analisando o dataset do problema, teremos uma regressão multivariada, na qual o gráfico scatter a seguir
ilustra a disposição de dados no espaço.

![Alt text](images/books-attend-grade-scatter-plot.png?)

Como o problema é de multivariável, foi plotado um gráfico que compara a regressão linear e quadratica na qual
no eixo X temos o valor real de Y e no eixo Y temos o valor da regressão de Y.

![Alt text](images/books-attend-grade-lms.png?)

Para o problema US Census, temos o seguinte dataset:

![Alt text](images/us-census-dataset.png?)

Na qual foi plotado o gráfico a seguir que compara os dados juntamente com a regressão utilizando o método linear
e o método quadratico:

![Alt text](images/us-census-lms.png?)

## V. CONCLUSÃO ##
Dado os resultados vistos em IV podemos inferir que o Método dos Mínimos Quadrados chegou ao resultado esperado e
graficamente é possivel inferir que o erro de aproximação é relativamente baixo.<br>
Um dos objetivos do projeto em curso é implementar o algoritimo do MMQ. Se analisarmos os dados chegamos a conclusão de 
que o algorítimo foi implementado corretamente, porém não é possivel fazer inferencias relativas aos problemas abordados 
anteriormente devido a não implementação de funções que calculem o erro, erro médio quadrático, implementação do Teste F,
Teste T e outras abordagens estatísticas que validem a solução de regressão proposta anteriormente.

## VI. AGRADECIMENTOS ##

Agradecimentos especiais a CAPES e ao Centro Universitário FEI por financiar o mestrado que está em curso; 
ao professor Reinaldo Bianchi por proporcionar visões sobre o mundo acadêmico e orientar trabalhos científicos 
com o objetivo de lapidar os conhecimentos abordados em sala; aos meus pais e a minha família que sempre me 
apoiaram em meio a dificuldades.

## VII. REFERÊNCIAS ##

[1]	O. A. M. Helene, Método dos mínimos quadrados com formalismo matricial: guia do usuário, Editora: Livraria da Física, São Paulo, 2016<br>
[2]	R. Bianchi, Tópicos Especiais em Aprendizagem, 2019, ppt slide Centro Universitário FEI.