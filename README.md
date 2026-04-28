Análise de Dados de Poluição do Ar Global (2025-2026)
Este repositório contém o código e os dados brutos utilizados para a análise de dados de poluição do ar global para os anos de 2025 e 2026.

Visão Geral do Projeto
O objetivo deste projeto é processar e analisar dados de poluição do ar de várias cidades ao redor do mundo, com foco em:

Limpeza e padronização dos dados.
Classificação da qualidade do ar (PM2.5) em categorias de saúde.
Extração de informações temporais detalhadas (dia, mês, ano, hora).
Conjunto de Dados
O conjunto de dados principal utilizado é Global_Air_Pollution_Data_2025_2026.csv, que inclui as seguintes colunas:

Date: Data e hora da medição.
City: Cidade onde a medição foi realizada.
Latitude, Longitude: Coordenadas geográficas.
PM2.5, PM10, NO2, SO2, CO, Ozone: Níveis de poluentes.
Aerosol_Optical_Depth: Profundidade Óptica de Aerossol.
AQI_Class: Classe do Índice de Qualidade do Ar.
Processamento de Dados (Pipeline)
O script pipeline realiza as seguintes etapas:

Backup: Cria uma cópia do DataFrame original (df_dados_raw).
Padronização de Nomes de Colunas: Converte todos os nomes de colunas para snake_case (minúsculas e espaços substituídos por underscores) para facilitar o acesso.
Classificação da Qualidade do Ar (PM2.5): Aplica regras de negócio para classificar os níveis de PM2.5 em categorias de saúde (e.g., 'Boa', 'Moderado', 'Insalubre').
Conversão de Data/Hora: Converte a coluna Date para o tipo datetime e cria uma nova coluna timestamp.
Extração de Componentes de Data/Hora: Extrai dia, mês, ano, data (apenas data) e hora da coluna timestamp.
O resultado final do processamento é salvo em dados_poluicao.csv.

Visualizações
Para a exploração e visualização dos dados, utilizei o Looker Studio. Foram criados dashboards interativos para exibir as tendências de poluição, a distribuição da qualidade do ar por cidade e outros insights relevantes.# Dados_poluicao_2025_2026
