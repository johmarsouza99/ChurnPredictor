# Customer Churn Prediction

Este projeto tem como objetivo analisar dados de clientes de uma empresa de telecomunicações para prever o churn (cancelamento de serviço). Utilizamos análise exploratória de dados (EDA), engenharia de features e diferentes modelos de machine learning para criar um modelo preditivo eficiente.

## 📌 Objetivos

- Analisar padrões de cancelamento de clientes (churn).
- Criar um modelo preditivo para identificar clientes com alto risco de churn.
- Oferecer insights estratégicos para retenção de clientes.

---

## 📊 Metodologia

1. **Coleta e Importação de Dados**
   - Leitura de múltiplos arquivos `.csv` contendo informações de contrato, internet, telefone e dados pessoais dos clientes.
   - Identificação e tratamento de valores ausentes e duplicatas.

2. **Análise Exploratória de Dados (EDA)**
   - Identificação de padrões de churn por meio de estatísticas descritivas e visualizações.
   - Análise do impacto de variáveis como tipo de contrato, serviços adicionais e métodos de pagamento no churn.

3. **Pré-processamento e Engenharia de Features**
   - Padronização dos nomes das colunas para o formato `snake_case`.
   - Conversão de variáveis categóricas para formato adequado.
   - Criação de novas features, como tempo de assinatura e quantidade de serviços contratados.

4. **Divisão do Conjunto de Dados**
   - Separação dos dados em `treino (80%)`, `validação (10%)` e `teste (10%)`.
   - Balanceamento de classes usando upsampling da classe minoritária.

5. **Treinamento de Modelos**
   - Modelos testados:
     - DummyClassifier (baseline)
     - Logistic Regression
     - Decision Tree
     - LightGBM
     - CatBoost
     - XGBoost
   - Utilização do **Optuna** para otimização de hiperparâmetros.
   - Avaliação dos modelos usando **ROC AUC**, **accuracy** e matriz de confusão.

6. **Salvamento e Implementação**
   - Modelos treinados são salvos na pasta `models/` usando `pickle`.
   - O melhor modelo pode ser utilizado para previsões futuras.

---

# 📈 Resultados
  - Clientes que pagam entre $70 e $100/mês apresentam a maior taxa de churn (~38%).
  - O tipo de contrato tem grande impacto no churn: planos mensais têm maior taxa de cancelamento.
  - Serviços como segurança online, backup e suporte técnico reduzem o churn.
  - Métodos de pagamento eletrônico (e-check) possuem maior taxa de churn.
  - O modelo LightGBM apresentou a melhor performance, com um ROC AUC de 96%.

# 📄 Contribuição
  - Sinta-se à vontade para abrir uma issue ou enviar um pull request caso tenha melhorias para o projeto.



