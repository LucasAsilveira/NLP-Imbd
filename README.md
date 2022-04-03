# NLP-Imbd: Análise de Sentimento

## Intrudoção
Este é um projeto de estudos, onde será feita um modelo de Machine Learn usando técnicas de NLP para estudo e aprendizado destas. 

## 1. Problema
O site da IMBd possúi resenhas do público sobre diversos filmes, com classificações positivas ou negativas. Assim, usando técnicas de NLP é possível desenvolver um algoritmo que analise as resenhas e realize uma comparação com a classificação dada pelos usuários consiga identificar se a resenha é uma resenha positiva ou negativa. 

## 2. Técnicas Usadas:

- NLP(Natural Language Processing): Utiliza de técnicas de AI e computacionais mescladas com Linguística para comprensão automática da linguagem natural. A disponibilidade de dados em linguagem natural é enorme, tratar e desenvolver algorítmos que possibilitem aplicações úteis com estas informaçoes é parte fundamental do NLP. 

### 2.1 Vetorização:

- Bag of Words: Representação simplificada utilizando NLP. O texto é representado como um muticonjunto de suas palavras, desconsiderando sua estrutura gramátical e ordenação, mas mantendo a multiplicidade.
- IF-IDF( Term Frequency – Inverse Document Frequency ): Diferente da Bag of Words, o IF-IDF ao converter palavras em vetores, da peso a cada palavra conforme a frequência que aparecem, usando a semântica da palavra. 
- N-Gram: Sequência contínua de N itens de uma determinada amostra de texto ou fala, onde N pode ser qualquer número interio. Nesta técnica, os n-grams ajudam a reter o contexto.

### 2.2 Bibliotecas NLP

- NLTK( Natural Language Toklkit ): Conjunto de bibliotecas e programas para processamento de NLP, suportando funcionalidades de classificação, tokenização, semantização, marcação, analise e raciocínio semântico. 

### 2.3 Algoritmo de Machine Learning

- Logistic Regression: Processo de modelagem da probabilidade de um resultado discreto dado uma variável de entrada. Mais comumente usado para modelar resultados binários. Usada em problema de classificação onde se quer determinar se uma nova amostra se encaixa melhor em uma categoria. 

### 2.4 Técnicas de visualização
- Word Cloud: Conhecida como nuvem de palavras ou etiquetas. Onde gera-se uma imagem com as palavras mostradas de tamanho proporcional ao tamanho da fonte com a quantidade de repetições das mesmas. 

### 3.0 Etapas do projeto

- Ciclo 1: Foi feito uma analise inicial do dataset, checando a dimensão e os textos das resenhas. Criada uma feature com o resultado das avaliaçes como 1 para as positiva e 0 para as negativas, para facilitar o processamento do algorítmo. 
Usando a técnica de bag of words foi feita a vetorização das resenhas, assim foi possível criar um modelo de regressão logistica usando o LogisticRegression da biblioteca sklearn, criando nosso primeiro modelo de analise de sentimento das resenhas. Separando as resenhas em treino e teste. 
Com este primeiro modelo conseguimos um resultado de acertividade de 75,34%

- Ciclo 2: Buscando melhorar o primeiro modelo construído, realizou-se uma analise usando o WordCloud para visualizar as palavras mais usadas, separando as resenhas em positivas e negativas. Assim, foi possivel perceber que muitas das palavras que eram mais frequêntes nas resenhas eram usadas para tanto nas resenhas positivas como nas negativas, então foi realizado o primeiro tratamento usando a função 'stopwords' da biblioteca nltk para retirar da analise do algoritmo palavras que eram pouco uteis para a classificação do modelo. 
Após este primeiro tratamento o resultado da acertividade foi de 77,63%

- Ciclo 3: Neste ciclo foi feito mais dois tratamentos nas resenhas. Primeiro retiramos a pontuação e em seguida a acentuação dos textos.
Ao rodar o modelo após estes dois tratamentos obteve-se uma acertividade de 77,68%

- Ciclo 4: Neste ciclo fizemos mais 2 tratamentos, primeiro foi normalizado o texto transformando todas as palavras em minúsculas em seguida usamos o Steammer do NLTK, esta função remove afixos morfológicos das palavras, deixando apenas o seu radical. 
Após estes novos tratamentos, o modelo teve uma acertividade de 79,56%.

- Ciclo 5: Após realizar os tratamentos iniciais, resolvemos testar diferentes tipos de vetorização, para compararmos o desempenho do modelo com outras téncias além da bag of words que é uma das mais basicas. Assim, foi utilizada as técnicas TF-IDF e a N-GRAM. Realizando vetorizações mais sofisticadas na tentativa de melhorar ainda mias nosso modelo. 
Com isto obteve-se um resultado de 79,63 de acertividade no modelo final com o uso de N-GRAM. 

### 4.0 Resultados

##### 4.1 Comparação dos resultados após cada tratamento:

![image](https://user-images.githubusercontent.com/94136773/161434122-6abed4aa-f1ac-45e9-b01a-418160a94d23.png)









