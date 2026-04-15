# CallMeMaybe — Análise de Desempenho Operacional

Este repositório contém a análise de desempenho operacional da CallMeMaybe com base em dados de chamadas.

## 🎯 Objetivo

O notebook `callmemaybe.ipynb` analisa a qualidade dos dados, a performance de atendimento, os padrões de chamadas inbound/outbound e a eficiência dos operadores. A análise inclui:

- verificação e limpeza dos dados
- criação de indicadores operacionais (KPIs)
- segmentação de chamadas internas e externas
- identificação de operadores com melhor e pior desempenho
- construção de um score de ineficiência
- testes estatísticos para validar diferenças entre grupos

## 📊 Principais Insights
- A ineficiência está concentrada na perda de chamadas e no tempo de espera
- Operadores críticos apresentam desempenho significativamente inferior
- A atividade outbound não impacta significativamente a performance

## 📁 Estrutura do projeto

- `callmemaybe.ipynb` — notebook principal com a análise completa
- `telecom_dataset_new.csv` — dados das chamadas
- `telecom_clients.csv` — informações de clientes relacionadas
- `decomposicao.md` — material auxiliar de decomposição (se aplicável)
- `df_calls_exportado_do_notebook.csv`, `df_ops_exportado_do_notebook.csv`, `kpi_ops_final.csv` — arquivos de exportação gerados pelo notebook

## ▶️ Como usar

1. Abra `callmemaybe.ipynb` no Jupyter Notebook ou JupyterLab.
2. Execute as células na ordem apresentada.
3. Certifique-se de que os arquivos CSV estão no mesmo diretório do notebook.

## 🔗 Links importantes

- Link do relatório CAR: (https://public.tableau.com/views/AnlisedeIneficinciaOperacionaldoCallCenter/Dashboard1?:language=pt-BR&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)
- Link do Dashboard no Tableau: (https://drive.google.com/drive/folders/17Zlbq1LWB6XZPcSDyg5hTgnFHx8gOFYd?usp=sharing)

## 📝 Observações

- As análises foram feitas com `pandas`, `numpy`, `matplotlib`, `seaborn` e `scipy`.
- Se necessário, atualize os caminhos dos dados no notebook caso os arquivos sejam movidos.
- O README está formatado para ser compatível com o fluxo do notebook e para registrar facilmente os links finais de relatório e dashboard.
