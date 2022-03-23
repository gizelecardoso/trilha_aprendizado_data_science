## Análise de Cluster

![Analise Cluster](http://4.bp.blogspot.com/-h8or7zxPK9w/UnvMaVbl6TI/AAAAAAAAAHw/HFsaXeyeEpA/s1600/Cluster.JPG)

Dentro da área de Aprendizado de Máquina, temos os modelos não Supervisionados, usados quando não temos uma variável alvo. Existem alguns tipos e nesse texto falaremos sobre os Modelos Não Supervisionados que o objetivo é a **Agrupamento** das observações em Grupos.

A análise de cluster tem por objetivo agrupar as observações em grupos que sigam as seguintes características fundamentais:
    - Semelhantes entre si - homogêneos
    - Distintas entre grupos - heterogêneos
Como?
    Através de alguma medida de distância (variável quantitativa) ou semelhança (variável binária)
    Medidas de distâncias utilizadas: Euclidiana, manhattan, minkowski, etc
    Medidas de semelhança: Emparelhamento simples, jaccard, dice, etc 

A análise pode ser feita com Métodos:

* Hierárquicos
* Não-Hierárquicos

## Hierárquicos
    
- O algoritmo é capaz de fornecer mais de um tipo de partição de dados.
- Existem 5 técnicas de como particionar os dados
    - Vizinho mais próximo
    - Vizinho mais longe
    - Média
    - Centróide
    - Incremento soma dos quadrados

O resultado dessas partições pode ser observada através de um gráfico chamado **Dendograma**

![Analise Cluster](https://www.edrawsoft.com/images/creatediagram/dendrogram-template.png)

No dendograma conseguimos visualizar os grupos sendo formados.
Exemplo: 
- De acordo com a imagem na distância 16,5 - temos 2 grupos:
    - Grupo 1: 12,23,19,10,7,9,34
    - Grupo 2: 28,21,13,14,9,12,18,7

- Conforme diminui a distância, aumenta o número de grupos.