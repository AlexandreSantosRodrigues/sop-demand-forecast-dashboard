# S&OP Demand Forecast Dashboard

Dashboard analítico desenvolvido para simular uma rotina de **Sales & Operations Planning (S&OP)**, com foco em **previsão de demanda, comparação entre vendas realizadas e forecast e análise da acurácia do planejamento**.

O projeto utiliza uma base fictícia de vendas de três linhas de lubrificantes ao longo de 24 meses e transforma os dados em indicadores e visualizações executivas no **Looker Studio**.

> **Nota:** todos os dados utilizados neste projeto são fictícios e foram criados exclusivamente para fins de estudo e portfólio.

---

## Dashboard

🔗 **[Acessar o Dashboard no Looker Studio](https://datastudio.google.com/reporting/bf13f866-7db9-4c08-86ca-528ba5f16281)**

---

## Objetivo

Simular um cenário de planejamento de demanda no qual a área de S&OP precisa acompanhar:

- Demanda prevista;
- Venda realizada;
- Desvios entre forecast e realizado;
- Forecast Accuracy;
- WAPE;
- Performance por linha de produto.

O objetivo é transformar os dados históricos em informações que possam apoiar o acompanhamento do planejamento e a tomada de decisão.

---

## Contexto do projeto

O projeto foi desenvolvido utilizando como cenário uma operação fictícia de **lubrificantes**, considerando três linhas de produtos e um histórico mensal de vendas.

A estrutura foi pensada para representar uma situação em que o planejamento precisa responder perguntas como:

> Quanto foi previsto para o período?

> Quanto realmente foi vendido?

> Qual foi o desvio entre o planejado e o realizado?

> Qual linha de produto apresentou maior aderência ao forecast?

> Em quais períodos o erro de previsão aumentou?

---

## Tecnologias utilizadas

| Tecnologia | Utilização |
|---|---|
| **Google Sheets** | Armazenamento e organização da base |
| **Looker Studio** | Dashboard e visualização dos indicadores |
| **Forecasting** | Modelo simples de previsão de demanda |
| **Data Analysis** | Análise dos desvios entre forecast e realizado |
| **Business Intelligence** | Construção de indicadores para apoio à decisão |

---

## Estrutura dos dados

A base possui:

- **24 meses** de histórico;
- **3 linhas de produtos**;
- **72 registros**;
- Volume de vendas em litros;
- Forecast mensal;
- Venda real;
- Indicadores de erro e acurácia.

### Campos principais

```text
Mês/Ano
Linha de Produto
Previsão de Vendas (Litros)
Venda Real (Litros)
Forecast Accuracy (%)
```

---

## Modelo de Forecast

Para simular a previsão de curto prazo, foi utilizado um modelo simples de **média móvel ponderada**, considerando os três períodos anteriores.

### Fórmula

```text
Forecast =
50% × mês anterior
+
30% × dois meses atrás
+
20% × três meses atrás
```

---

## Métricas

### Erro Absoluto

```text
Erro Absoluto =
ABS(Venda Real - Forecast)
```

### WAPE

O **Weighted Absolute Percentage Error (WAPE)** mede o erro do forecast considerando o peso do volume realizado.

```text
WAPE =
SUM(Erro Absoluto)
/
SUM(Venda Real)
```

Quanto menor o WAPE, menor o erro ponderado do forecast.

### Forecast Accuracy

```text
Forecast Accuracy =
1 - WAPE
```

---

## Dashboard

O dashboard foi estruturado para responder rapidamente às principais perguntas de acompanhamento da demanda.

### KPIs

- **Venda Real**
- **Previsão de Vendas**
- **Forecast Accuracy**
- **WAPE**

### Visualizações

#### 1. Venda Real × Previsão

Gráfico temporal comparando o volume efetivamente vendido com o volume previsto.

#### 2. Forecast Accuracy por Linha

Comparação da acurácia do forecast entre as diferentes linhas de produto.

#### 3. Real × Forecast por Linha

Comparação do volume realizado e previsto por linha de produto.

#### 4. Tabela de Performance

Tabela consolidando:

```text
Linha de Produto
Venda Real
Forecast
Erro Absoluto
Forecast Accuracy
```

---

## Principais perguntas de negócio

O dashboard foi construído para permitir análises como:

1. Qual foi o volume total vendido no período?
2. Qual foi o volume previsto?
3. Qual foi a aderência do forecast ao realizado?
4. Qual linha apresentou maior desvio?
5. Como a acurácia se comportou entre as linhas de produto?
6. Em quais períodos ocorreram maiores diferenças entre forecast e vendas reais?

---

## Fluxo do projeto

```text
Histórico de vendas
        ↓
Organização da base
        ↓
Modelo de Forecast
        ↓
Comparação Forecast × Real
        ↓
Cálculo de Erro / WAPE
        ↓
Forecast Accuracy
        ↓
Dashboard no Looker Studio
        ↓
Análise de desvios
        ↓
Apoio à tomada de decisão
```

---

## Resultado

O projeto demonstra a aplicação de conceitos de:

- **Sales & Operations Planning (S&OP)**
- **Demand Planning**
- **Forecasting**
- **Business Intelligence**
- **Data Analysis**
- **Data Visualization**
- **KPI Design**
- **Performance Analysis**

Mais do que apresentar gráficos, o objetivo foi construir uma visão orientada a perguntas de negócio, conectando **dados históricos → previsão → realizado → erro → indicador → análise**.

---

## Próximos passos

Possíveis evoluções do projeto:

- Inclusão de histórico maior;
- Comparação entre diferentes modelos de previsão;
- Inclusão de sazonalidade;
- Análise de tendência;
- Forecast por segmento;
- Indicadores de viés do forecast;
- Integração com outras fontes de dados;
- Automatização da atualização da base;
- Alertas para grandes desvios.

---

## Autor

**Alexandre Santos**

Projeto desenvolvido para fins de estudo e portfólio, com foco em **Data Analytics, Business Intelligence e aplicação de dados a problemas de negócio**.

---


