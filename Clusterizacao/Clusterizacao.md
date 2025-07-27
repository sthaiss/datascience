🧠 **Modelos de Clusterização** – Visão Geral
Clusterização (ou agrupamento) é uma técnica de aprendizado não supervisionado usada para identificar padrões e segmentar dados em grupos (clusters), onde os itens de um mesmo grupo são mais semelhantes entre si do que com os de outros grupos.

Ao contrário dos modelos supervisionados (que aprendem a partir de rótulos), a clusterização não utiliza uma variável-alvo. O objetivo é descobrir estruturas naturais ou ocultas nos dados, com base em alguma métrica de similaridade (ex: distância Euclidiana).

---

🔍 **Quando usar clusterização?**
Quando você não tem rótulos nos dados e quer explorar ou segmentar padrões.
Para análise exploratória de dados, redução de dimensionalidade, detecção de anomalias, segmentação de clientes ou produtos, etc.
Em problemas onde entender os grupos latentes ajuda a orientar decisões (ex: marketing, recomendação, agrupamento genético, imagens).

---

📌 ***Resumo***
“Clusterização é uma forma de aprendizado não supervisionado que agrupa dados com base em similaridade. Escolho o algoritmo com base na forma dos clusters, presença de ruído, e se preciso descobrir o número de grupos ou não. Em geral, uso K-Means como baseline, DBSCAN quando há ruído, e hierárquicos quando quero entender a estrutura global.”