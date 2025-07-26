🧠 **Regressão Logística (Logistic Regression)**

**A Regressão Logística é um modelo supervisionado utilizado para tarefas de classificação binária ou multiclasse.** Apesar do nome, é um modelo de **classificação**, que estima a **probabilidade de pertencimento a uma classe**, usando a **função logística (sigmoide)**.

---

🧩 **Como funciona**

1. Calcula uma **combinação linear dos atributos**:
   $z = w_0 + w_1x_1 + w_2x_2 + \ldots + w_nx_n$
2. Aplica a **função sigmoide** para transformar o valor em uma **probabilidade**:
   $\hat{y} = \frac{1}{1 + e^{-z}}$
3. Define um **limiar de decisão** (ex: 0.5) para classificar.

---

⚙️ **Hiperparâmetros principais**

* `penalty`: tipo de regularização (`l1`, `l2`, `elasticnet`).
* `C`: força da regularização (inverso de λ → **quanto menor o C, maior a penalização**).
* `solver`: algoritmo de otimização (ex: `liblinear`, `saga`, `lbfgs`).
* `max_iter`: número máximo de iterações.
* `class_weight`: útil em problemas com classes desbalanceadas.

---

📏 **Pré-processamento essencial**

* **Sensível à escala** dos atributos → **padronização** recomendada.
* **Não lida com valores ausentes** → é necessário **imputar antes**.
* **Pode ser sensível a outliers**, que afetam os coeficientes.
* Funciona melhor com **atributos informativos e linearmente separáveis**.
* Em caso de **classes desbalanceadas**, usar `class_weight='balanced'` ou técnicas de resampling.

---

📊 **Métricas de avaliação**

* **Acurácia, Precisão, Recall, F1-score, ROC-AUC, Matriz de Confusão**.
* Curvas de **precisão-recall** são úteis em contextos desbalanceados.
* **Validação cruzada** recomendada para avaliar generalização e ajustar hiperparâmetros.

---

✅ **Vantagens**

* **Simples, rápido e interpretável** (coeficientes têm significado).
* **Funciona bem com poucos dados e features relevantes**.
* Fácil de regularizar para **evitar overfitting**.
* Serve como **baseline forte** para comparação com modelos mais complexos.

---

⚠️ **Desvantagens**

* **Assume separabilidade linear** → pode ter desempenho ruim com dados não lineares.
* **Sensível a outliers e multicolinearidade**.
* Não trata **valores ausentes diretamente**.
* Pode sofrer com **underfitting** se o modelo for mal especificado.
* **Desempenho limitado em problemas complexos ou com muitos atributos irrelevantes**.

---

⚙️ **Desempenho computacional**

* **Treinamento e predição rápidos**, mesmo em datasets grandes.
* Baixo consumo de recursos → ideal para **produção em larga escala**.
* **Escala bem com número de amostras**, mas pode ser impactado por **alta dimensionalidade** sem regularização adequada.

---

📌 **Quando aplicar**

* Quando se deseja um modelo **simples, rápido e interpretável**.
* Como **baseline em tarefas de classificação binária**.
* Quando os dados são **linearmente separáveis** ou próximos disso.
* Quando **explicabilidade dos coeficientes** é importante para o negócio.


