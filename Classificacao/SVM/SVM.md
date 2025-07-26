🧠 **SVM - Support Vector Machine**

**SVM é um algoritmo supervisionado poderoso para classificação e regressão**, especialmente eficaz em espaços de alta dimensionalidade. Ele busca encontrar o **hiperplano ótimo que separa as classes com a maior margem possível** entre os dados.

Pode ser usado para **classificação binária, multiclasse (via One-vs-Rest)** e regressão (SVR).

---

🧩 **Como funciona**

1. Identifica os **vetores de suporte**: pontos mais próximos da fronteira de decisão.
2. Encontra o **hiperplano que maximiza a margem** entre as classes.
3. Pode usar **funções kernel** para projetar os dados em espaços de maior dimensão e **lidar com dados não linearmente separáveis**.

---

⚙️ **Hiperparâmetros principais**

* `C`: controla a penalização de erros (trade-off entre margem e erro).
* `kernel`: tipo de função usada para transformar os dados (`linear`, `rbf`, `poly`, `sigmoid`).
* `gamma`: define a influência de um ponto de treino (para kernels não lineares).
* `degree`: grau do polinômio (se `kernel='poly'`).
* `class_weight`: útil para tratar **classes desbalanceadas**.

---

📏 **Pré-processamento essencial**

* **Exige padronização dos dados** (SVM é sensível à escala).
* **Não lida com valores ausentes** → imputação necessária.
* Pode ser **sensível a outliers**, que influenciam o hiperplano.
* **Dados desbalanceados** afetam a fronteira → usar `class_weight='balanced'` ou técnicas de reamostragem.

---

📊 **Métricas de avaliação**

* **Acurácia, Precisão, Recall, F1-score, ROC-AUC, Matriz de Confusão**.
* **Validação cruzada** é essencial, especialmente para **ajuste fino de C e gamma**.
* Grid search com validação cruzada ajuda a encontrar o melhor conjunto de hiperparâmetros.

---

✅ **Vantagens**

* **Alta performance em espaços de alta dimensionalidade**.
* Funciona bem com **margem clara entre classes**.
* **Kernel trick** permite aplicar SVM em problemas **não lineares**.
* Modelo **robusto contra overfitting** com os hiperparâmetros corretos.

---

⚠️ **Desvantagens**

* **Lento em grandes volumes de dados** (custo quadrático/cúbico).
* Difícil de interpretar e explicar.
* **Sensível a outliers** e **dados desbalanceados**.
* Não lida com **valores ausentes diretamente**.
* Pode sofrer com **underfitting** se mal parametrizado ou com kernel inadequado.

---

⚙️ **Desempenho computacional**

* **Treinamento pode ser lento** em datasets grandes ou com muitos atributos.
* **Predição é mais rápida**, mas depende do número de vetores de suporte.
* Escala mal com muitos dados, mas funciona bem com **alta dimensionalidade e poucos exemplos**.
* Ideal para conjuntos de dados **médios ou pequenos**.

---

📌 **Quando aplicar**

* Quando há **clara separação entre classes** ou **poucos dados, mas com muitas features**.
* Quando você precisa de um modelo **potente e com boa generalização**.
* Para problemas **não lineares**, com uso de **kernels apropriados**.
* Quando o foco é **precisão**, mesmo com maior custo computacional.
