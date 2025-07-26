🧠 **Random Forest**

**Random Forest é um algoritmo de aprendizado supervisionado baseado em ensemble de Árvores de Decisão.** Ele combina várias árvores construídas com aleatoriedade (tanto nos dados quanto nas features) para produzir **uma predição mais robusta, precisa e generalizável.**

É usado tanto para **classificação quanto para regressão**.

---

🧩 **Como funciona**

1. Gera **várias árvores de decisão** com amostras aleatórias do dataset (com substituição – *bootstrap*).
2. Em cada split da árvore, considera **um subconjunto aleatório de atributos**.
3. Para **classificação**: usa **votação majoritária** entre as árvores.
   Para **regressão**: usa a **média das predições**.

---

⚙️ **Hiperparâmetros principais**

* `n_estimators`: número de árvores na floresta.
* `max_depth`: profundidade máxima de cada árvore.
* `min_samples_split` / `min_samples_leaf`: controle de crescimento das árvores.
* `max_features`: número de features consideradas por split.
* `bootstrap`: se usa amostragem com substituição.
* `class_weight`: importante em problemas com classes desbalanceadas.

---

📏 **Pré-processamento essencial**

* **Tolera bem dados ausentes** (algumas libs imputam internamente).
* **Não precisa de normalização ou padronização**.
* **Robusto a outliers e ruído**.
* **Pode lidar com dados desbalanceados** usando `class_weight='balanced'` ou técnicas como *resampling*.
* Funciona com **variáveis categóricas** (se codificadas corretamente).

---

📊 **Métricas de avaliação**

* **Classificação**: Acurácia, Precisão, Recall, F1-score, Matriz de Confusão, ROC-AUC.
* **Regressão**: MAE, RMSE, MSE, $R^2$.
* **Validação cruzada** é importante para avaliar a estabilidade e evitar overfitting em datasets pequenos.

---

✅ **Vantagens**

* **Reduz overfitting** em relação a árvores individuais.
* **Alta acurácia** em diversos tipos de problemas.
* **Robusto a outliers, ruído e dados ausentes**.
* Funciona bem com **dados grandes e de alta dimensionalidade**.
* **Importância das features** pode ser extraída (feature importance).

---

⚠️ **Desvantagens**

* **Menos interpretável** que uma única árvore.
* **Mais lento para treinar e predizer** do que modelos simples.
* Pode **sofrer em tempo real** ou sistemas com restrição de recursos.
* Tende a ser **pesado em memória**, especialmente com muitas árvores profundas.
* Pode **subestimar classes minoritárias** sem ajustes (desbalanceamento).

---

⚙️ **Desempenho computacional**

* **Treinamento mais lento** que árvores individuais.
* **Predição mais pesada**, pois depende da média/votação de várias árvores.
* Pode ser **paralelizado facilmente** (cada árvore pode ser treinada separadamente).
* **Escala bem com volume de dados**, mas consome **mais RAM** e **tempo**.

---

📌 **Quando aplicar**

* Quando você quer **um modelo robusto e com boa performance sem muito tuning**.
* Quando o **overfitting das árvores de decisão** é um problema.
* Quando você **não precisa de interpretabilidade completa**, mas quer **boa acurácia geral**.
* Ideal como **modelo de produção padrão**, especialmente com **datasets mistos e complexos**.




