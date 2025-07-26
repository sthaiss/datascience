🧠 **K-Means (Clustering)**

**K-Means é um algoritmo não supervisionado** que agrupa os dados em **K clusters (grupos)** com base na **similaridade** (geralmente distância Euclidiana). O objetivo é **minimizar a variância intra-cluster** (distância dos pontos ao centroide do grupo).

---

🧩 **Como funciona**

1. Define **K centroides iniciais** (aleatórios ou por método como K-Means++).
2. Atribui cada ponto ao **cluster mais próximo** com base na distância.
3. Recalcula os centroides como **média dos pontos de cada cluster**.
4. Repete os passos 2 e 3 até convergir (sem mudanças relevantes nos grupos).

---

⚙️ **Hiperparâmetros principais**

* `n_clusters (K)`: número de clusters desejado.
* `init`: método de inicialização (`random`, `k-means++`).
* `max_iter`: número máximo de iterações.
* `n_init`: quantas vezes o algoritmo será rodado com diferentes inicializações.
* `tol`: tolerância para convergência.

---

📏 **Pré-processamento essencial**

* **Altamente sensível à escala dos dados** → **padronizar ou normalizar** é fundamental.
* **Não lida com valores ausentes** → imputação necessária.
* **Sensível a outliers**, que podem puxar centroides.
* K-Means assume **variância esférica** (dados em clusters de forma circular/similar tamanho).

---

📊 **Métricas de avaliação (clustering)**

* **Inércia** (soma das distâncias intra-cluster) – usada internamente.
* **Silhouette Score** – avalia separação e coesão dos clusters.
* **Davies-Bouldin Index**, **Calinski-Harabasz Score**.
* **Validação cruzada não se aplica diretamente**, mas técnicas como **elbow method** ou **gap statistic** ajudam a definir K ideal.

---

✅ **Vantagens**

* **Simples, rápido e fácil de interpretar**.
* **Escalável para grandes volumes de dados**.
* Funciona bem quando os clusters têm **forma aproximadamente esférica**.
* Razoável para **segmentação inicial** ou **exploração de padrões**.

---

⚠️ **Desvantagens**

* Requer definição de **K (número de clusters)** antecipadamente.
* **Sensível a outliers e inicialização aleatória**.
* Supõe clusters de **tamanho e forma semelhantes** (pode falhar com formatos complexos).
* **Não garante solução ótima global** (solução pode depender da inicialização).
* **Não lida com valores ausentes** diretamente.

---

⚙️ **Desempenho computacional**

* **Muito eficiente** para datasets grandes e de baixa/média dimensionalidade.
* Treinamento é rápido, mas pode demorar se `K` ou `n_init` forem grandes.
* Escala bem com paralelização e versões otimizadas (ex: MiniBatchKMeans).

---

📌 **Quando aplicar**

* Quando você precisa **segmentar dados sem rótulos**.
* Em análises exploratórias, como **segmentação de clientes**, **agrupamento de produtos**, etc.
* Quando há **suspeita de padrões naturais nos dados** e é necessário descobri-los.
* Quando os dados são **padronizados** e você pode assumir clusters com forma esférica.

