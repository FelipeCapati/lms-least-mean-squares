# LMS - Least Mean Squares #

## I.	 INTRODUÇÃO ##
Esse projeto tem como objetivo exemplificar a aplicação do algorítimo LMS, tambem chamado de MMQ (Método dos 
Mínimos Quadrados) utilizado para regressão multivariada.

## II.	FUNDAMENTAÇÃO TEÓRICA ##
### A.	METODO DOS MÍNIMOS QUADRADOS ###

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

TODO: FAAAAAAAAAAAAAZER AINDA<BR><BR>
Dado os resultados vistos em IV podemos inferir que o Método de Integração de Monte Carlo é funcional, 
converge ao valor real de (9) com cerca 30.000 iterações e que o tempo de processamento tem um comportamento 
crescente proporcional a N tanto para o cálculo da integral utilizando MPI, quanto para integral 
sem o MPI.<br>
Para essa análise 30.000 iterações foram suficientes, porém vale ressaltar que o valor de N é função do 
problema proposto, ou seja, varia para cada aplicação do modelo.<br> 
O MPI proporcionou um aumento significativo para o tempo de processamento (3,5x) quando utiliza-se 4 nós de 
processamento, sendo que é possível escalar esse valor para M máquinas ligadas em rede, o que daria um 
aumento muito mais significado do que o apresentado nesse projeto.

## VI. AGRADECIMENTOS ##

Agradecimentos especiais a CAPES e ao Centro Universitário FEI por financiar o mestrado que está em curso; 
ao professor Reinaldo Bianchi por proporcionar visões sobre o mundo acadêmico e orientar trabalhos científicos 
com o objetivo de lapidar os conhecimentos abordados em sala; aos meus pais e a minha família que sempre me 
apoiaram em meio a dificuldades.

## VII. REFERÊNCIAS ##

TODO FAZER AINDA <BR><BR>
[1]	R. E. Caflisch, “Monte Carlo and quasi-Monte Carlo methods” Mathematics Department, UCLA, Los Angeles, CA, USA, 1998.<br>
[2]	W. Fellen, An Introduction to Probability Theory and its Application, vol. 1. Wiley, 1971.