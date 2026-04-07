# Processos ambientais de 1985 a 2025

Utilizando a biblioteca Requests do Python, o algoritmo busca por dados básicos de processos ambientais utilizando a API do DataJud. Neste caso, em específico a buca foi realizada no TRF-1, que concentra 80% dos casos. Também serão feitas requisições nos Tribunais de Justiça estaduais na região da Amazônia Legal, todos disponíveis nas APIs do pŕóprio DataJud.

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

A próxima etapa, além de realizar as buscas nos órgãos regionais, será de webscraping de detalhes dos processos em suas respectivas páginas de consulta dos órgãos competentes. Serão obtidos informações como o andamento e as partes envolvidas.

O material será utilizado em projeto da ONG Sumaúma.

Neste caso, do TRF-1, foram coletados 58.043 processos.

OBS: o algoritmo do exemplo foi executado em 07/04/2026 às 17:00
