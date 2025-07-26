🧠 **Gradient Boosting**

**Gradient Boosting é uma técnica de ensemble supervisionado** que constrói modelos fracos (geralmente árvores de decisão rasas) de forma sequencial, onde **cada novo modelo corrige os erros do anterior**, minimizando uma **função de perda via gradiente**.

Usado tanto para **classificação quanto regressão**, com versões otimizadas como **XGBoost, LightGBM e CatBoost**.

---

🧩 **Como funciona**

1. Começa com uma predição inicial (ex: média).
2. Calcula o **erro residual** do modelo atual.
3. Ajusta uma **nova árvore aos resíduos** (gradiente negativo da perda).
4. Soma as árvores anteriores, ponderadas por uma taxa de aprendizado.
5. Repete o processo iterativamente.

---

⚙️ **Hiperparâmetros principais**

* `n_estimators`: número de árvores (iterações).
* `learning_rate`: taxa de aprendizado (quanto corrigir a cada passo).
* `max_depth`: profundidade das árvores.
* `subsample`: fração dos dados usada em cada árvore (para evitar overfitting).
* `colsample_bytree`: fração de features usada por árvore.
* `min_child_weight` (XGBoost) ou `min_data_in_leaf` (LightGBM): mínimo de dados em um nó folha.
* `boosting_type` (LightGBM): `gbdt`, `dart`, etc.

---

📏 **Pré-processamento essencial**

* **Não lida com valores ausentes diretamente** → algumas libs imputam internamente (ex: XGBoost, LGBM).
* **Não precisa de normalização/padronização**.
* Pode ser sensível a **outliers e overfitting** se mal parametrizado.
* **Lida bem com classes desbalanceadas**, especialmente com ajuste de `scale_pos_weight` ou `class_weight`.

---

📊 **Métricas de avaliação**

* Classificação: Acurácia, Precisão, Recall, F1-score, ROC-AUC.
* Regressão: MAE, RMSE, MSE, $R^2$.
* **Validação cruzada** e **early stopping** são cruciais para evitar overfitting.
* **Grid search ou random search** com cross-validation para ajuste fino dos hiperparâmetros.

---

✅ **Vantagens**

* **Alta performance** e precisão em tarefas complexas.
* Funciona bem com **dados estruturados e tabulares**.
* **Flexível com diferentes funções de perda**.
* Suporta **paralelização** (especialmente LightGBM e XGBoost).
* **Boas técnicas internas de regularização** (shrinkage, subsampling, etc.).

---

⚠️ **Desvantagens**

* **Mais difícil de interpretar** que modelos simples (árvore única, regressão).
* **Custo computacional alto** em datasets grandes.
* **Propenso a overfitting** se não regularizado corretamente.
* Não lida com **valores ausentes** nativamente em todas as implementações.
* Pode exigir **bastante tuning** para atingir performance ideal.

---

⚙️ **Desempenho computacional**

* Treinamento **mais lento** que modelos simples, mas versões como **LightGBM e XGBoost são otimizadas**.
* **Predição é relativamente rápida**, mesmo com muitas árvores.
* **Escala bem com grandes volumes de dados**, especialmente com uso de **GPU** ou paralelismo.

---

📌 **Quando aplicar**

* Quando o objetivo é **maximizar performance em dados estruturados**.
* Quando se tem **tempo para tuning** e boa capacidade computacional.
* Quando modelos simples não capturam bem a complexidade do problema.
* Ideal para **competições de ML**, **problemas tabulares**, e **produção com alta exigência de acurácia**.

