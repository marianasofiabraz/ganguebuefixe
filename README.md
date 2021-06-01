# GREENHOUSE GASES IN NEW ZEALAND 

📅️ **Última actualização**: 30 de maio de 2021

❗️If you would like an english version, please contact me or my colleague❗️

ℹ️ **Os nossos dados:**

Como alunos que não tem experiência no que toca a procurar dados decidimos, como ponto de partida, procurar simplesmente no google “CSV data” e ver que opções tínhamos para  selecionar os nossos dados. Na nossa pesquisa cruzamo-nos com o website **Stats NZ** que é uma agência de dados oficial da Nova Zelândia de renome logo é,  consequentemente, bastante confiável. Lá encontramos vários conjuntos de dados, desde dados de censos a dados económicos a dados de saúde, mas preferimos ir com dados relacionados com o meio ambiente. Escolhemos este tema não só porque nos diz algo pessoalmente, mas também porque queríamos uma boa mistura de dados escritos e de valores numéricos. Assim chegamos ao ficheiro CSV que decidimos analisar sobre **as emissões de Greenhouses Gases nas regiões da Nova Zelândia nos últimos anos**. 

Neste conjunto de dados existem alguns valores que estão em falta e, como é óbvio, no âmbito deste projecto só faz sentido analisar variáveis que estejam preenchidas em todos os parâmetros logo, através do data scraping eliminamo-los. Posto isto, no que toca a valores repetidos decidimos mantê-los ao longo das várias linhas em determinadas colunas. Por exemplo, na coluna dos anos aparecem vários valores repetidos no entanto esses valores repetidos referem-se a diferentes regiões, isto é, o ano 2018 aparece várias vezes na mesma coluna porque se refere ou à região Auckland ou à região Bay of Plenty ou à região Canterbury, etc… Tendo isto em conta, o tipo de dados mais relevantes para a nossa análise são **todas as regiões, os gases, os  anos e os valores da quantidade de gas produzido**.

O ficheiro CSV estava complementado por 7 colunas de dados, duas das quais decidimos remover. A coluna "anzsic _descriptor" não foi utilizada em nenhum contexto dentro do projeto, portanto achámos que seria mais conciso manter apenas as colunas utilizadas. Para além desta coluna, também removemos a coluna "magnitude" pois em todos os seus registos, apenas existia um valor - "Carbon dioxide equivalents" - e pensamos que se trata de um erro na entrada dos dados, logo não hesitámos na sua remoção. Apesar de não termos utilizado a coluna "year", pensamos que a sua existência completa o contexto do tema, logo decidimos mantê-la.

Além disto, à medida que foram criadas novas DataFrames baseadas na original, foram eliminadas as colunas não utilizadas naquele caso. Por exemplo, para analisar a quantidade total de gases por cada região, foi criada uma dataframe apenas com a coluna "Region" e a coluna "Total Data Value", pois estas eram as únicas importantes neste contexto.

🤔 **Contexto:**

Com o aumento da preocupação em salvar o nosso planeta tornou-se urgente compreender como é que cada zona está ou não a contribuir para isso. Assim, com esta análise das **emissões de gases estufa entre 2007 e 2018 na Nova Zelândia**, conseguimos perceber exatamente o impacto que as suas diversas regiões tem na poluição do ar, no aumento do efeito estufa e na destruição da camada de ozono. 

Eticamente este tipo de dados pareceu-nos correto porque, por um lado, não é uma invasão de **privacidade** dos indivíduos, mas, por outro, permite a quem se encontra numa determinada região na Nova Zelândia **ter conhecimento e ficar consciencializado** dos valores dos gases emitidos por lá. Mais ainda, o conhecimento destes valores é algo extremamente importante para se poder perceber onde estão as regiões mais e menos problemáticas para, futuramente, se poder **arranjar soluções** para reduzir a quantidade de gases estufa emitidos.

📚 **Bibliografia:**

Statz NZ: https://www.stats.govt.nz/ 

🧱 **Estrutura:**

`grenhouse.csv`: Contém os dados relativos ás emissões de greenhouse gases por região entre 2007 e 2018.

📔 **Dicionário dos dados:**

| Nome da coluna        | Significado           | Possíveis valores  |
| ------------- |:-------------:| -----:|
| `region` | Regiões da Nova Zelândia | West Coast |
| `anzsic_descriptor` | Australian New Zealand Standard Industrial Classification, ou seja, o setor que está a produzir os gases estufa | Agriculture |
| `gas` | Nome do gás estufa emitido | Carbon Dioxide |
| `units` | Unidades da quantidade de gases | Kilotoneladas |
| `magnitude` | Dados Errados | - |
| `year` | Anos entre 2007 e 2018 a que os valores se referem | YYYY |
| `data_value` | Quantidade do gás em kilotoneladas | Float >= 0 |
