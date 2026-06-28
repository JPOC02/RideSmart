# Projeto Final — RideSmart: Modelagem e Análise de Rotas Urbanas

Este projeto, desenvolvido como parte da disciplina de **Algoritmos e Estruturas de Dados II (DCA3702)** da UFRN, explora a modelagem de rotas urbanas multimodais na cidade de Assú/RN utilizando teoria dos grafos.

## 📝 Descrição do Problema
O objetivo é otimizar o tempo de deslocamento entre um ponto de origem `A` e um destino `B`, permitindo que o usuário caminhe até um ponto de embarque `P` (respeitando uma distância máxima `X`). A rota é composta por:
1. **Caminhada:** A até P
2. **Deslocamento:** P até B (veículo)

O sistema analisa diferentes estratégias de busca para minimizar o tempo total, considerando trânsito sintético aplicado à malha viária.

## 🛠️ Tecnologias e Ferramentas
* **Linguagem:** Python
* **Grafos:** `NetworkX`
* **Geoprocessamento:** `OSMnx`
* **Visualização:** `Folium`, `Matplotlib`, `Seaborn`
* **Análise de Dados:** `Pandas`, `NumPy`

## 🚀 Algoritmos Implementados
O projeto compara a performance e eficiência de quatro algoritmos de caminho mínimo:
1.  **Dijkstra Simples:** Busca linear, base para comparação.
2.  **Dijkstra com Heap:** Versão otimizada utilizando fila de prioridade para melhor desempenho.
3.  **A* (Customizado):** Busca informada utilizando a distância geodésica como heurística.
4.  **Dijkstra Bidirecional:** Executa buscas simultâneas a partir da origem e do destino para reduzir a área de exploração.

## 📊 Resultados Principais
* **Performance:** O Dijkstra Bidirecional e o A* mostraram-se significativamente mais eficientes em cenários de longa distância, com um número reduzido de nós expandidos.
* **Impacto RideSmart:** A estratégia de caminhar até um ponto de embarque mais eficiente provou ser altamente eficaz em zonas centrais (ganho de até **24,5%** no tempo de viagem), enquanto o ganho em zonas residenciais foi marginal, dependendo da densidade da malha viária.

## 👥 Componentes do Grupo
* **João Paulo:** Criação do código e estruturação do repositório.
* **Gustavo Quezado:** Criação do código e redação do relatório.

## 📂 Estrutura do Repositório
* `/notebooks`: Contém o arquivo `AED2_projeto_final.ipynb` com toda a implementação.
* `/relatorio`: Contém o relatório final em PDF (`AED2.pdf`).
* `/images`: Gráficos gerados durante as simulações.
* `requirements.txt`: Arquivo que contem as versões das bibliotecas utilizadas na implementação do trabalho

---
*Relatório de Projeto Final apresentado à disciplina DCA3702, UFRN, Junho de 2026.*