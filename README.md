# ConectaUFF

Introdução

O TweetScraper pode obter tweets da Busca do Twitter. Ele é construído com base no Scrapy sem usar as APIs do Twitter. Os dados coletados não são tão limpos quanto os obtidos pelas APIs, mas a vantagem é que você pode se livrar das limitações e restrições de taxa da API. Idealmente, você pode obter todos os dados da Busca do Twitter.

AVISO: seja educado e siga a política de cortesia dos crawlers.
Instalação

    Instale o conda, você pode obtê-lo no miniconda. A versão testada do Python é a 3.7.

    Instale os bindings do Selenium para Python: https://selenium-python.readthedocs.io/installation.html. (Nota: o erro KeyError: 'driver' é causado por uma configuração incorreta).

    Para usuários do Ubuntu ou Debian, execute:

    $ bash install.sh
    $ conda activate tweetscraper
    $ scrapy list
    $ # Se a saída for 'TweetScraper', então você está pronto para começar.

    O script install.sh irá criar um novo ambiente tweetscraper e instalar todas as dependências (como firefox-geckodriver e firefox).

Uso

    Altere o USER_AGENT no arquivo TweetScraper/settings.py para identificar quem você é.

 USER_AGENT = 'seu site/e-mail'

Na pasta raiz do projeto, execute o seguinte comando:

     scrapy crawl TweetScraper -a query="foo,#bar"

Onde query é uma lista de palavras-chave separadas por vírgula e entre aspas. A consulta pode ser qualquer coisa (palavra-chave, hashtag, etc.) que você deseja buscar na Busca do Twitter. O TweetScraper irá rastrear os resultados da busca da consulta e salvar o conteúdo dos tweets e as informações dos usuários.

    Os tweets serão salvos no diretório ./Data/tweet/ por padrão, e os dados dos usuários serão salvos em ./Data/user/. O formato dos arquivos é JSON. Você pode alterar os caminhos de salvamento modificando os parâmetros SAVE_TWEET_PATH e SAVE_USER_PATH no arquivo TweetScraper/settings.py, se desejar outro local.

Agradecimentos.
