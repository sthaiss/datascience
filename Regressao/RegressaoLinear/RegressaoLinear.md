🧠 **Regressão Linear**

**Regressão Linear é um modelo supervisionado usado para prever valores contínuos.** Ela assume uma relação **linear entre os atributos (features) e a variável alvo**, ajustando uma reta (ou hiperplano) que minimiza o erro entre as previsões e os valores reais.

---

🧩 **Como funciona**

1. Aprende os **coeficientes (pesos)** que multiplicam cada variável de entrada.
2. Ajusta a equação da forma:
   $\hat{y} = w_0 + w_1x_1 + w_2x_2 + \ldots + w_nx_n$
3. O objetivo é **minimizar o erro (função de custo)**, normalmente o **Erro Quadrático Médio (MSE)**.

---

⚙️ **Hiperparâmetros principais**

> Obs: a Regressão Linear "pura" tem poucos hiperparâmetros. Para regularização, usamos variantes:

* `fit_intercept`: se ajusta o termo independente.
* `normalize`: se normaliza os dados internamente (em versões antigas do sklearn).
* `regularização`:

  * **Ridge (L2)**: penaliza coeficientes grandes.
  * **Lasso (L1)**: pode zerar coeficientes (seleção de variáveis).
  * **ElasticNet**: combinação de L1 + L2.

---

📏 **Pré-processamento essencial**

* **Sensível à escala** → é recomendada a **padronização dos dados**.
* **Não lida com valores ausentes** → requer **imputação**.
* **Muito sensível a outliers**, que distorcem a linha de regressão.
* **Multicolinearidade entre variáveis** pode afetar o modelo → verificar com VIF.
* Não faz suposições sobre **distribuição dos dados de entrada**, mas **assume resíduo normal e homocedástico**.

---

📊 **Métricas de avaliação (regressão)**

* **MAE (Erro Absoluto Médio)**
* **MSE (Erro Quadrático Médio)**
* **RMSE (Raiz do Erro Quadrático Médio)**
* **$R^2$** (Coeficiente de Determinação)
* **Validação cruzada** é importante para avaliar a estabilidade e evitar overfitting em datasets pequenos.

---

✅ **Vantagens**

* **Simples, rápido e interpretável** (coeficientes indicam influência de cada variável).
* Fácil de implementar e explicar.
* Requer **pouco poder computacional**.
* Funciona bem quando a **relação é de fato linear**.

---

⚠️ **Desvantagens**

* **Assume relação linear**, o que pode ser uma limitação em dados reais.
* **Muito sensível a outliers e multicolinearidade**.
* Pode sofrer com **underfitting** em problemas complexos.
* **Não trata valores ausentes**.
* Não modela interações ou efeitos não lineares sem transformação manual das features.

---

⚙️ **Desempenho computacional**

* **Extremamente rápido** para treinar e predizer.
* **Escala bem com grandes volumes de dados**, especialmente se o número de features for pequeno.
* Ideal para aplicações com **restrição de tempo ou recursos**.

---

📌 **Quando aplicar**

* Quando você quer um modelo **rápido, simples e interpretável**.
* Como **baseline para comparação com modelos mais complexos**.
* Quando os dados mostram **tendência linear clara** ou **você precisa entender a contribuição de cada variável**.
