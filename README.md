# Credit Card Fraud Prediction

> https://www.kaggle.com/datasets/kelvinkelue/credit-card-fraud-prediction

**Autora do Notebook:** Isabella Heder

Este projeto tem como objetivo identificar transações fraudulentas em cartões de crédito utilizando técnicas de análise exploratória de dados e machine learning.

A detecção de fraudes é um desafio comum em instituições financeiras devido ao forte desbalanceamento entre transações legítimas e fraudulentas. Além do impacto financeiro direto, modelos eficientes ajudam a reduzir prejuízos, aumentar a segurança dos clientes e tornar os processos de prevenção mais eficazes.

Diferente de datasets anonimizados, este conjunto de dados apresenta atributos reais relacionados ao perfil do cliente, transação e comerciante, permitindo análises mais próximas de cenários reais de negócio e maior interpretabilidade dos resultados.

### **Objetivo**

Desenvolver modelos de machine learning capazes de:

- Identificar transações fraudulentas com alta precisão
- Minimizar falsos negativos (fraudes não detectadas)
- Avaliar diferentes estratégias para tratamento do desbalanceamento dos dados
- Apoiar processos de prevenção e monitoramento de fraudes

### Dataset

- Dataset público disponível no Kaggle (link no início deste README)
- Cada linha representa uma transação financeira

### Variável Alvo

**is_fraud**

- **0** → Transação legítima
- **1** → Transação fraudulenta
- A variável alvo apresentou forte desbalanceamento entre transações legítimas e fraudulentas
  - Para reduzir este problema foi aplicada a técnica de **Random Undersampling**
  - O impacto dessa estratégia foi posteriormente avaliado comparando o desempenho do modelo em dados que ficaram fora da amostra utilizada no treinamento

## Resultado:

Foram testados diferentes algoritmos de classificação, incluindo:
- Logistic Regression
- Random Forest
- XGBoost

> Melhor modelo: XGBoost

<img width="539" height="432" alt="6e662a88-5186-4e6d-a16d-00af767b9478" src="https://github.com/user-attachments/assets/aa4051b8-5a1d-4ae7-9126-f9ab141f32d8" />

              precision    recall  f1-score   support

           0       0.97      0.97      0.97       429
           1       0.97      0.97      0.97       429

    accuracy                           0.97       858
    macro avg      0.97      0.97      0.97       858
    weighted avg   0.97      0.97      0.97       858
