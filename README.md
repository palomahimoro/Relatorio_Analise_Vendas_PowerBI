# Relatorio_Analise_Vendas_PowerBI

# Exercício DSA - Crie um Dashboard no Power BI que responda a estas perguntas:


1- Qual dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas? 

2- Qual o total de vendas por estado e por categoria? Use um mapa.

3- Qual o total de vendas por segmento? 

4- Qual segmento tem maior influência no valor médio de venda? 


-
Anotações

Preencher a lacuna entre os dados e a tomada de decisão. Business  Intelligence (Análise descritiva)/ inteligência  de  Negócios,  é  um  termo  abrangente destinado  a  cobrir  todas  as  atividades  necessárias  para  que  uma  empresa  transforme  dados brutos em conhecimento. 
O objetivo final é ser capaz de aumentar os lucros e aprimorar sua vantagem competitiva.
Os softwares de BI têm sido fundamentais nesta progressão constante para um conhecimento mais  aprofundado  sobre  negócios,  concorrentes,  clientes,  indústria,  mercado  e  fornecedores, para citar apenas alguns possíveis objetivos métricos. 

O dados x Informação x Conhecimento x Inteligência
Inteligência é a capacidade de resolver problemas, usando o conhecimento, através das informações disponíveis. 
Nosso objetivo é começar com os dados, transformá-los em informações e conhecimento e permitir que tomadores de decisão usem sua inteligência para resolver problemas, a partir do conhecimento adquirido. 

A técnica de Análise depende do tipo de negócio: Descritiva (o que aconteceu) Diagnóstica (Por que isso aconteceu?) Preditivam (O que acontecerá?) Prescritiva (O que deve ser feito?).

Big Data Analytics: Extrair conhecimento a partir dos dados (Big Data) aplicando técnicas de análise (Data Science). Análise descritiva.  

Machine Learning: Treinar algoritmos para encontrar os padrões nos dados de forma automática e então fazer previsões. Análise Preditiva. 

Big  Data geralmente se refere a grandes conjuntos de dados que são simplesmente muito grandes para ser gerenciados ou consultados com ferramentas tradicionais de análise de dados. Esse volume imenso de dados é resultado da explosão  de ferramentas de geração de dados, rastreamento, monitoramento, transações e redes sociais (para citar alguns) que se tornaram tão populares nos últimos anos.Não  só  essas ferramentas  geram  cargas  denovos  dados,  mas  também  geram  um  novo tipo de dado, chamado dados "não estruturados". Em termos gerais, dados não estruturados são simplesmente  dados  que  não  foram  organizados  de  forma  predefinida. Um dos principais produtos atualmente para armazenar e processar Big Data, é o Apache Hadoop, que é uma estrutura de software de código aberto que foi projetado especificamente para pesquisar grandes conjuntos de dados armazenados de forma distribuída (o que significa: no seu data center, na nuvem ou em ambos). 

Pg inicial> obter dados
Detecção de dados: com base em conjunto de dados inteiro; Delimitador: o que faz a separação das coluna. 
Enconding: quando os acentos estão incorretos: alterar origem do arquivo para: UTF-8. Carregar. 

Quando está nas configurações regionais em Portugues, se os dados tiverem centavos, o ponto não é reconhecido como separador. Necessário edição.
Trabalho de Manipulação:
Pagina inicial> Transformar dados> o tipo de dado pode ser alterado no ícone ao lado do título.
Do lado direito, em etapas aplicadas fica o histórico do que foi aplicado e é possível desfazer no X.
Fechar e Aplicar. 

Criar gráficos/ tabelas> Relatório> Visualizações (lado direito), escolher o tipo de gráfico> 

Drill-Down (descer) up(subir) chamado também de grau de granualidade, a medida mais granular é por hora/ minutos, etc. Navegar na hierarquia de dados> ao clicar no gráfico aparece os ícones em cima, onde é possível visualizar por ano, semestre, mês, etc.	

Problema de acento, geralmente é encoding; Problema com campo decimal, geralmente é configuração regional. 

