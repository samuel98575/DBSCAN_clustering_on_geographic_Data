# Clustering DBSCAN em Dados Geográficos de Logística

Este projeto apresenta uma análise exploratória e técnica de um dataset de logística (entregas) na Índia, focado na identificação de padrões espaciais, limpeza de anomalias geográficas e validação de estratégias de entrega *Last-Mile*.

## 1. Volume e Qualidade da Base
O dataset de entregas conta com **43.739 registros**, apresentando uma estrutura sólida de dados numéricos (`float64`) e ausência total de valores nulos (NaN). Contudo, a integridade "visual" da base esconde inconsistências geográficas críticas. A análise estatística das coordenadas revelou que a Índia situa-se inteiramente no Hemisfério Norte (acima de $8^\circ$ N), mas registros com latitudes de -30.90 evidenciam erros de input. Além disso, cerca de **3.693 registros (8,4%)** localizam-se em áreas oceânicas ou possuem coordenadas próximas a zero, que atuariam como distorções em algoritmos de clustering.

## 2. Diagnóstico de Mercado e Hubs Econômicos
A análise demonstra um domínio claro dos hubs econômicos, com concentração estratégica nos estados de **Maharashtra e Karnataka** (mais de 6.000 entregas cada). Isso reflete a importância de Mumbai e Bengaluru como centros financeiros e tecnológicos. 

A rede logística mostra-se perfeitamente alinhada à densidade demográfica: as Top 10 cidades possuem populações entre 8 e 12 milhões de habitantes, e a proximidade entre os pontos de origem e destino confirma uma operação de **baixa distância radial**. Isso valida a hipótese de fluxos predominantemente intramunicipais e uma estratégia de *Last-Mile* altamente capilarizada.

## 3. Dinâmica de Demanda e Centros Médios
Um *insight* crucial revelado pela escala logarítmica é a não linearidade da demanda. Identificamos um cluster de cidades de médio porte (entre $10^5$ e $10^6$ habitantes) com volumes de entrega que rivalizam com grandes metrópoles. Observamos que cidades com perfis demográficos similares apresentam volumes distintos, indicando que a infraestrutura local e a proximidade de centros de distribuição impactam o sucesso operacional mais do que apenas o contingente populacional.

## Tecnologias Utilizadas
* **Python:** Processamento e análise de dados.
* **Pandas & NumPy:** Manipulação estatística.
* **Matplotlib & Seaborn:** Visualização de dados (Escala Logarítmica e Dispersão).
* **DBSCAN:** Algoritmo de clustering para identificação de padrões geográficos.

---
*Este projeto faz parte de um estudo sobre otimização logística e tratamento de dados geoespaciais.*
