**ÍNDICE**
<br>
<a href="#1">1. Introdução</a>
<br>
<a href="#2">2. Objetivo</a>
<br>
<a href="#3">3. Modelagem da Base de Dados</a>
<br>
<a href="#4">4. Dashboard</a>
<br>
<a href="#dis">5. Disclaimer</a>

<h2 id="1"></h2>

**1. INTRODUÇÃO**
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Este projeto aborda a análise e visualização de dados, mais especificamente, dados das vendas de uma pizzaria. Para a concretização do projeto, foram realizadas duas etapas. Inicialmente, foi feita uma limpeza dos dados presentes no dataset utilizado Python (Pandas, NumPy) e uma Análise Descritiva dos dados.</p>
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Para a segunda etapa, a fim de responder às perguntas levantadas sobre os dados, uma visualização destes foi feita. Foi desenvolvido um Dashboard Interativo fazendo uso da ferramenta Power BI para a apresentação do comportamento dos dados no contexto das dúvidas estabelecidas.</p>

<h2 id="2"></h2>

**2. OBJETIVO**
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Responder, de forma visual (em um dashboard), as seguintes perguntas:
<li>1 - Qual é a receita total gerada no período analisado? </li>
<li>2 - Qual é o valor médio de um pedido (Average Order Value - AOV)? </li>
<li>3 - Quantas pizzas foram vendidas no total? </li>
<li>4 - Quantos pedidos foram feitos no total? </li>
<li>5 - Qual a média de pizzas por ordem? </li>
<li>6 - Quais são os dias da semana com maior volume de vendas? </li>
<li>7 - Como as vendas se distribuem ao longo do ano? Existem meses com desempenho significativamente melhor ou pior? </li>
<li>8 - Qual o total de pizzas vendidas por categoria? </li>
<li>9 - Existe alguma diferença na emissão de ordens por semana do mês? </li>
<li>10 - Qual o percentual de pizza vendidas por categoria? </li>
<li>11 - Qual o percentual de pizza vendidas por tamanho? </li>
<li> - Quais são as top 5 melhores pizzas em termos de faturamento, quantidade e pedidos? </li>
<li> - Quais são as top 5 piores pizzas em termos de faturamento, quantidade e pedidos? </li>

<h2 id="3"></h2>

**3. MODELAGEM DA BASE DE DADOS**
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;A estrutura/modelagem da base de dados tem alguns pontos de possíveis melhorias, dividir a tabela principal em mais entidades é o ponto principal, organizar todas as informações citadas em uma única entidade pode ocasionar em diversos problemas de inserção de dados, erros de digitação podem ser frequentes no modelo no estado atual. A estrutura original pode ser vista abaixo:</p>
<br>
Venda(#pizza_id, order_id, pizza_name_id, quantity, order_date, order_time, unit_price, pizza_size, pizza_category, pizza_ingredients, pizza_name)
<br><br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Uma alternativa seria dividir a entidade principal em 6 outras entidades, dessa forma, a relação dos dados de uma coluna com os de outra coluna seria mais clara, além de evitar erros de digitação do usuário. Um Diagrama de Entidade-Relacionamento (DER ou MER) que siga as premissas levantadas pode ser visto abaixo:</p>
<img src="https://github.com/user-attachments/assets/e808a3df-f1a2-44f2-8a93-bb40c9b654cb" alt=0>
<br>

<h2 id="4"></h2>

**4. DASHBOARD**
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Para a visualização dos dados de forma a conseguirmos responder as perguntas sobre as vendas da pizzaria, o dashboard foi estruturado dividindo as informações em duas páginas.</p>

**4.1 Tela Inicial**
<br>
<img src="https://github.com/user-attachments/assets/7087a281-aba9-4f2d-9982-1c4c9ad2f530" alt="1">
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;A primeira página, ou ainda, a Tela Inicial, exibe na primeira coluna à esquerda, um menu, onde inicialmente podemos navegar entre às páginas, logo abaixo, temos algumas opções de filtros a serem utilizados para uma possível análise mais aprofundada. Por fim, há uma área de links para contato.</p>
<p>&nbsp;&nbsp;&nbsp;&nbsp;Desconsiderando o título, a primeira linha horizontal exibe alguns KPIs, estes cartões respondem as perguntas 1, 2, 3, 4 e 5. A segunda linha, nas duas primeiras caixas, nos mostra a quantidade de ordens emitidas por dia da semana e por mês, esses gráficos nos ajudam a responder as perguntas 6 e 7. Quanto as vendas pelos dias da semana, percebe-se que dias próximos de sexta-feira (incluindo sexta-feira) tendem a ter um maior índice de ordens e quanto à emissão de ordem pelos meses do ano, podemos observar que temos um pico de vendas em julho, enquanto que até outubro as vendas tendem a cair. A terceira, e última, caixa desta linha responde a pergunta 8. Podemos observar que a pizza da categoria Classic tem uma boa diferença em questão de vendas quando comparada com as outras categorias.</p>
  
<p>&nbsp;&nbsp;&nbsp;&nbsp;Na terceira linha horizontal, iniciando respondendo a pergunta 9, temos que as vendas tendem a se manter estáveis na 2ª, 3ª e 4ª semana do mês, decaindo nas outras. Deve-se levar em consideração que os meses dificilmente possuem semanas 5 e 6, isto pode explicar o porquê da queda observada nessas duas semanas finais. Por fim, temos dois gráficos de aneis que nos mostram o percentual de pizzas vendidas por categoria e tamanho, isto faz referência as perguntas 10 e 11, respectivamente. Pizzas do tipo Grande englobam grande parte das pizzas, enquanto que as do tipo XExtra-Grande são pouco pedidas. Para a proporção por categoria, há um bom equilíbrio nas vendas.</p>
<br>

**4.2 Melhores e Piores Vendas**
<br>
<img src="https://github.com/user-attachments/assets/feb74bd8-915c-4564-a627-7a3ff32a11d3" alt="2">
<br>
<p>&nbsp;&nbsp;&nbsp;&nbsp;A segunda página, traz novos gráficos de barras com os top 5 melhores/piores nomes de pizzas dependendo da métrica (elas vão de Faturamento, Quantidade Vendida de Pizzas e Quantidade de Ordens Emitidas contendo estas pizzas). Quanto ás top melhores, pode-se observar que não há uma diferença significante entre as melhores, mas ao observar o tipo das pizzas, percebe-se que as pizzas "The Classic Deluxe", "The Thai Chicken" e "The Barbecue Chicken Pizza" sempre aparecem entre os top 5.
</p>

<h2 id="dis"></h2>

**DISCLAIMER**
<br>
1 - O arquivo Dashboard Vendas.pdf foi importado propositalmente no formato pdf. Infelizmente, dessa forma, a interatividade do dashboard não pode ser representada. 
<br>
2 - O projeto tem como característica primária o aprendizado. A base de dados utilizada está presente em: 
https://topmate.io/data_tutorials/868486?utm_source=public_profile&utm_campaign=data_tutorials 