Defininição do problema de negócio> Preparação dos Dados> Modelagem dos Dados> Visualização dos Dados. 

Um dashboard é uma página única/ tela, que usa as visualizações para contar uma história.

BI é um conceito, é um conjunto de técnicas e ferramentas que permite que a organização utilize a análise das informações para o suporte a tomada de decisão. Quanto mais perto da área de negócios, maior a empregabilidade. 
-

qual fab. vende mais

vendas realizadas nos últimos 4 anos (período de 2012 a 2015)

criar um modelo de dados que permita a extração de relatórios a qualquer momento e que permita extrair dados por diferentes visões e ângulos.

data lake armazena os dados não estruturados

manipulação dos dados: correr atrás das informações ou o engenheiro de dados geralmente extrai e fornece os dados, sua função é acrescentar ou tirar colunas, analisar as informações, organizar as informações, etc. 

Perguntas para a Organização de Dados:

1) Posso levar os dados para o Power BI da forma que estão?
2) Quais são os requerimentos de organização dos dados?

3) Workflow: Como mantenho os dados em um formato de atualização sob demanda? (Não precisar extrair as informações todos os dias, deixar de uma forma que ela atualize). 

4) Como visualizar os dados por diferentes visões e ângulos?

Com o BI se organiza os dados primeiros e depois carrega. No Big Data se pega os dados no formato bruto, carregar e depois editar. 

Como definimos o melhor modelo de organização dos dados? Processo de negócio (exemplo: venda de produtos eletrônicos)> 
Definimos o nível de detalhamento (granularidade, exemplo: total de produtos mais vendidos por dia)>
Identificamos as dimensões necessárias(exemplo: fabricante, produto, loja, tempo)> 
Criamos o schema (modelo criado no DW ou no Power BI (mais simples). 

Dois modelos: Star Schema (mais simples) ou Snow Flake (mais detalhado). Também é possível se criar os dois. 

Resumo até aqui. 
Business Intelligenceé um conceito que envolve técnicas, ferramentas e procedimentos para transformar dados brutos em informação e conhecimento para os tomadores de decisão.O Power BI é uma ferramenta de Self-Service BI, cujo objetivo é permitir que pessoas sem conhecimentotécnico avançado possam realizar análises em dados.Para trabalhar de forma eficiente e profissional com o Power BI, pode ser necessário criar um  modelo  de  organização  dos  dados.  Esse  modelo  permite  realizar  análises  por  diferentes ângulos, sob demanda eorientada à solução dos problemas de negócio.Existem  2  modelos  principais  de  organização  dos  dados:  Star  Schema  e  SnowFlake.  Em ambos, o objetivo é criar uma estrutura de organização, que facilite a compreensão dos dados.Normalmente o modelo de dados é criado em um Data Warehouse (DW), um banco de dados  que  serve  de  fonte  para  processos  de  BI.  As  empresas  extraem  dados  de  sistemas transacionais, como CRM ou ERP, consolidam os dados e carregam no DW seguindo o modelo adotado. As ferramentas de BI podem conectar no DW e extrair os dados para análise.Nas  aulas  seguintes,  vamos  criar  um  modelo  Star  Schema  diretamente  no  Power  BI. Embora  o  Power  BI  não  seja  um  banco  de  dados,  ele  permite  criar  o  modelo  de  organização exatamente pelos fatores acima mencionados e por se tratar de uma solução de Self-Service BI.Para o Estudo  de Caso deste capítulo, um  modelo  Star Schema não seria obrigatório, e nosso objetivo aqui é demonstrar como isso pode ser feito no Power BI.

Star Schema (O objetivo é ter uma visão geral)

Cada fato acontece a partir da junção das dimensões.

Ferramentas para modelagem de dados: Erwin, Archi (gratuita) que possui o ArchiMate, SqlDBM, Toad, pgModeler, Enterprise data Modeler, Oracle, IBM 	InfoSphere Data Architect.

PK- Primary Key (Chave Primária)
FK - Foreign Key (Chave Estrangeira)

Sempre arquivar o que foi feito, manter a documentação: digitar o nome da dimensão, tipos de dados e colunas.

Duplicar as tabelas (sempre deixar a original) editar nome e escolher colunas

Exemplo: DIM_PRODUTO (ID PRODUTI, PRODUTO, CATEGORIA, SEGMENTO E FABRICANTE)
DIM_LOJA  (LOJA, CIDADE E ESTADO)
DIM_VENDEDOR (NOME DO VENDEDOR E ID VENDEDOR)
DIM_TEMPO (DATA DE VENDA)	


Pag inicial> selecionar a TB_fato> gerenciar relações> detecção automática> caso o power bi não consiga automaticamente, vamos fazer manualmente> criar um relacionamento> se nao der certo, os dados da tabela podem ser com problemas, ex: podem estar duplicados (estados, cidade, etc)> clicar na tabela> transformar datas> remover duplicatas de todas as tabelas> 

Exerc. Cap 03

Construir um dashboard que responda a estas perguntas:
1) Qual dos fabricantes dos produtos vendidos, apresenta melhor desempenho nas vendas?
2) Qual o valor total de vendas por estado e por categoria? Use um mapa. 
3) Qual o total de vendas por segmento?
4) Qual segmento tem maior influência no valor médio de venda? 
Criar uma análise de principais influenciadores e editar conforme a análise foi solicitada. Ex: neste caso é Analisar por: valor venda e Explicar por: Segmento.

