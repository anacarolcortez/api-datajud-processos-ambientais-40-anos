# Processos ambientais na Amazônia Legal

Utilizando a biblioteca Requests do Python, o algoritmo "processos_ambientais_datajud" busca por dados básicos de processos ambientais utilizando a API do DataJud. Neste caso, em específico a busca foi realizada no TRF-1, que concentra 80% dos casos, mas pode ser feito com qualquer Tribunal, basta alterar a URL da requisição, conforme documentação das APIs do pŕóprio DataJud.

* API: https://api-publica.datajud.cnj.jus.br/api_publica_trf1/_search
* Documentação da API: https://datajud-wiki.cnj.jus.br/api-publica

A consulta utiliza os seguintes códigos de assuntos relativos a direitos ambientais:

* Direito Ambiental propriamente dito: 10110,9994,10116,11828,15302,15301,10114,10113,10119,11822,15008,15300,11830,11825,11829,11824,11823,10112,10111,11862,10115,10118,11827,11826, 10438, 11869, 10396
* Direito Ambiental dentro da esfera do Direito Administrativo e Outros Direitos Públicos: 10396

Campos obtidos:
* numero_processo
* classe
* data_ajuizamento
* orgao_julgador
* assuntos

Em seguida, o algoritmo "TRF1_webscraping_sincrono" realiza as buscas pelos detalhamentos dos processos com base em seus números, obtidos no algoritmo de requests. Para isso, faz raspagem de dados com Selenium na página web de consulta do órgão. O resultado inclui:

* Número do Processo
* Data de Distribuição
* Classe Judicial 
* Assunto
* Jurisdição
* Órgão Julgador
* Status
* Polo Ativo
* Polo Passivo
* Outros Interessados

O algoritmo de exemplo trabalha com controle de registros processados para contenção de falhas de execução caso ocorra algum bloqueio anti-bot. Recomenda-se rodar localmente e de maneira síncrona - as tentativas de refatoração com assincronicidade falharam por serem facilmente bloqueadas como bots pelo servidor.
