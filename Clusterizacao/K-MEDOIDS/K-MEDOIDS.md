🧠 **K-Medoids (Clustering)**

**K-Medoids é um algoritmo de clustering não supervisionado**, parecido com o K-Means, mas em vez de usar a média dos pontos para representar cada cluster, ele usa um **medoide** — o ponto real mais central do cluster.

---

🧩 **Como funciona**

1. Inicializa com K medoids (pontos centrais reais).
2. Atribui cada ponto ao cluster cujo medoide é mais próximo (distância).
3. Para cada cluster, seleciona o ponto que minimiza a soma das distâncias intra-cluster como novo medoide.
4. Repete os passos até que os medoides não mudem mais ou alcance o número máximo de iterações.

---

⚙️ **Hiperparâmetros principais**

* `n_clusters (K)`: número de clusters.
* `max_iter`: número máximo de iterações.
* **Métrica de distância**: pode ser Euclidiana, Manhattan, etc.

---

📏 **Pré-processamento essencial**

* **Sensível à escala dos dados** → padronização ou normalização recomendada.
* **Mais robusto a outliers que K-Means**, pois usa pontos reais como centros.
* Não lida com valores ausentes → imputação necessária.

---

📊 **Métricas de avaliação (clustering)**

* Soma das distâncias intra-cluster.
* Silhouette Score.
* Davies-Bouldin Index, Calinski-Harabasz Score.

---

✅ **Vantagens**

* Mais **robusto a outliers** que K-Means.
* Pode usar qualquer métrica de distância.
* Utiliza pontos reais como centros, facilitando interpretação.

---

⚠️ **Desvantagens**

* Computacionalmente **mais caro que K-Means** (calcula distâncias de vários pontos).
* Pode ser lento em grandes bases de dados.
* Requer definição prévia de K.
* Não lida com valores ausentes diretamente.

---

⚙️ **Desempenho computacional**

* Mais lento que K-Means, especialmente em bases grandes.
* Pode precisar de otimizações (ex: PAM, CLARA) para escalabilidade.

---

📌 **Quando aplicar**

* Quando os dados possuem **outliers** que podem prejudicar K-Means.
* Quando a **interpretação por pontos reais** como centroide é importante.
* Em datasets de tamanho pequeno a médio.