Cap 04 - Modelagem

A cardinalidade é a forma pela qual implementamos os relacionamentos entre as tabelas. 
Um para muitos. Ex: um produto pode ser vendido várias vezes então o relacionamento é de um para muitos. (Cada produto é único. Cada produto pode ser vendido diversas vezes).
Um para Um. Ex: Geralmente Um vendedor pode ter apenas um registro. 
Muitos para Muitos. tb chamado de Filtro Cruzado, uma tabela que serve de ligação para outra tabela. Quando o power bi identifica o relacionamento automaticamente, é necessário sempre checar se está correto. 
Clicar em cima da linha e propriedades ou dar dois cliques para ir em editar relaciomento> (definir filtro cruzado na tabela do meio) Direção de filtro cruzado> Ambas. (fazer isso dos dois lados, nas duas tabelas, é mais seguro do que fazer o relacionamento direto entre duas tabelas). 
Para excluir o relacionamento, clica em cima da linha: excluir. 
Gerenciar relações para criar relações, tem a opçao de detectar automaticamente ou criar relacionamento. 
(Nem sempre o BI consegue relacionar da forma correta, sempre verificar se esta ok). 
Criar relacionamentos> selecionar as tabelas, ex: a tabela de produtos, depois a tabela de vendas. O BI identificou que a cardinalidade é de Um para Um, mas na verdade, com um produto pode se fazer mais de uma venda, entao seria necessario alterar de Um para Muitos. Nesse caso, nao colocar filtro cruzado para ambos, somente para Único. 

Criando medidas com DAX para média de vendas.
Para criar a média do valor de venda, é a média da coluna inteira> clicar na coluna inteira> Ferramentas de tabela> nova medida> na linha de fórmulas, average= cálculo de média e confirmar. Selecionar a média total de vendas, marcar a coluna de Produtos para ele apresentar a média de vendas por produtos. 
Media_vendas =  average(custos[valor de venda])

Cap. 05

Eixo data
valores media de venda

Ao criar a medida o bi entende que tem que somar, para alterar isso precisa clicar com o direito e alterar para: média ou o que for necessário.

Para criar uma nova coluna com grupos (ex: de faixa etária, faixa salarial, etc), ir em dados> ferramentas de colunas> editar conforme desejado. 

O comportamento do bi é criar resumos, dá para alterar também clicando com a direita e em: não resumir. 

Para conectar no Google Analytics> pag inicial> obter dados> serviços online> google analytics

ofuscar= encobrir os dados
