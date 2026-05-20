# CallMeMaybe — Análise de Eficiência Operacional do Call Center

Este projeto apresenta uma análise completa da eficiência operacional de um call center, com foco na identificação de gargalos, operadores críticos e oportunidades de melhoria no atendimento.

---

## 🎯 Objetivo

Avaliar o desempenho operacional das chamadas e identificar os principais fatores de ineficiência, com base em:

* taxa de chamadas perdidas
* tempo de espera
* comportamento inbound vs outbound
* desempenho individual dos operadores

A análise busca apoiar decisões para melhoria da experiência do cliente e otimização da operação.

---

## 📊 Principais entregas

* Construção de KPIs operacionais (volume, taxa de outbound, duração média)
* Criação de um **score de ineficiência** baseado em múltiplos fatores
* Identificação dos operadores mais críticos
* Análise comparativa entre diferentes tipos de chamadas
* Validação estatística das hipóteses com testes de significância
* Dashboard interativo no Tableau

---

## 📁 Estrutura do projeto

* `callmemaybe.ipynb` — análise completa (EDA, KPIs e modelagem do score)
* `telecom_dataset_new.csv` — base principal de chamadas
* `telecom_clients.csv` — dados complementares de clientes
* `kpi_ops_final.csv` — dataset consolidado com métricas por operador
* `df_calls_exportado_do_notebook.csv`, `df_ops_exportado_do_notebook.csv` — bases tratadas

---

## ▶️ Como executar

1. Abra o notebook `callmemaybe.ipynb` em Jupyter Notebook ou JupyterLab
2. Execute as células em sequência
3. Garanta que os arquivos CSV estejam no mesmo diretório

---

## 🔗 Visualizações

* 📊 Dashboard Tableau: https://public.tableau.com/views/AnlisedeIneficinciaOperacionaldoCallCenter/Dashboard1?:language=pt-BR&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
* 📄 Relatório CAR: https://drive.google.com/drive/folders/17Zlbq1LWB6XZPcSDyg5hTgnFHx8gOFYd?usp=sharing

---

## 🧠 Tecnologias utilizadas

* Python (pandas, numpy)
* Visualização: matplotlib, seaborn
* Estatística: scipy
* BI: Tableau

---

## 📌 Principais insights

* A ineficiência operacional está fortemente associada à **alta taxa de chamadas perdidas** e ao **tempo de espera elevado**
* Operadores com maior score de ineficiência apresentam desempenho significativamente inferior
* A atividade outbound não demonstrou impacto relevante na diferenciação de performance

---

## 🚀 Conclusão

Os resultados indicam oportunidades claras de melhoria operacional, especialmente na redução de perdas e otimização do tempo de espera, fatores diretamente ligados à experiência do cliente e eficiência do atendimento.
