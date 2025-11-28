# Cálculo de Métricas de Avaliação de Aprendizado

Este projeto implementa cálculos de métricas fundamentais utilizadas em modelos de Machine Learning.  
É um exercício prático para reforçar o entendimento dos indicadores usados para avaliar algoritmos supervisionados. Tem como objetivo calcular as principais métricas para avaliação de modelos de classificação, focando no entendimento de como cada métrica funciona e como calculá-las a partir de uma matriz de confusão.

## Métricas Abordadas

As métricas que serão calculadas são:

*   **Acurácia:** Representa a correção geral do modelo, ou seja, a proporção de previsões corretas em relação ao total de previsões.
*   **Sensibilidade (Recall):** Mede a capacidade do modelo de identificar todos os casos positivos corretamente. Em outras palavras, ela indica quantos dos positivos reais foram encontrados.
*   **Especificidade:** Mede a capacidade do modelo de identificar todos os casos negativos corretamente. Indica quantos dos negativos reais foram classificados corretamente.
*   **Precisão:** Indica a proporção de previsões positivas que realmente são positivas. Em outras palavras, ela responde a pergunta "de todas as previsões positivas, quantas estavam corretas?".
*   **F-score (ou F1-score):** É uma média harmônica entre precisão e sensibilidade. É útil quando você quer um equilíbrio entre essas duas métricas.
*   **Curva ROC (Receiver Operating Characteristic):** É um gráfico que mostra o desempenho de um modelo de classificação para vários limiares de classificação. Essa curva é usada para avaliar a capacidade do modelo de distinguir entre classes.

## Componentes Chave

### Matriz de Confusão

*   É a base para todos os cálculos das métricas.
*   Ela representa a contagem de verdadeiros positivos (VP), verdadeiros negativos (VN), falsos positivos (FP) e falsos negativos (FN).
*   Para os cálculos, uma matriz de confusão é escolhida de forma arbitrária.

### Fórmulas das Métricas

As fórmulas utilizadas para calcular cada métrica são:

*   **Sensibilidade (Recall):** VP / (VP + FN)
*   **Especificidade:** VN / (FP + VN)
*   **Acurácia:** (VP + VN) / N (onde N é o número total de elementos)
*   **Precisão:** VP / (VP + FP)
*   **F-score:** 2 * (Precisão * Sensibilidade) / (Precisão + Sensibilidade)

## Aplicação Prática

*   O projeto foca em consolidar a compreensão de como as métricas funcionam e como realizar os cálculos.
*   Assume-se que o projeto se baseia em conceitos aprendidos em módulos anteriores.
*   Bibliotecas como `pandas`, `matplotlib` e `scikit-learn` podem ser utilizadas, pois são ferramentas comuns para aprendizado de máquina em Python.

## Matriz de Confusão de Exemplo

A matriz de confusão utilizada como exemplo para os cálculos é:

1 0 0 0 0 0 0 0 0 0

0 0.99 0 0 0 0 0 0 0 0

0 0 0.98 0.01 0 0 0 0.01 0 0

0 0 0 1 0 0 0 0 0 0

0 0 0 0 0.99 0 0 0 0 0.01

0 0 0 0.02 0 0.98 0 0 0 0

0.01 0 0 0 0 0 0.99 0 0 0

0 0 0 0 0 0 0 1 0 0

0 0 0 0.01 0 0 0 0 0.99 0

0 0 0 0 0 0 0 0.01 0 0.98
