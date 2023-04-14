### Uniasselvi_project_raw_tweets

### Objetivo
Estabelecido o Twitter como a base de dados, sendo os comentários dos usuários chamados de “tweets” objetiva-se neste projeto efetuar a coleta para que seja realizado um pré-processamento preparando a classificação dos “tweets” e suas conotações. Ou seja,  se o sentimento passado por aquele “tweet” poderia ser positivo, negativo ou neutro. Então, com o uso de ”machine learning” e da técnica de Processamento de Linguagem Natural (PLN), iremos treinar um modelo que se comporte como um classificador de “tweets” acerca do tema de busca Uniasselvi. 
Após o treinamento, poderemos utilizar este modelo que foi treinado em uma base com “tweets” rotulados para assim poder categorizar nossos “tweets” criando um rótulo de classificação de sentimento dos 'tweets' do “dataset”. 

### Especificação Técnica
Para a realização deste projeto, optamos em criar nosso próprio dataset, através de uma biblioteca disponível na linguagem Python chamada Snscrape que irá simular o comportamento de uma API para assim efetuarmos a coleta de nossos dados com foco em tweets publicados relacionados à Uniasselvi.

Após a coleta, teremos uma base de dados com os seguintes campos:
- Data_ref Tipo Data: Data da postagem do Tweet.
- Tweet_id Tipo texto: ID daquele Tweet.
- Tweet_url Tipo texto: Url daquele Tweet.
- Tweet_user Tipo texto: Usuário que escreveu o Tweet.
- Tweet_hashtags 	Tipo texto: Hashtag utilizada naquele Tweet caso houver.
- Tweet Tipo texto: Tweet em forma de texto.
- Likes Tipo Inteiro: Quantidade de likes ou curtidas que aquele Tweet recebeu 
- Sentimento Tipo texto: Campo que será incluso ao fim do projeto pelo classificador.

Para efetuarmos a rotulação dos Tweets treinaremos o modelo em uma base classificada, utilizando como principal algoritmo de Machine Learning o Naive Bayes MultinomialNB.
Com os dados rotulados será realizada a etapa de pré-processamento dos dados utilizando técnicas de processamento de linguagem natural. Tendo a base tratada será feita a divisão de treino e teste e avaliação utilizando o classification_report do pacote Scikit-learn. E por fim o treino do modelo.
