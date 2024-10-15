# Análise e Modelagem de Dados de E-commerce
## Descrição do Projeto
Este projeto visa estruturar e analisar dados de vendas de uma empresa de e-commerce, aplicando técnicas de limpeza e organização de dados (data cleaning e data wrangling). O objetivo é calcular as métricas RFM (Recência, Frequência e Ticket Médio) para os clientes e gerar gráficos para análise de vendas por mês, produtos e países.

## Dataset Utilizado
O dataset utilizado contém informações sobre compras realizadas em um e-commerce em 37 países. As principais colunas do dataset são:

- CustomerID: Código de identificação do cliente
- InvoiceNo: Código da fatura
- StockCode: Código do produto
- Description: Descrição do produto
- Quantity: Quantidade de produtos comprados
- InvoiceDate: Data da compra
- UnitPrice: Preço unitário do produto
- Country: País de onde a compra foi realizada

## Passos Realizados
### Passo 1: Carregamento e Análise Inicial
No primeiro passo, o dataset foi carregado no Google Colab. Utilizei as bibliotecas Pandas, NumPy, Seaborn e Matplotlib para a manipulação e visualização dos dados. Realizei uma análise inicial para entender a estrutura do dataset, verificar valores nulos e identificar possíveis outliers.

### Passo 2: Limpeza e Organização de Dados
Nesta etapa, limpei os dados removendo valores nulos, tratando outliers e criando novas colunas relevantes, como o valor total de cada pedido (TotalPrice). Também criei a coluna YearMonth para facilitar a análise de vendas mensais.

### Passo 3: Cálculo das Métricas RFM
Calculei as métricas RFM (Recência, Frequência e Ticket Médio) para cada cliente, com base nos dados de compras:

Recência (R): Tempo desde a última compra de cada cliente

Frequência (F): Quantidade total de compras realizadas

Ticket Médio (M): Média do valor gasto por pedido

### Passo 4: Análise Gráfica
Criei gráficos para visualizar os dados e insights obtidos:

Top 10 países com maior valor em vendas: Um gráfico de barras foi gerado para mostrar os 10 países que mais contribuíram em vendas.

Top 10 produtos mais vendidos: Outro gráfico de barras destacou os produtos mais vendidos.

Valor de vendas por mês: Um gráfico de linha mostrou a evolução das vendas ao longo dos meses.

Valor de vendas por mês e por país (Top 10 países): Visualizei a tendência das vendas ao longo dos meses, segmentada pelos 10 países com maior volume de vendas.

#### Resultados
Top 10 Países: Identificamos os países que mais geraram receita para o e-commerce.

Top 10 Produtos: Os produtos mais vendidos foram mapeados, permitindo otimizar o estoque.

Tendência de Vendas Mensais: Observamos variações no valor total de vendas ao longo dos meses, destacando períodos de alta e baixa.

Análise por País: Foi possível entender o desempenho de vendas segmentado pelos principais países, o que pode ajudar a ajustar campanhas de marketing e operações.

### Conclusão
Este projeto mostrou a importância da limpeza e organização dos dados para garantir uma análise precisa. As métricas RFM fornecem uma visão detalhada sobre o comportamento dos clientes, enquanto os gráficos gerados ajudaram a identificar padrões de vendas ao longo do tempo e em diferentes regiões.

