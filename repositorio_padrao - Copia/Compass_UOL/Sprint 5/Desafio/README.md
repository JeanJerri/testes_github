# Etapa I


- Selecionei um arquivo .csv do portal de dados indicado no desafio (https://dados.gov.br/home) onde é registrado as vendas de derivados de petróleo e biocombustíveis feito pela Agência Nacional do Petróleo. Nele, são apresentados os dados referentes à quantidade vendida entre a UF de origem e a de destino informada pelos produtores e o mês em que foram realizadas essas vendas.

[biodiesel_dadosabertos_csv_vendas.csv](../Desafio/etapa-1/biodiesel_dadosabertos_csv_vendas.csv)

- Fiz a analise do conjunto de dados para elaborar uma consulta com os critérios solicitados no desafio.

![Critérios](../Desafio/critérios%20(1).png)
- ![Critérios](../Desafio/critérios%20(2).png)

- Subi o arquivo para um bucket que eu criei para executar a consulta.

![Bucket](../evidencias/bucket%20criado.png.png)

- Na consulta obtive a data em que foi realizado o processamento através da função UTCNOW() e fiz sua conversão com o TO_STRING. 

- Usei as funções agregadas SUM, AVG e COUNT para fazer a soma do total de produtos vendidos, a média por vendas e a quantidade de vendas, - respectivamente. E também usei o SUM para calcular a quantidade de vendas nordeste/sudeste.

- Fiz um filtro para mostrar apenas os registros que tem como origem o Sul ou como destino o nordeste e as que tem como origem o nordeste e destino sudeste, logo, selecionando dados com pelo uma das 3 condições.

- Tudo isso somente em uma consulta.

    ![Evidencia 1](../Desafio/etapa-1/consulta_sql.sql)

![Evidencia 1](../evidencias/execução%20da%20consulta%20SQL.png)
