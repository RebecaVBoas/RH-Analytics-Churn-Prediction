# 📊 RH Analytics: Previsão de Rotatividade (Churn)

## 💼 O Problema de Negócio
A empresa estava enfrentando uma alta taxa de rotatividade (turnover) e precisava entender:
1. Quais são os principais fatores que levam um funcionário a sair?
2. Podemos prever quem será o próximo a sair para agir preventivamente?

## 🛠️ Estratégia da Solução
Utilizei dados históricos de funcionários (IBM HR Analytics) e segui os seguintes passos:
1. **Análise Exploratória:** Descobri que Jovens e pessoas com Baixa Renda saem mais.
2. **Pré-processamento:** Transformei variáveis categóricas em numéricas (Label Encoding) e apliquei Escala (MinMax) para normalizar salários e idades.
3. **Machine Learning:** Testei Regressão Logística e Random Forest.
   - O modelo final (Random Forest) alcançou um **Recall de 60%**, ou seja, detecta 6 de cada 10 funcionários em risco.

## 📈 Principais Insights
* **Salário é Rei:** A variável `MonthlyIncome` foi a mais importante para o modelo.
* **Idade:** Jovens tendem a sair mais (falta de plano de carreira?).
* **Horas Extras:** Funcionários com `OverTime` também mostraram maior tendência de saída.

## 🤖 Performance do Modelo
| Modelo | Acurácia | Recall (Classe 1) |
| :--- | :---: | :---: |
| Regressão Logística | 60% | 0.60 |
| Random Forest | 85% | 0.45 |

*Optei por priorizar o Recall para minimizar o risco de perder talentos despercebidos.*

## 🏁 Conclusão
O projeto demonstrou que é possível antecipar a saída de funcionários analisando métricas básicas de RH. O próximo passo seria implementar esse modelo em um Dashboard para o time de RH monitorar mensalmente.

---
**Ferramentas:** Python, Pandas, Scikit-Learn, Seaborn.
