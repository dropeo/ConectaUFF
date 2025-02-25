Projeto Conecta UFF
Introdução

O TweetScraper é uma ferramenta avançada de coleta de dados que permite extrair tweets diretamente da Busca do Twitter, sem depender das APIs do Twitter. Ele é desenvolvido com a poderosa biblioteca Scrapy para web scraping e utiliza Selenium para garantir a captura de dados de forma eficaz. A principal vantagem dessa abordagem é a eliminação das limitações e restrições impostas pelas APIs do Twitter, permitindo a coleta de uma quantidade maior de dados de forma livre.

AVISO: Seja responsável e siga sempre a política de cortesia dos crawlers.
Objetivo do Projeto

Este é um projeto acadêmico com o objetivo de identificar e classificar notícias falsas na plataforma Twitter. A coleta de dados é realizada utilizando técnicas avançadas de web scraping em Python, enquanto a análise dos dados é feita por meio de processamento de linguagem natural. O projeto resultou na criação de um modelo de classificação de notícias falsas altamente preciso, com grande potencial para combater a disseminação de desinformação nas redes sociais.
Instalação

    Instale o conda. Você pode obtê-lo no Miniconda. A versão testada do Python é a 3.7.

    Instale os bindings do Selenium para Python: Instalação do Selenium. (Nota: o erro KeyError: 'driver' é causado por uma configuração incorreta).

    Para usuários do Ubuntu ou Debian, execute:

    $ bash install.sh
    $ conda activate tweetscraper
    $ scrapy list

    Se a saída for TweetScraper, então você está pronto para começar.

O script install.sh irá criar um novo ambiente tweetscraper e instalar todas as dependências necessárias, como firefox-geckodriver e firefox.
Uso

    Altere o USER_AGENT no arquivo TweetScraper/settings.py para identificar quem você é.

USER_AGENT = 'seu site/e-mail'

Na pasta raiz do projeto, execute o seguinte comando:

scrapy crawl TweetScraper -a query="foo,#bar"

Onde query é uma lista de palavras-chave separadas por vírgula e entre aspas. A consulta pode ser qualquer coisa (palavra-chave, hashtag, etc.) que você deseja buscar na Busca do Twitter. O TweetScraper irá rastrear os resultados da busca da consulta e salvar o conteúdo dos tweets e as informações dos usuários.

Os tweets serão salvos no diretório ./Data/tweet/ por padrão, e os dados dos usuários serão salvos em ./Data/user/. O formato dos arquivos é JSON. Você pode alterar os caminhos de salvamento modificando os parâmetros SAVE_TWEET_PATH e SAVE_USER_PATH no arquivo TweetScraper/settings.py, se desejar outro local.
Onde query é uma lista de palavras-chave separadas por vírgula e entre aspas. A consulta pode ser qualquer coisa (palavra-chave, hashtag, etc.) que você deseja buscar na Busca do Twitter. O TweetScraper irá rastrear os resultados da busca da consulta e salvar o conteúdo dos tweets e as informações dos usuários.

    Os tweets serão salvos no diretório ./Data/tweet/ por padrão, e os dados dos usuários serão salvos em ./Data/user/. O formato dos arquivos é JSON. Você pode alterar os caminhos de salvamento modificando os parâmetros SAVE_TWEET_PATH e SAVE_USER_PATH no arquivo TweetScraper/settings.py, se desejar outro local.

Agradecimentos.
