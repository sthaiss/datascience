## 📎 **Comparativo Rápido: K-Means vs K-Medoids**

| Aspecto                  | **K-Means**                                       | **K-Medoids**                                             |
| ------------------------ | ------------------------------------------------- | --------------------------------------------------------- |
| Centroide                | Média dos pontos do cluster (ponto virtual)       | Medoide: ponto real mais central no cluster               |
| Sensibilidade a outliers | Alta — outliers puxam o centroide                 | Mais robusto — outliers não afetam tanto o medoide        |
| Métrica de distância     | Normalmente Euclidiana                            | Qualquer métrica (Euclidiana, Manhattan, etc.)            |
| Velocidade               | Rápido, eficiente em grandes datasets             | Mais lento, custo computacional maior                     |
| Escalabilidade           | Escala bem para grandes volumes                   | Escala pior, precisa de otimizações para datasets grandes |
| Valores ausentes         | Não lida diretamente                              | Também não lida diretamente                               |
| Aplicações típicas       | Quando clusters têm forma esférica e dados limpos | Quando há outliers ou dados com formatos irregulares      |
| Interpretabilidade       | Centroide pode não corresponder a um ponto real   | Medoide é ponto real, facilitando interpretação           |

---

💡 **Resumo**

> *“K-Means é a escolha padrão para clustering rápido quando seus dados são limpos e você espera clusters esféricos. Já K-Medoids é melhor quando seus dados têm outliers ou formatos complexos, pois usa pontos reais como centros, o que é mais robusto, mas com custo computacional maior.”*
