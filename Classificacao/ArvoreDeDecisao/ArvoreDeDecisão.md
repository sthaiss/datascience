🧠 **Árvore de Decisão (Decision Tree)**

**Árvores de decisão são modelos supervisionados que utilizam uma estrutura em forma de árvore para tomar decisões.** Elas dividem os dados em **nós de decisão**, baseando-se em **condições sobre os atributos**, até atingir folhas com previsões finais (classe ou valor).

Podem ser usadas tanto para **classificação quanto regressão**.

---

🧩 **Como funciona**

1. O algoritmo escolhe o **atributo que melhor separa os dados**, com base em métricas como:

   * **Gini**, **Entropia** (classificação)
   * **MSE** (regressão)
2. Divide recursivamente os dados em **subconjuntos mais puros**.
3. Para prever, segue os ramos da árvore com base nas características do exemplo.

---

⚙️ **Hiperparâmetros principais**

* `max_depth`: profundidade máxima da árvore (limita complexidade).
* `min_samples_split`: número mínimo de amostras para dividir um nó.
* `min_samples_leaf`: número mínimo de amostras em uma folha.
* `criterion`: função de avaliação do split (ex: gini, entropy).
* `max_features`: número de atributos considerados por split (ajuda a reduzir overfitting).

---

📏 **Pré-processamento essencial**

* **Tolera dados ausentes** (algumas implementações tratam nativamente ou por imputação simples).
* **Não exige normalização ou padronização** dos dados.
* Pode lidar com **variáveis categóricas e numéricas**.
* **Sensível a outliers**: pode criar splits desbalanceados.
* **Pode se adaptar a dados desbalanceados**, mas a performance pode cair — usar pesos ou balanceamento ajuda.

---

📊 **Métricas de avaliação**

* **Classificação**: Acurácia, Precisão, Recall, F1-score, Matriz de Confusão, ROC-AUC.
* **Regressão**: MAE, MSE, RMSE, $R^2$.
* **Validação cruzada** é essencial para medir a generalização e evitar overfitting.

---

✅ **Vantagens**

* **Fácil de entender e interpretar** (visualização da árvore).
* **Pouco pré-processamento** necessário.
* Suporta **dados mistos** (categóricos e numéricos).
* Pode lidar com **dados com valores faltantes** em algumas bibliotecas.
* Boa capacidade de **modelar relações não-lineares**.

---

⚠️ **Desvantagens**

* Alta tendência ao **overfitting**, especialmente com árvores profundas.
* **Instável** a pequenas variações nos dados (gera árvores muito diferentes).
* **Sensível a outliers e ruído**.
* Pode ter **viés para atributos com mais níveis** (categorias).
* **Desempenho pior** que métodos ensemble (ex: Random Forest) em datasets complexos.

---

⚙️ **Desempenho computacional**

* **Treinamento rápido**, especialmente em datasets menores.
* **Predição muito rápida** (caminho único até a folha).
* **Escala moderadamente bem** com dados maiores.
* Pode crescer demais se não for controlada (profundidade, mínimo de amostras, etc).

---

📌 **Quando aplicar**

* Quando você precisa de um modelo **simples, explicável e visualizável**.
* Em problemas onde a **interpretabilidade é importante**.
* Como **modelo baseline**, ou como base para métodos ensemble como **Random Forest** e **Gradient Boosting**.



