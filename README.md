# NLP-Imbd: Análise de Sentimento

## Introdução
Este é um projeto de estudos, onde será feita um modelo de machine learning usando técnicas de NLP para estudo e aprendizado destas. 

## 1. Problema
O site da IMBd possui resenhas do público sobre diversos filmes, com classificações positivas ou negativas. Assim, usando técnicas de NLP é possível desenvolver um algoritmo que analise as resenhas e realize uma comparação com a classificação dada pelos usuários e assim consiga identificar se a resenha é uma resenha positiva ou negativa. 

## 2. Técnicas Usadas:

- NLP(Natural Language Processing): Utiliza de técnicas de AI e computacionais mescladas com Linguística para compreensão automática da linguagem natural. A disponibilidade de dados em linguagem natural é enorme, tratar e desenvolver algoritmos que possibilitem aplicações úteis com estas informações é parte fundamental do NLP. 

### 2.1 Vetorização:

- Bag of Words: Representação simplificada utilizando NLP. O texto é representado como um multiconjunto de suas palavras, desconsiderando sua estrutura gramátical e ordenação, mas mantendo a multiplicidade.
- IF-IDF( Term Frequency – Inverse Document Frequency ): Diferente da Bag of Words, o IF-IDF ao converter palavras em vetores, da peso a cada palavra conforme a frequência que aparecem, usando a semântica da palavra. 
- N-Gram: Sequência contínua de N itens de uma determinada amostra de texto ou fala, onde N pode ser qualquer número inteiro. Nesta técnica, os n-grams ajudam a reter o contexto.

### 2.2 Bibliotecas NLP

- NLTK( Natural Language Toklkit ): Conjunto de bibliotecas e programas para processamento de NLP, suportando funcionalidades de classificação, tokenização, semantização, marcação, analise e raciocínio semântico. 

### 2.3 Algoritmo de Machine Learning

- Logistic Regression: Processo de modelagem da probabilidade de um resultado discreto dado uma variável de entrada. Mais comumente usado para modelar resultados binários. Usada em problema de classificação onde se quer determinar se uma nova amostra se encaixa melhor em uma categoria. 

### 2.4 Técnicas de visualização
- Word Cloud: Conhecida como nuvem de palavras ou etiquetas. Onde gera-se uma imagem com as palavras mostradas de tamanho proporcional ao tamanho da fonte com a quantidade de repetições das mesmas. 

## 3.0 Etapas do projeto

- Ciclo 1: Foi feito uma analise inicial do dataset, checando a dimensão e os textos das resenhas. Criada uma feature com o resultado das avaliações como 1 para as positiva e 0 para as negativas, para facilitar o processamento do algoritmo. 
Usando a técnica de bag of words foi feita a vetorização das resenhas, assim foi possível criar um modelo de regressão logística usando o LogisticRegression da biblioteca sklearn, criando nosso primeiro modelo de analise de sentimento das resenhas. Separando as resenhas em treino e teste. 
Com este primeiro modelo conseguimos um resultado de assertividade de 75,34%

- Ciclo 2: Buscando melhorar o primeiro modelo construído, realizou-se uma analise usando o WordCloud para visualizar as palavras mais usadas, separando as resenhas em positivas e negativas. Assim, foi possível perceber que muitas das palavras que eram mais frequentes nas resenhas eram usadas para tanto nas resenhas positivas como nas negativas, então foi realizado o primeiro tratamento usando a função 'stopwords' da biblioteca nltk para retirar da analise do algoritmo palavras que eram pouco uteis para a classificação do modelo. 
Após este primeiro tratamento o resultado da assertividade foi de 77,63%

- Ciclo 3: Neste ciclo foi feito mais dois tratamentos nas resenhas. Primeiro retiramos a pontuação e em seguida a acentuação dos textos.
Ao rodar o modelo após estes dois tratamentos obteve-se uma assertividade de 77,68%

- Ciclo 4: Neste ciclo fizemos mais 2 tratamentos, primeiro foi normalizado o texto transformando todas as palavras em minúsculas em seguida usamos o Steammer do NLTK, esta função remove afixos morfológicos das palavras, deixando apenas o seu radical. 
Após estes novos tratamentos, o modelo teve uma assertividade de 79,56%.

- Ciclo 5: Após realizar os tratamentos iniciais, resolvemos testar diferentes tipos de vetorização, para compararmos o desempenho do modelo com outras téncias além da bag of words que é uma das mais básicas. Assim, foi utilizada as técnicas TF-IDF e a N-GRAM. Realizando vetorizações mais sofisticadas na tentativa de melhorar ainda mias nosso modelo. 
Com isto obteve-se um resultado de 79,63 de assertividade no modelo final com o uso de N-GRAM. 

## 4.0 Resultados

#### 4.1 Tabela com resultados após cada tratamento:

Na tabela a baixo, conseguimos melhorar uma assertividade de 75.32%, com o modelo sem nenhum tratamento para uma assertividade de 79,56% após realizar todos os tratamentos. Com isto tivemos uma melhora de 4,25% no modelo apenas realizando tratamentos nos textos das resenhas.  

![image](https://user-images.githubusercontent.com/94136773/161434221-e13c1741-955c-49fc-9494-a9ef38b315af.png)




#### 4.2 Tabela com resultados com diferentes técnicas de vetorização:

Ao implementar técnicas de vetorização mais sofisticadas ao nosso modelo, não conseguiu-se uma melhor significativa. Analisando a tabela a baixo, percebe-se que utilizando a técnica TF-IDF o resultado foi de 0,01% inferior, ao utilizar o Ngram conseguimos uma melhora de 0,08%

![image](https://user-images.githubusercontent.com/94136773/161434438-32558962-803f-4af2-a409-d9f532f3f217.png)

## 5.0 Próximos passos

- Implementação de outros algorítmos de Machine Learning. 
- Uso do modelo obtido em resenhas filmes de outros sites para testar a usualidade do modelo

## 6.0 Conclusão

O objetivo principal deste projeto de estudos que era estudo e implementação de técnicas de NLP para analise de sentimento foi feita com sucesso. Conseguimos implementar diversas técnicas de tratamento para melhoria do modelo assim como usar algumas das principais técnicas de vetorização. 
Foi usado apenas um modelo de Machine Learning, pois o objetivo deste projeto de estudo não era focado em achar o melhor modelo ou estudar algortimos de Machine Learning. Porém fica para um próximo ciclo, implementar outros algoritmos e testar o modelo melhorado em diferentes dados com resenhas de filmes testando a sua usabilidade. 








