🧠 **Árvore de Regressão (Decision Tree Regressor)**

**A Árvore de Regressão é um modelo supervisionado usado para prever valores contínuos.** Ela divide o espaço de entrada em regiões baseadas em regras de decisão, aprendidas diretamente dos dados, sem necessidade de relação linear.

---

🧩 **Como funciona**

1. **Divide recursivamente** os dados com base em regras de "maior redução do erro" (ex: MSE).
2. Em cada nó, escolhe o **melhor atributo e ponto de divisão**.
3. Para prever, segue o caminho da árvore até uma **folha**, que contém o valor médio dos dados daquele grupo.

---

⚙️ **Hiperparâmetros principais**

* `max_depth`: profundidade máxima da árvore.
* `min_samples_split`: número mínimo de amostras para dividir um nó.
* `min_samples_leaf`: número mínimo de amostras em uma folha.
* `max_features`: número de features consideradas em cada split.
* `criterion`: métrica usada para divisão (`squared_error`, `mae`, etc.).

---

📏 **Pré-processamento essencial**

* **Não precisa de normalização/padronização**.
* **Lida com dados numéricos e categóricos** (categóricos precisam ser codificados).
* **Não lida com valores ausentes nativamente** → precisa imputar.
* **Pouco sensível a outliers** comparado à Regressão Linear.
* **Desbalanceamento de dados** pode afetar divisões iniciais — menos comum em regressão, mas ainda pode ocorrer.

---

📊 **Métricas de avaliação (regressão)**

* **MAE**, **MSE**, **RMSE**, **$R^2$**.
* **Validação cruzada** é recomendada para evitar overfitting e avaliar estabilidade do modelo.
* Pode usar **podas (pruning)** ou limitar profundidade para melhorar generalização.

---

✅ **Vantagens**

* **Não assume linearidade** ou distribuição específica dos dados.
* Fácil de **interpretar e visualizar**.
* Funciona bem com **interações entre variáveis**.
* **Capaz de modelar relações não lineares**.
* Baixa necessidade de pré-processamento.

---

⚠️ **Desvantagens**

* **Propensa a overfitting** em profundidades grandes (modelo muito específico).
* Pequenas mudanças nos dados podem gerar árvores bem diferentes.
* **Menor performance geral** comparado a ensembles como Random Forest ou Boosting.
* **Não lida com valores ausentes** diretamente.

---

⚙️ **Desempenho computacional**

* **Rápida para treinar e prever** em datasets pequenos a médios.
* Pode ser **ineficiente com muitos atributos** (alta dimensionalidade).
* Treinamento e predição são **leves**, mas o tamanho da árvore pode crescer rápido sem restrições.

---

📌 **Quando aplicar**

* Quando se quer **modelo interpretável** com **pouco pré-processamento**.
* Quando os dados têm **relações não lineares ou interações complexas**.
* Como **baseline explicativo** antes de usar ensembles.
* Em problemas de regressão **simples ou de média complexidade**.
