🧠 **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**

**DBSCAN é um algoritmo de clustering não supervisionado baseado em densidade**, que identifica grupos como regiões densas separadas por regiões esparsas. Ele pode detectar clusters de forma arbitrária e identificar ruídos (outliers).

---

🧩 **Como funciona**

1. Para cada ponto, conta quantos vizinhos estão dentro de uma distância `eps`.
2. Pontos com vizinhança maior ou igual a `min_samples` são considerados **pontos centrais**.
3. Clusters são formados conectando pontos centrais e seus vizinhos diretamente ou via pontos intermediários.
4. Pontos que não pertencem a nenhum cluster são considerados **ruído**.

---

⚙️ **Hiperparâmetros principais**

* `eps`: raio máximo para considerar vizinhos.
* `min_samples`: número mínimo de pontos para formar uma região densa.
* `metric`: métrica de distância (Euclidiana por padrão).

---

📏 **Pré-processamento essencial**

* **Sensível à escala dos dados** → normalização ou padronização recomendada.
* **Não lida com valores ausentes** → imputação necessária.
* **Robusto a outliers** — eles são classificados como ruído.
* Funciona melhor com dados de densidade variável.

---

📊 **Métricas de avaliação (clustering)**

* **Silhouette Score** (considerando ruído).
* **Número de clusters formados** e **quantidade de ruído**.
* **Validação cruzada não se aplica diretamente**, mas análises visuais ajudam.

---

✅ **Vantagens**

* Detecta clusters de **formato arbitrário** (não esféricos).
* Identifica **outliers** automaticamente.
* Não precisa informar número de clusters previamente.
* Funciona bem com dados ruidosos.

---

⚠️ **Desvantagens**

* Escolha de `eps` e `min_samples` pode ser difícil.
* Desempenho ruim em alta dimensionalidade (maldição da dimensionalidade).
* Sensível a escala dos dados.
* Pode ter dificuldade em clusters com densidades muito variadas.

---

⚙️ **Desempenho computacional**

* Complexidade média de $O(n \log n)$ com estruturas de dados eficientes (ex: KD-Tree).
* Pode ser lento em grandes bases de dados sem otimizações.
* Escala mal com alta dimensionalidade.

---

📌 **Quando aplicar**

* Quando há suspeita de **clusters com formas irregulares**.
* Quando precisa detectar **outliers/ruídos** automaticamente.
* Quando não se sabe o número de clusters a priori.
* Em dados com **densidades razoavelmente uniformes**.

