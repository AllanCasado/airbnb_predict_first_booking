# O Problema

Por exemplo, temos uma acurácia geral de 70%, porém para a classe 1 temos uma acurácia de 0, para a classe 2 acurácia de 0 e para a classe 3 temos 99%...

Se plotarmos uma matriz de confusão (previsões x realidade) veremos uma concentração grande de previsões pra a classe dominante.

A acurácia não representa bem esse tipo de problema.


# Possíveis Causas

* Falta de features representativas do fenômeno.
* Dados com ruídos ("sujeira").
* Escassez de exemplos de treino para as outras classes (desbalanceamento de classes).
* Divergência entre o viés dos dados e o viés do modelo (é o modelo mais adequado?).


# Possíveis Soluções

* Criação de features relevantes
* Remoção de ruídos
* Balanceamento das classes
* Escolher outros algoritmos de machine learning

Usar as métricas corretas!


# Métricas

* Accuracy
* Precision
* Recall
* F1-Score
* Balanced Accuracy
* Kappa Score
* MICC

### Balanced Accuracy

A acurácia balanceada é basicamente a média da acurácia de cada classe.

BalancedAccuracy = ((#pred correta classe A/ total predicao classe A) + (#pred correta classe B/ total predicao classe B) + ...) / # número de classes


### Kappa Score

Para calcular essa métrica precisamos medir o nível de acordo entre 2 avaliadores.

Kappa = (#acordo - (#acordo ao acaso))/1 - #acordo ao acaso

O nível de acordo é calculado somando os casos em que os avaliadores concordaram e dividindo pelo total de casos.

O nível de acordo ao acaso é uma soma do nível de acordo ao acaso de cada uma das classes.

O nível de acordo de uma classe é calculado da seguinte maneira:

Nível de Acordo da Classe 1 = Prob A (Classe 1) * Prob B (Classe 1)

Sendo A e B os avaliadores, que no caso são as previsões e os valores reais do modelo.

O Cohen's Kappa Score sempre é menor ou igual a 1. Valor de 0 ou menor indica que o classificador é inútil. De formageral, temos as seguintes faixas para interpreta:
0-0.2 slight, 0.21 - 0.4 fair, 0.41 - 0.6 moderate, 0.61 -0.8 substantial, 0.81 - 1 perfect agreement.

Esse coeficiente é interessante, também, para comparar a perfomarnce de diferentes classificadores.

# MCC

MCC - Matthew's Correlation Coefficient

MCC leva em conta todos os quatro valores da matriz de confusão (verdadeiros positivos, falsos positivos, verdadeiros negativos e falsos negativos). 

O coeficiente varia entre -1 e 1, sendo -1 indicativo de predições totalmente erradas, 0 indicativo de previsões aleatórias e 1 de predições perfeitas.

MCC = (TP x TN - FP x FN) / sqrt((TP+FP) x (TP+FN) x (TN+FP) x (TN+FN))
