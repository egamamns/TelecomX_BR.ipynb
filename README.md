# TelecomX_BR.ipynb
Projeto: Análise de Evasão de Clientes (Churn) – TelecomX
Introdução

Este projeto tem como objetivo analisar dados de clientes da empresa fictícia TelecomX para entender melhor o fenômeno de evasão de clientes (churn). O cancelamento de contratos por parte dos clientes é um dos maiores desafios para empresas de telecomunicações, pois impacta diretamente a receita e o crescimento sustentável do negócio.

Através da análise exploratória de dados (EDA), limpeza e transformação de variáveis, além da criação de métricas adicionais, buscamos identificar padrões e fatores que contribuem para o cancelamento, permitindo sugerir estratégias de retenção de clientes.

Conjunto de Dados

Os dados foram disponibilizados em formato JSON e contêm informações sobre o perfil demográfico dos clientes, serviços contratados, faturamento mensal e total, além do status de churn.

Etapas do Projeto
1. Extração de Dados

Carregamento do dataset a partir de um arquivo JSON remoto (GitHub) ou local.

Normalização dos dados para formato tabular com pandas.

2. Transformação e Limpeza

Conversão de colunas para tipos de dados adequados (numéricos e categóricos).

Remoção de registros duplicados e inconsistentes.

Exclusão de registros com variável alvo (Churn) ausente.

Preenchimento de valores faltantes em Charges.Total utilizando Monthly * tenure.

Padronização de categorias redundantes como "No phone service" e "No internet service".

Criação de uma nova métrica: Contas_Diarias, obtida a partir de Charges.Monthly / 30.

3. Análise Exploratória (EDA)

Estatísticas descritivas das variáveis numéricas.

Distribuição de clientes com e sem churn.

Proporções de churn por variáveis categóricas, como tipo de contrato, método de pagamento e gênero.

Análise das distribuições de variáveis numéricas (tenure, Charges.Total, Charges.Monthly, Contas_Diarias) entre clientes que permaneceram e os que cancelaram.

Cálculo de relevância das variáveis para churn por meio da métrica de Informação Mútua.

4. Relatório Final

Documentação das etapas de limpeza e transformação.

Visualizações para explorar padrões e diferenças entre clientes com e sem churn.

Principais conclusões extraídas da análise.

Recomendações práticas para reduzir a evasão de clientes.

Conclusão:

Clientes com contratos de curto prazo e menor tempo de relacionamento (tenure baixo) apresentam maior probabilidade de churn.

O valor total gasto e a forma de pagamento estão associados ao comportamento de evasão.

Contratos mensais e pagamentos eletrônicos específicos apresentam taxas de churn mais elevadas.

A métrica de faturamento diário (Contas_Diarias) auxilia no acompanhamento granular do comportamento dos clientes.


Tecnologias Utilizadas:
Python 3
Pandas
NumPy
Matplotlib
Jupyter Notebook
