# Métricas Adequadas para o trabalho (provisório)

## 1. **Erro Absoluto Médio (MAE - Mean Absolute Error)**
- Mede a média dos erros absolutos.
- Interpretação simples, fácil de entender.
- Fórmula:
  \[
  MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
  \]

---

## 2. **Erro Médio Quadrático (MSE - Mean Squared Error)**
- Penaliza erros maiores, tornando-o sensível a outliers.
- Fórmula:
  \[
  MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
  \]

---

## 3. **Raiz do Erro Médio Quadrático (RMSE - Root Mean Squared Error)**
- Raiz quadrada do MSE, retornando os erros na mesma escala da variável original.
- Fórmula:
  \[
  RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2}
  \]

---

## 4. **Erro Percentual Absoluto Médio (MAPE - Mean Absolute Percentage Error)**
- Mede o erro relativo em porcentagem, útil para interpretar o impacto do erro em relação ao valor real.
- Fórmula:
  \[
  MAPE = \frac{1}{n} \sum_{i=1}^{n} \left| \frac{y_i - \hat{y}_i}{y_i} \right| \times 100
  \]
- **Cuidado:** Não é adequado quando há valores reais próximos de zero.

---

## 5. **Coeficiente de Determinação (R² - R-Squared)**
- Mede a proporção da variância explicada pelo modelo.
- Fórmula:
  \[
  R^2 = 1 - \frac{\sum_{i=1}^{n} (y_i - \hat{y}_i)^2}{\sum_{i=1}^{n} (y_i - \bar{y})^2}
  \]

---

## 6. **Erro Médio Simétrico Absoluto (sMAPE - Symmetric Mean Absolute Percentage Error)**
- Versão modificada do MAPE que evita distorções para valores pequenos.
- Fórmula:
  \[
  sMAPE = \frac{1}{n} \sum_{i=1}^{n} \frac{|y_i - \hat{y}_i|}{(|y_i| + |\hat{y}_i|)/2} \times 100
  \]

---

## 7. **Log-Loss ou Likelihood para Modelos Probabilísticos**
- Avalia a qualidade das previsões probabilísticas.

---

## 8. **Akaike Information Criterion (AIC) e Bayesian Information Criterion (BIC)**
- Métricas para comparar modelos SARIMA ou similares.
- Penalizam a complexidade do modelo para evitar overfitting.

---

## 9. **Teste de Resíduos (Ex.: Ljung-Box Test)**
- Avalia se os resíduos do modelo são ruído branco (sem autocorrelação).

---

## **Seleção de Métricas**
- **Se o foco for precisão:** RMSE ou MAE.
- **Se os dados forem sensíveis a escalas:** MAPE ou sMAPE.
- **Para comparação entre modelos ARIMA:** AIC/BIC.
- **Para validação de independência dos erros:** Teste Ljung-Box.
