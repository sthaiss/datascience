✅ O que é
✅ Como funciona
✅ Quando aplicar
✅ Hiperparâmetros
✅ Métricas de avaliação
✅ Vantagens
✅ Desvantagens

---

🧠 **Naive Bayes**

**Naive Bayes é um algoritmo supervisionado de classificação baseado no Teorema de Bayes**, com a **suposição ingênua (naive) de independência entre os atributos**. Funciona bem em problemas com **alta dimensionalidade** e **texto categorizado**, como **classificação de e-mails (spam ou não)**.

---

🧩 **Como funciona**

Baseia-se na fórmula:

> **P(C|X) ∝ P(X|C) \* P(C)**

Ou seja, calcula a **probabilidade posterior** de uma classe $C$ dado um conjunto de atributos $X$, assumindo que os atributos são **independentes entre si**.

1. Calcula a **probabilidade de cada classe** com base nos dados de treino.
2. Para um novo exemplo, calcula a **probabilidade de cada classe** dada suas características.
3. Retorna a **classe com maior probabilidade**.

---

⚙️ **Hiperparâmetros principais**

Depende da **variação do Naive Bayes** usada:

* **GaussianNB**: assume distribuição normal dos atributos contínuos.

  * Hiperparâmetro: `var_smoothing` (evita divisão por zero).
* **MultinomialNB**: para contagens (ex: texto).

  * Hiperparâmetro: `alpha` (suavização de Laplace).
* **BernoulliNB**: para atributos binários (0/1).

  * Hiperparâmetro: `alpha`, `binarize`.

---

📏 **Pré-processamento essencial**

* **Imputação de dados ausentes** é necessária (Naive Bayes padrão **não lida diretamente com valores nulos**).
* Multinomial e Bernoulli exigem **atributos positivos**.
* GaussianNB exige atenção à **distribuição dos dados contínuos** (idealmente normal).
* **Outliers** podem afetar o desempenho, especialmente no **GaussianNB**.
* Funciona melhor com **atributos informativos e discretos**.

---

📊 **Métricas de avaliação**

* **Acurácia, Precisão, Recall, F1-score, Matriz de Confusão**.
* **ROC-AUC** útil especialmente com **classes desbalanceadas**.
* **Validação cruzada** é importante para avaliar a robustez do modelo e evitar overfitting.

---

✅ **Vantagens**

* **Extremamente rápido** para treinar e prever.
* Funciona bem com **grandes volumes de dados** e **alta dimensionalidade**.
* **Robusto a atributos irrelevantes** e tolerante a ruído.
* **Poucos hiperparâmetros**, fácil de ajustar.
* Menor risco de **overfitting**, principalmente com dados simples.

---

⚠️ **Desvantagens**

* Suposição de **independência entre atributos muitas vezes é irrealista**.
* Pode ter **baixa acurácia comparado a modelos mais complexos**.
* **Sensível a outliers** (no caso de GaussianNB).
* Não lida com **valores ausentes** diretamente.
* Pode sofrer com **classes desbalanceadas**, favorecendo a classe majoritária.
* Risco de **underfitting** em problemas com interações complexas entre variáveis.

---

📌 **Quando aplicar**

* Em **problemas de classificação de texto** (spam, sentimento, tópicos).
* Como **modelo baseline rápido, simples e interpretável**.
* Em **conjuntos de dados com muitos atributos e poucas amostras**.
* Quando há **necessidade de treinar e testar rapidamente**, inclusive com validação cruzada.


