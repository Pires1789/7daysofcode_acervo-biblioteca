# Informações sobre acervo de biblioteca universitária

Este projeto é parte do desafio #7DaysOfCode e objetiva treinar e estudar habilidades de Python Pandas e outras hard skills (como Git e estatística) no contexto de análise de dados.

| :placard: Vitrine.Dev |     |
| -------------  | --- |
| :sparkles: Nome        | **Análise do acerto da biblioteca**
| :label: Tecnologias | python; tableau
| :fire: Desafio     | [7 Days of Code - Python Pandas](https://7daysofcode.io/matricula/pandas)

## 7 Days of Code: o desafio
  Explorar os dados de empréstimos dos acervos do sistema de bibliotecas da UFRN utilizando o **Pandas**. Sera possível fortalecer conhecimentos sobre importação de diferentes tipos de arquivos,formatos de dados, agregações, divisões e transformações de tabelas, e até a exportação de tabelas estilizadas com sua análise pronta para ser inserida em alguma aplicação.

  ### Dia 01 - 17/11/2023
  A proposta do primeiro dia é a importação de vários arquivos CSV e parquet, além de um join entre esses arquivos. 
  Optei por algumas etapas de limpeza como:

  - Organização das colunas dos arquivos de empréstimo;
  - Alteração do datatype de certas colunas (principalmente colunas de ID)

  Com relação ao merge, optei pelo left já que perdemos apenas 3k de registros. Por curiosidade montamos um relatório com os livros que não foram requisitados pelos alunos.
  Entendemos que esse tipo de relação é interessante já que a universidade pode optar por divulgar melhor tais livros ou reformular seu acervo, talvez doando esse material.
  
  ```
  dfnao_usados = pd.merge(df_emprestimos, df_exemplares, on='codigo_barras', how='right', indicator=True)
  dfnao_usados[['codigo_barras', 'colecao', 'biblioteca', 'status_material']].head()
  ```

  ### Dia 02 - 18/11/2023
  Limpeza de dados. Essa etapa está programa para acontecer no dia 18 de novembro - que é um sábado. Eu optei por não realizar nenhum tipo de atividade neste final de semana para aproveitar melhor meu tempo com miha família. Então voltaremos na segunda-feira!
