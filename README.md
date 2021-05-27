# GREENHOUSE GASES IN NEW ZEALAND ☁️🇳🇿

📅️ **Última actualização**: 27 de maio de 2021

❗️If you would like an english version, please contact me or my colleague.

ℹ️ **Os nossos dados:**

Como alunos que não tem experiência no que toca a procurar dados decidimos, como ponto de partida, procurar simplesmente no google “CSV data” e ver que opções tínhamos para  selecionar os nossos dados. Na nossa pesquisa cruzamo-nos com o website **Stats NZ** que é uma agência de dados oficial da Nova Zelândia de renome logo é,  consequentemente, bastante confiável. Lá encontramos vários conjuntos de dados, desde dados de censos a dados económicos a dados de saúde, mas preferimos ir com dados relacionados com o meio ambiente. Escolhemos este tema não só porque nos diz algo pessoalmente, mas também porque queríamos uma boa mistura de dados escritos e de valores numéricos. Assim chegamos ao ficheiro CSV que decidimos analisar sobre **as emissões de Greenhouses Gases nas regiões da Nova Zelândia nos últimos anos**. 

Neste conjunto de dados existem alguns valores que estão em falta e, como é óbvio, no âmbito deste projecto só faz sentido analisar variáveis que estejam preenchidas em todos os parâmetros logo, através do data scraping eliminamo-los. Posto isto, no que toca a valores repetidos decidimos mantê-los ao longo das várias linhas em determinadas colunas. Por exemplo, na coluna dos anos aparecem vários valores repetidos no entanto esses valores repetidos referem-se a diferentes regiões, isto é, o ano 2018 aparece várias vezes na mesma coluna porque se refere ou à região Auckland ou à região Bay of Plenty ou à região Canterbury, etc… Tendo isto em conta, o tipo de dados mais relevantes para a nossa análise são **todas as regiões, os setores descritos na coluna “anzsic_descriptor”, os respetivos gases, anos e valores da quantidade de gas produzido**. Mais ainda, não há nenhum tipo de dado que necessite de ser corrigido ou rejeitado o que é uma mais valia.

🤔 **Contexto:**

📚 **Bibliografia:**

Statz NZ: https://www.stats.govt.nz/ 

🧱 **Estrutura:**

'greenhouse.csv'

📔 **Dicionário dos dados:**

| Nome da coluna        | Significado           | Possíveis valores  |
| ------------- |:-------------:| -----:|
| `data` | Data da publicação dos dados | DD-MM-YYYY |
| `confirmados_arsalentejo` | Casos confirmados na ARS Alentejo     | Inteiro >= 0 |
