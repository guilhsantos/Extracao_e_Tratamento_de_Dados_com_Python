🇧🇷 **Português** · [🇺🇸 English](README.en.md)

# Limpeza de dados e RFM de clientes de e-commerce

Tratamento de uma base real de vendas de e-commerce em 37 países e cálculo da RFM (recência, frequência e ticket médio) de cada cliente, pronta para segmentação.

[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/guilhsantos/Extracao_e_Tratamento_de_Dados_com_Python/blob/main/DataPreparationnapratica.ipynb)

## Problema

A base bruta tinha clientes sem identificação, preços zerados e quantidades negativas (devoluções e descontos). Qualquer análise feita sobre ela mostraria números errados.

## Solução

Um pipeline em pandas que limpa a base, cria as colunas de valor do pedido e de mês, calcula a RFM por cliente e gera os gráficos de vendas.

## Resultado

- **Tabela RFM por cliente** exportada em `e-commerce_RFM.csv`. Exemplo: o cliente 12347 comprou há 1 dia, tem 182 compras e ticket médio de 23,68.
- **Top 10 países** em faturamento e **top 10 produtos** mais vendidos.
- **Evolução mensal das vendas**, no geral e por país, mostrando os picos e vales do ano.

## Como fiz

1. Carga e inspeção: nulos, preços ≤ 0 e quantidades ≤ 0.
2. Limpeza: remoção de nulos, devoluções e outliers.
3. Novas colunas: `TotalPrice` (quantidade × preço) e `YearMonth`.
4. RFM por cliente: dias desde a última compra, número de compras e valor médio por pedido.
5. Gráficos de barras e linhas com Seaborn e Matplotlib.

## Próximo passo

Clusterizar os clientes sobre essa RFM. A primeira versão da segmentação, feita por compra, está em [RFV_Analysis_Clustering](https://github.com/guilhsantos/RFV_Analysis_Clustering).

## Stack

Python · pandas · NumPy · Seaborn · Matplotlib · Google Colab

---

Feito por [Guilherme Santos](https://portifolio-guilherme-santos.vercel.app) · [LinkedIn](https://www.linkedin.com/in/guilherme-santos-dataeng)
