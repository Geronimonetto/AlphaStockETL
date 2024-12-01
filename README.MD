# **Insights dos Dados das Ações**

## **ETL - Processo de Extração, Transformação e Carga (ETL)**

Neste projeto, o principal foco foi a criação de um pipeline ETL (Extração, Transformação e Carga) para processar e analisar dados de ações de empresas como **Apple (AAPL)**, **Microsoft (MSFT)** e **Google (GOOG)**. O objetivo é coletar, transformar e carregar os dados de forma eficiente para análise de insights e geração de visualizações. Abaixo estão os detalhes do processo:

### **1. Extração**
Os dados de ações foram extraídos de fontes financeiras confiáveis, como APIs de mercado de ações. As informações coletadas incluem preços de fechamento, abertura, máxima, mínima, volume negociado e outras variáveis pertinentes.

### **2. Transformação**
- **Limpeza de Dados:** Remoção de dados faltantes ou inconsistentes.
- **Cálculo de Métricas:** Durante o processo de transformação, várias métricas foram calculadas, como a variação diária de preços (high - low), volume médio negociado, e média móvel de 7 dias para identificar tendências.
- **Formatação de Dados:** Os dados foram estruturados para permitir análise eficiente, convertendo as informações em formatos adequados para modelos de machine learning ou análise estatística.

### **3. Carga**
Após a transformação, os dados foram carregados em um banco de dados **SQLite**, onde foram organizados para facilitar consultas rápidas. A carga também incluiu o armazenamento de métricas agregadas (como o preço médio anual de fechamento e volume médio de ações).

Com esse processo ETL, o projeto foi capaz de gerar insights detalhados sobre a volatilidade, volume de negociação, correlação de preços e tendências de ações, fornecendo informações valiosas para investidores e analistas financeiros.

---

## **Insights dos Dados das Ações**

### **1. Variação Diária de Preços (high - low)**
#### **Insight:**
A variação diária de preços identifica os dias com maior volatilidade, que podem estar relacionados a anúncios financeiros, resultados trimestrais ou eventos econômicos significativos.

#### **Resultado:**
Nos dias de maior volatilidade:
- A **Apple (AAPL)** teve uma variação máxima de **$184,31**, destacando-se pela maior oscilação entre as ações analisadas.
- A **Google (GOOG)** apresentou variações significativas de até **$165,45**, enquanto a **Microsoft (MSFT)** teve uma volatilidade relativamente menor.
- A análise sugere que a **Apple** e a **Google** foram mais suscetíveis a eventos extremos.

---

### **2. Volume Médio por Ação**
#### **Insight:**
O volume médio é um indicador de liquidez e interesse do mercado nas ações. Maiores volumes médios indicam maior atividade e liquidez.

#### **Resultado:**
- **Apple (AAPL):** Média de **33,171,430** ações negociadas por dia.
- **Microsoft (MSFT):** Média de **45,086,740** ações, apresentando o maior volume médio entre as ações.
- **Google (GOOG):** Média de **6,453,363** ações.
- A **Microsoft** se destaca pela maior liquidez, enquanto a **Google** tem o menor volume, indicando menor atividade de negociação.

---

### **3. Preço Médio de Fechamento por Ano e por Ação**
#### **Insight:**
O preço médio de fechamento por ano revela tendências de valorização ou desvalorização ao longo do tempo, sendo útil para investidores de longo prazo.

#### **Resultado:**
- **Apple:** Crescimento de preços consistente ao longo dos anos, com o preço médio em **2023** atingindo **$156,50** (+7,4%).
- **Microsoft:** Apresentou o maior aumento percentual em **2023**, com média de **$325,80** (+9,2%).
- **Google:** Valorização mais tímida, com média de **$2810,20** em **2023** (+2,2%).
- Os dados mostram que a **Microsoft** tem o crescimento mais robusto, enquanto a **Apple** também apresenta bom desempenho.

---

### **4. Correlação entre Preço de Abertura e Fechamento**
#### **Insight:**
A correlação próxima de 1 sugere alta estabilidade nos preços diários, com pequenas variações entre a abertura e o fechamento.

#### **Resultado:**
- **Apple (AAPL):** Correlação de **0,9997**, indicando alta estabilidade.
- **Microsoft (MSFT):** Correlação de **0,9998**, apresentando a maior estabilidade entre as ações.
- **Google (GOOG):** Correlação de **0,9997**.
- Todas as ações têm forte correlação, com a **Microsoft** liderando em consistência.

---

### **5. Análise de Tendência com Médias Móveis**
#### **Insight:**
A média móvel de 7 dias suaviza flutuações diárias e identifica tendências de curto prazo. Ela é útil para prever movimentos futuros.

#### **Resultado:**
Para a **Apple (AAPL)**, a média móvel sugere uma tendência de alta no período recente:
- Em **14/11/2024**, a média foi de **$228,13**.
- Em **13/11/2024**, a média foi de **$227,45**, mostrando um crescimento gradual.
- Essa tendência positiva reflete potencial valorização no curto prazo para a **Apple**.

---

### **Conclusão Geral:**
Esses insights mostram padrões de volatilidade, liquidez e crescimento nas ações, além de identificar tendências futuras. Com essas informações, investidores podem tomar decisões mais informadas, como:
- Investir em ações mais estáveis (ex.: Microsoft).
- Explorar tendências de alta (ex.: Apple).
- Monitorar eventos que impactem volatilidade (ex.: Google).

---

## **Perguntas para Insight**

### **1. Dias com Maior Variação Diária de Preços (Volatilidade):**
- Quais são os dias em que a volatilidade foi mais alta para cada ação?
- Que eventos podem ter causado essas variações extremas nos preços?
- Há padrões específicos de volatilidade (como meses ou anos com maior frequência de picos)?
- Quais ações apresentam maior volatilidade em comparação às outras?

### **2. Volume Médio Negociado por Ação:**
- Qual ação tem o maior volume médio de negociação? Isso reflete maior liquidez?
- O volume médio por ação é consistente ao longo dos anos ou varia significativamente?
- Quais fatores (notícias, lançamentos de produtos, resultados financeiros) influenciam o volume negociado de cada empresa?
- Existe alguma relação entre o volume de negociação e o preço da ação?

### **3. Preço Médio de Fechamento por Ano e por Ação:**
- Como os preços médios de fechamento mudaram ao longo dos anos para cada ação?
- Alguma ação apresenta crescimento mais rápido em comparação com as outras?
- Quais períodos (anos) foram mais lucrativos para os investidores de cada ação?
- Existe uma correlação entre o desempenho de uma ação e eventos externos, como crises ou avanços tecnológicos?

### **4. Correlação entre Preços de Diferentes Ações:**
- Existe alguma correlação entre os preços de fechamento das ações analisadas?
- Como a movimentação de uma ação (ex.: AAPL) pode influenciar outras do setor, como MSFT ou GOOG?
- A correlação é consistente ao longo dos anos, ou há períodos em que ela aumenta/diminui?

### **5. Tendências de Alta e Baixa no Preço de Fechamento:**
- Quais foram os anos de maior valorização ou desvalorização para cada ação?
- Qual é o padrão de tendência (alta ou baixa) para cada ação em diferentes períodos?
- A performance das ações é cíclica, ou há anos consecutivos de crescimento/queda?
- A tendência de crescimento reflete mudanças no mercado ou avanços específicos nas empresas?

