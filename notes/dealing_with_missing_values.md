# Substituição de NA

Porque não apenas tirar fora os dados faltantes?

O grande problema disso é a perda de dados.
* Perdemos informações relevantes em outras colunas. Se apenas um coluna tem NA e jogamos a linha fora, perdemos dados de todas as outras colunas que tinham valores preenchidos.
* Diminuição no volume de dados para o treinamento dos modelos.

Qual a solução?

Substituir os dados faltas.

Temos algumas técnicas para fazer isso:

1. Abordagem de negócio:
* Considera a natureza do problema
* Manter a consistência dos dados
* Considerar o modelo de negócio da empresa

2. Abordagem estatística:
* Introduz um viés aos dados, fortemente baseado na feature. Se tenho 80% das idades faltando e coloca a média nesses dados, estou dizendo que grande parte das pessoas tem a idade média. Isso faz com que o algoritmo aprenda esse viés.

3. Abordagem de machine learning:
* Essa é uma abordagem mais complexa, onde utilizamos modelos de machine learning para preencher os valores faltantes.

