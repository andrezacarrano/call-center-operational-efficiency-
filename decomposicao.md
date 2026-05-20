# Decomposição de Tarefas — Projeto Final CallMeMaybe

## 1. Identificação do Problema de Negócio

A CallMeMaybe é um serviço de telefonia virtual utilizado por empresas que dependem de operações de atendimento para lidar com clientes, parceiros e processos internos. A empresa está desenvolvendo uma nova funcionalidade que permitirá aos supervisores identificar operadores menos eficientes, com base em métricas operacionais.

Pesquisas do setor de atendimento, como relatado pela Zendesk, mostram que indicadores como taxa de chamadas perdidas, tempo de espera, resolução de problemas e satisfação do cliente são determinantes para a qualidade do serviço. Longos tempos de espera e chamadas não atendidas estão entre os principais fatores que reduzem a satisfação e aumentam o risco de churn.

Identificar operadores ineficientes permitirá:
- melhorar a qualidade do atendimento;
- reduzir perdas de chamadas;
- otimizar escala e distribuição de carga;
- orientar treinamentos e ações corretivas;
- aumentar a satisfação dos clientes corporativos.

---

## 2. Descrição dos Dados

### 2.1 Volume dos dados

Dataset principal (`telecom_dataset_us.csv`):
- 53.902 linhas
- 9 colunas

Dataset auxiliar (`telecom_clients_us.csv`):
- informações cadastrais dos clientes (user_id, plano, data de início)

### 2.2 Qualidade dos dados

- `internal`: 117 valores ausentes  
- `operator_id`: 8.172 valores ausentes  
- Demais colunas completas  
- Datas armazenadas como string  
- `operator_id` como float  
- Possíveis outliers em duração e volume de chamadas  
- Não há duplicatas aparentes (a confirmar)

### 2.3 Resumo estatístico

**Chamadas**
- Média: 16,45  
- Mediana: 4  
- Máximo: 4.817  

**Duração**
- `call_duration` média: 866,68 s  
- Mediana: 38 s  
- Máximo: 144.395 s  

- `total_call_duration` média: 1.157,13 s  
- Mediana: 210 s  
- Máximo: 166.155 s  

**Direção**
- Outbound: 31.917 registros  
- Inbound: 21.985 registros  

**Chamadas internas**
- False: 47.621  
- True: 6.164  
- NaN: 117  

**Chamadas perdidas**
- False: 30.334  
- True: 23.568  
→ Taxa de perda: 43,7%

### 2.4 Variáveis mais relevantes

- `is_missed_call` — indicador central de ineficiência  
- `total_call_duration` — inclui tempo de espera  
- `call_duration` — tempo efetivo de conversa  
- `direction` — separa inbound/outbound  
- `internal` — identifica chamadas internas  
- `calls_count` — volume de chamadas  
- `operator_id` — análise individual  
- `user_id` — análise por cliente  

---

## 3. Hipóteses a Serem Validadas

### H1 — Operadores ineficientes têm maior taxa de chamadas perdidas.
- H0: A taxa de chamadas perdidas é igual entre operadores.  
- H1: Alguns operadores têm taxa significativamente maior.

### H2 — Operadores ineficientes apresentam maior tempo de espera.
- H0: O tempo médio de espera é igual entre operadores.  
- H1: Operadores ineficientes têm tempo de espera maior.

### H3 — Operadores outbound ineficientes realizam menos chamadas ativas.
- H0: O volume de chamadas outbound é igual entre operadores.  
- H1: Alguns operadores fazem menos chamadas ativas.

### H4 — Chamadas internas e externas têm padrões diferentes de duração.
- H0: A duração média é igual entre chamadas internas e externas.  
- H1: Chamadas internas têm duração significativamente diferente.

---

## 4. Indicadores-Chave (KPIs)

### KPIs por operador
- Missed Call Rate = (missed calls / total calls)  
- Average Waiting Time = média de (total_call_duration − call_duration)  
- Outbound Activity = volume de chamadas de saída  
- Internal Call Ratio = (internal calls / total calls)

### KPIs por dia
- Total de chamadas por dia 
- Missed rate por dia 
- Tempo médio de espera por dia 

### KPIs por cliente
- Volume  
- Missed rate  
- Tempo médio de espera  

---

## 5. Ações a Executar

### 5.1 Limpeza e Processamento
- Converter `date` para datetime  
- Converter `operator_id` para inteiro  
- Tratar valores ausentes em `internal` e `operator_id`  
- Criar variáveis derivadas (ex.: waiting_time)  
- Remover ou tratar outliers extremos  
- Padronizar categorias (`direction`, `internal`)

### 5.2 Análise de Dados
- KPIs por operador  
- KPIs por dia 
- KPIs por cliente  
- Comparação inbound vs outbound  
- Análise de chamadas internas  
- Ranking de operadores  
- Visualizações (boxplots, histogramas, heatmaps)

### 5.3 Comunicação dos Resultados
- Relatório final CAR  
- Dashboard com KPIs  
- Tabelas e gráficos explicativos  
- Recomendações acionáveis

### 5.4 Estimativa de Tempo (2 semanas)
- Limpeza e preparação: 2 dias  
- EDA: 3 dias  
- KPIs e hipóteses: 3 dias  
- Testes estatísticos: 2 dias  
- Dashboard: 2 dias  
- Relatório final: 2 dias  

---

## 6. Stakeholders Impactados

- Supervisores de operação — monitoramento de desempenho  
- Gerentes de atendimento — decisões de escala e treinamento  
- Equipe de qualidade — auditoria e padrões de atendimento  
- Diretoria — visão estratégica e retenção de clientes  
- Clientes corporativos — impacto direto na qualidade do serviço  

