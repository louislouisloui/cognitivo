### ORGANISACAO

* 01_discover: analise visual do dataset
* 02_preprocessing: limpeza dos dados
* 03_models: modelos e resultados

### MODELAGEM

Encarei o problema como uma regressao. Porem o fato de ter poucas valores discretas pode eventualmente deixar um classificador ser um racional interessante.
A minha ideia era simplesmente ir testando varios tipos de modelos a partir de um data set limpo. Testei os tipos de modelos seguintes:
* Linear regression
 * simples e polynomial(2-5)
 * com regularisacao (Lasso)
* SVM
 * SVR
* Tree
 * RandomForest
* Nearest Neighbour
 * KNearestNeighbour

Pra cada teste, experimentei varios hyperparametros na medida do possivel (CPU local).

### FUNCAO DE CUSTO

Escolhi o erro medio absoluto (MAE) pois ele e pratico pra entender o quanto a predicao fazia sentido.

### CRITERIO DE SELECAO

Escolhi o modelo que tinha o melhor MAE sobre um CV de 10 folds. Gostaria de testar com varios valores de fold diferentes pois o fato de ter casos raros pode deixar os folds nao representativos.

### VALIDACAO

Usei um CV com 10 folds sem restricao particular sobre as observacao pois elas sao independentes

### EVIDENCIAS DESEMPENHO

Comparando o score de geralizacao dos demais modelos, o que me dava o melhor MAE era minha escolha. Olhei tambem os residuos pra entender como o modelo se comportava a respeito dos erros.