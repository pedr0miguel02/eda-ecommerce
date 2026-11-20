# Análise de um e-commerce de equipamento outdoor

Projeto de análise de dados em Python (Jupyter Notebook) que percorre as quatro fases de uma análise: **recolha → limpeza → análise exploratória (EDA) → conclusões**.

## Dados

Os dados foram obtidos no **Kaggle**. São 7 tabelas em CSV de uma loja online de equipamento outdoor, com encomendas de janeiro de 2024 a setembro de 2026:

| ficheiro | conteúdo |
|---|---|
| `customers.csv` | clientes (país, nível de fidelização…) |
| `products.csv` | produtos (categoria, marca, preço, custo…) |
| `orders.csv` | encomendas (data, estado, canal, valores) |
| `order_items.csv` | produtos dentro de cada encomenda |
| `payments.csv` | pagamentos |
| `shipments.csv` | envios |
| `returns.csv` | devoluções |

Os ficheiros de dados não estão incluídos neste repositório.

## Como correr

1. Descarregar o dataset do Kaggle e colocar os 7 ficheiros CSV na mesma pasta do notebook.
2. Instalar as bibliotecas:
   ```bash
   pip install -r requirements.txt
   ```
3. Abrir o notebook:
   ```bash
   jupyter notebook analise_ecommerce.ipynb
   ```

## Estrutura do notebook

1. **Recolha:** leitura dos 7 CSV e primeiro olhar sobre os dados.
2. **Limpeza:** valores em falta, duplicados, tipos de dados, valores inválidos, consistência entre tabelas e outliers.
3. **Análise exploratória:** 12 secções (tempo, estado das encomendas, canais, produtos, clientes, pagamentos, envios, devoluções, descontos e correlações), com 23 gráficos.
4. **Conclusões e recomendações.**

## Principais conclusões

- **48 milhões de dólares em vendas**, com um crescimento de 20–25% por ano, que vem sobretudo do aumento do número de encomendas.
- **Novembro e dezembro vendem quase o dobro** de um mês normal.
- **As vendas estão concentradas:** Tents, Backpacks e Navigation valem 51% das vendas, e 20% dos produtos valem 72%.
- **A margem bruta é de 48%.** Os pontos fracos são a categoria Footwear (42%) e a marca Stonebrook (43%).
- **Os clientes são fiéis** (83% voltam a comprar), mas não há clientes novos registados desde 2024.
- **O programa de fidelização e os descontos não mudam o comportamento** dos clientes.
- **As perdas são moderadas:** 6,5% das encomendas são canceladas (29% delas por pagamentos falhados) e 4,3% dos produtos são devolvidos.
- **Os canais, os pagamentos e os envios comportam-se todos de forma igual.**
- Vários padrões pouco realistas (por exemplo, horas e prazos uniformes) sugerem que os dados são simulados.

## Ferramentas

Python · pandas · NumPy · matplotlib · seaborn · Plotly · squarify · PyWaffle · pypalettes · Jupyter
