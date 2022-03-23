## Análise de Correspondência

![Mapa Perceptual](https://support.minitab.com/pt-br/minitab/18/simple_correspondence_row_plot_research_funding.png)

Dentro da área de Aprendizado de Máquina, temos os modelos não Supervisionados, usados quando não temos uma variável alvo. Existem alguns tipos e nesse texto falaremos sobre os Modelos Não Supervisionados que o objetivo é a **Redução da Dimensionalidade** das variáveis do conjunto de dados.

Um desses casos é a Análise de Correspondência, que tem por objetivo reduzir a dimensionalidade do conjunto de dados com base na associação entre as categorias da variável, ou seja é utilizado quando as variáveis se aprensentam de forma **QUALITATIVA**, como resultado obtemos um mapa perceptual com linhas e colunas da tabela de contingência.

Temos uma subdivisão dentro desse Modelo:
* **ANACOR** - Análise de Correspondência Simples
    - Utilizada quando o número de variáveis estudadas for igual a 2.
* **ACM** - Análise de Correspondência Múltipla
    - Utilizada quando o número de variáveis estudadas for maior que 2.

Esse é um método que usa muito a estística por debaixo do panos, por conta dessa associação entre variáveis qualitativas, segue o passo a passo:

1. **Construção da Tabela de Contingência** (tabela que vai fazer o cruzamento par a par entre as categorias de 2 variáveis categóricas)
![Tabela Contingencia](https://image.slidesharecdn.com/iad-aula10-141030080648-conversion-gate02/95/sumarizao-estatstica-2d-variveis-nominais-3-638.jpg?cb=1414656492)
    no caso dessa tabela 2 variáveis categóricas região x sexo -> com região com 5 categorias e sexo com 2 categorias, a tabela mostra a frequência observada do cruzamento de cada par de categorias.
2. **Cálculo das Frequências Esperadas**.
3. **Cálculo dos resíduos**
    - frequencia_observada - frequencia_esperada
4. **Teste qui-quadrado (X²)**

![Fórmulas](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRI-w4Mr0Ff4gbhtGVoVC7AkWfsMOKUT0tB3w&usqp=CAU)

5. **Teste de Hipótese:**
    - H0: Hipótese Nula
        - as variáveis associam-se de forma aleatória
    - H1: Hipótese Alternativa 
        - a associação entre as variáveis não se dá de forma aleatória.

    Existe associação significante a determinado nível de confiança se o valor da estatística for maior que seu Valor Crítica ou p-valor(área vermelha) < 0.05 (depende do nível de significância.)

![qui-quadrado](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcT9VaIJX3mKxaVBUVCEbGzl4HJJb-Aev5dsGw&usqp=CAU)

Se H0 for rejeitada temos ANACOR ou ACM.

Próximos passos são cálculos mais matemáticos (álgebra linear), inclusos aqui mais a base de conhecimento

6. **Calculo Resíduos Padronizados**
    - Intensidade ou magnitude das associações

7. **Calculo Resíduos Padronizados Ajustados**
    - Adota-se valores maiore que 1.96 que é o valor do resíduo na distribuição normal padrão a um nível de significância de 5%.

8. **Decomposição da Inércia Principal Total**
    - Como o X² é muito sensível ao aumento da amostra, fica difícil a decomposição dele. A Inércia Total entra como um artifício para ser realizada essa decomposição.
    Importante nesse momento é o conceito de **eigenvalue**(autovalores) e **eigenvectors** (autovetores)


https://www.professores.uff.br/gbenitez/wp-content/uploads/sites/98/2017/08/Aula_8.pdf - pesquisar melhor futuramente 

https://www.kaggle.com/code/cmcoutosilva/an-lise-de-correspond-ncia-c-mara-dos-deputados/notebook - prática em python para ver melhor

Todo esse matematiquês para chegar no par de de coordenadas para podermos plotar as variáveis no Mapa Perceptual.


