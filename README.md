
# Credit Risk Prediction — Previsão de Inadimplência com Machine Learning

## Sobre o projeto

O presente projeto tem como objetivo aplicar técnicas de Ciência de Dados e Machine Learning para analisar o comportamento financeiro de clientes e identificar possíveis riscos de inadimplência.

A proposta consiste em explorar uma base de dados real, identificar padrões relacionados ao histórico de pagamentos e desenvolver modelos preditivos capazes de estimar a probabilidade de um cliente não cumprir suas obrigações financeiras.

O projeto foi desenvolvido como parte do aprimoramento dos meus conhecimentos práticos em Ciência de Dados, análise exploratória, estatística e aprendizado de máquina.

## Tecnologias utilizadas

- Python
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab
- Git e GitHub

## Base de dados

Foi utilizada a base pública **Default of Credit Card Clients**, disponibilizada pela UCI Machine Learning Repository.

A base contém informações de 30.000 clientes de cartão de crédito de Taiwan, incluindo características demográficas, limites de crédito, históricos de pagamentos e registros de inadimplência.

Fonte: https://archive.ics.uci.edu/dataset/350/default+of+credit+card+clients

## Metodologia

O desenvolvimento foi dividido nas seguintes atividades:

1. **Análise exploratória:** investigação da distribuição de inadimplência e das características dos clientes.
2. **Tratamento dos dados:** verificação de valores ausentes, registros duplicados e categorias não documentadas.
3. **Preparação:** separação das variáveis preditoras e da variável-alvo, seguida da divisão dos dados.
4. **Treinamento:** desenvolvimento de modelos de Regressão Logística e Random Forest.
5. **Avaliação:** utilização de accuracy, precision, recall, F1-score e matriz de confusão.
6. **Experimentação:** comparação de diferentes limiares de classificação para o Random Forest.

## Resultados dos modelos

Os modelos foram comparados utilizando um conjunto de validação com 4.800 registros.

| Métrica | Regressão Logística | Random Forest |
|---|---:|---:|
| Accuracy | 81% | 82% |
| Precision (classe 1) | 71% | 65% |
| Recall (classe 1) | 26% | 38% |
| F1-score (classe 1) | 38% | 48% |

O Random Forest apresentou melhor recall e F1-score para identificar clientes inadimplentes.

### Ajuste do limiar de decisão

Foram avaliados diferentes limiares de classificação do Random Forest.

| Limiar | Precision | Recall | F1-score |
|---|---:|---:|---:|
| 0,30 | 51% | 56% | 54% |
| 0,40 | 60% | 47% | 53% |
| 0,50 | 65% | 38% | 48% |

O limiar de 0,30 apresentou o melhor F1-score entre os valores testados, aumentando a identificação de inadimplentes, mas também gerando mais falsos positivos.

## Conclusão

O desenvolvimento deste projeto permitiu aplicar conhecimentos de Ciência de Dados em um problema relacionado à análise de
