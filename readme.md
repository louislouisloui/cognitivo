### ORGANISACAO

* 01_discover: analise visual do dataset
* 02_preprocessing: Limpeza dos dados
* 03_models: Modelos e resultados

### MODELAGEM

Encarei o problema como uma regressao mesmo que o fato de ter poucas valores discretas me fez pensar num problema de classificacao.
A minha ideia era simplesmente ir testando varios modelos a partir de um data set limpo. Testei os tipos de modelos seguintes:
* Linear regression
 * simples e polynomial(2-5)
 * com regularisacao (Lasso)
* SVM
 * SVC
* Tree
 * RandomForest
* Nearest Neighbour
 * KNearestNeighbour

Pra cada teste, experimentei varios hyperparametros.

### FUNCAO DE CUSTO

Escolhi o erro medio absoluto (MAE) pois ele e pratico pra entender o quanto a predicao fazia sentido. Completei olhando pra o r2 pra ver como performava contra o zeror.

### CRITERIO DE SELECAO

Escolhi o modelo que tinha o melhor MAE gerlaizado, ou pela media do CV ou calculando em cima do testing set.

### VALIDACAO

Usei um CV com 2 folds quando usava o gridsearch e um simple train/test com 0.2 de test no resto dos casos. Basicamente usava o CV quando procurava automaticamente os parametros, e train/test quando so queria testar o resultado final de um modelo. Escolhi um pequeno fold pois o dataset e pequena e tem output raros.

### EVIDENCIAS DESEMPENHO

Comparando o score de geralizacao dos demais modelos, o que me dava o melhor MAE era minha escolha