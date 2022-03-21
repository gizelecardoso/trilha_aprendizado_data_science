## Regressão Logística

![Grafico Logistica](https://aprenderdatascience.com/wp-content/uploads/2020/08/Untitled-design-3-1.png)

Ainda dentro dos módulos supervisionados temos a Regressão Logística.

Que ao contrário da Regressão Linear, a variável dependente, precisa ser **QUALITATIVA**, com isso é estimada a probabilidade de determinado evento(y) acontecer em função de x's variáveis explicativas.

Na Regressão Logística a variável dependente que se apresenta na forma qualitativa pode ser do Tipo:
    - Binária: existem duas categorias 0 (não evento) ou 1 (evento).
    - Multinomial: mais de duas categorias.

Regressão Logística, entra nos Modelo chamados de **Classificação**, pois iremos calcular a probabilidade de uma observação cair em uma classe(categoria, rótulo), etc.

Equação Regressão Logistica

![Equação Logistica](https://aprenderdatascience.com/wp-content/uploads/2020/08/Untitled-design-4-1-520x245.png)

Qual a chance(probabilidade) de um evento **y** em razão de uma ou mais variáveis **x**.

Dentro da equação temos algumas informações importantes:

* **e** -> número de euler - numero irracional e positivo, cujo logaritmo na sua base é chamado natural e = exp(1) = 2,718....  

* **g(x)** -> como expoente do numero de euler tem-se o negativo g(x) que é chamado de **LOGITO**, e é a equação linear (alfa + beta1.x1) sem erro com uma ou mais variáveis explicativas.

* **p(y=1)** ->  p é a probabilidade no caso de y ser 1, ou seja a probabilidade de ocorrência do evento.

* essa fórmula parte da tranformação do ln(chance) onde a chance é igual a p / 1-p (evento sobre não evento).

## Estimação do Parâmetros:

1. Máxima Verossimilhança
    Em estatística é o método para estimar os parâmetros de um modelo. A ideia é encontrar os valores que maximizam a probabilidade dos dados amostrados.


### Análises de Ajuste do Modelo

Após rodarmos o modelo alguns outputs são usados para validar o quão bom o modelo é.

1. LogLik (Log Likelihood - Verossimilhança)
    Qualidade do ajuste, é análogo ao R² na Regressão Linear sem os resíduos.
    Probabilidade de valores de acerto entre valores reais e previstos, a partir da estimação dos parâmetros levando em consideração determinada função densidade probabilidade da y aderente.

    Para Binária - Distribuição Bernoulli
    Para Multinomial - Distribuição Binomial

### Testes Estatísticos
1. X²
    -2 *(llo - llmod)
    - llo = log lik do modelo nulo (somente com intercepto)
    - llmod = log lik do modelo

    - X² é análogo ao F no OLS

    - p-valor < 0.05


2. AIC (Akaike Info Criterion)
    - -2* llmod + 2K (onde K, numero de parâmetros incluindo alfa)
    - na comparação de modelos, escolhe com menos AIC

3. BIC
    - -2* llmod + K.ln(N)
    - na comparação de modelos, escolhe com menos BIC


4. Matriz de Confusão

    Tabela que mostra o desempenho do modelo de classificação;

    ![Matriz de Confusão](https://diegonogare.net/wp-content/uploads/2020/04/matrizConfusao-600x381.png)

    Com base na Matriz de Confusão, podemos calcular:

    - Sensibilidade / Sensitividade:
        - Taxa de Acerto do Evento

            TP / (TP + FP)

    - Especificidade:
        - Taxa de Acerto do Não Evento

            TN / (FN + TN)

    - Acurácia
        - Quão bom o modelo é

            (TP + TN) / N

5. Curva ROC

    Baseada nos valores de sensitividade x 1 - especificidade

    ![Matriz de Confusão](https://i.ytimg.com/vi/MLq5xWNq-T8/maxresdefault.jpg)

    AUC - área abaixo da curva - quanto mais próximo de 1 ou 100% melhor.

    - Coeficiente de GINI


## Comparar Modelos

- Teste de Razão de Verossimilhança

- Teste de Delong

**Modelagem Principio da Parcimônia**



