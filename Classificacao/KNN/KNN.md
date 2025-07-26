✅ O que é
✅ Como funciona
✅ Quando aplicar
✅ Hiperparâmetros
✅ Métricas de avaliação
✅ Vantagens
✅ Desvantagens


🧠 **KNN - K-Nearest Neighbors**

**KNN é um algoritmo supervisionado, simples e intuitivo**, utilizado tanto para **classificação quanto para regressão**. Ele é baseado na ideia de que **pontos semelhantes estão próximos no espaço de atributos**.


🧩 **Como funciona**

Para fazer uma predição, o KNN segue estes passos:

1. **Calcula a distância*entre o ponto a ser classificado e todos os pontos do conjunto de treino (normalmente usando distância Euclidiana).
2. **Seleciona os K vizinhos mais próximos*com base nessa distância.
3. Para **classificação**, escolhe a **classe mais frequente*entre os vizinhos.
   Para **regressão**, retorna a **média (ou mediana)*dos valores.


⚙️ **Hiperparâmetros principais**

**K**(número de vizinhos): afeta o viés e variância do modelo.
**Métrica de distância**: Euclidiana, Manhattan, Minkowski, etc.
**Ponderação dos vizinhos**: uniforme ou ponderada pela distância.


📏 **Pré-processamento essencial**

O KNN é **sensível à escala das variáveis**, então é fundamental **normalizar ou padronizar os dados**.
Pode ser afetado por **outliers e atributos irrelevantes**.


📊 **Métricas de avaliação**

Para classificação: **Acurácia, Precisão, Recall, F1-score*e **Matriz de Confusão**.
Para regressão: **MAE (Mean Absolute Error)**, **RMSE (Root Mean Squared Error)**, etc.


✅ **Vantagens**

**Simples de entender e implementar**.
**Não-paramétrico*(não faz suposições sobre a distribuição dos dados).
Funciona bem em problemas com **fronteiras de decisão não lineares**.
**Alta interpretabilidade local*(fácil de explicar cada predição).


⚠️ **Desvantagens**

**Lento na fase de predição**, já que precisa calcular distância para todos os pontos.
**Escalabilidade ruim*com bases de dados grandes.
**Sensível a dados desbalanceados*e à **maldição da dimensionalidade**.
Requer bom **tratamento dos dados*para funcionar bem.



📌 **Quando aplicar**

Quando você quer um **modelo baseline simples e rápido**.
Quando os dados são **pequenos ou moderados*em tamanho e dimensionalidade.
Quando a **explicabilidade local*da decisão é importante.