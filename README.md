# Wine_quality

Definição da estratégia de modelagem

A estratégia para modelagem consistiu em uma análise inicial para explorar os dados. Com essa análise exploratória, verifiquei que alguns valores não eram válidos e limpei os dados. Além disso, como existiam dois tipos de vinho e as distribuições das variáveis eram bem diferentes entre os tipos, criei dois data frames. Com isso, trabalhei e ajustei um modelo para cada tipo de vinho. Antes de começar com os ajustes dos modelos, normalizei as variáveis para todas ficarem com média 0 e desvio-padrão igual a 1. Esse passo é importante pois todas as variáveis ficam na mesma escala e a diferença entre os intervalos de valores não é afetada. Esse pré-processamento evita que variáveis com grandes valores influenciem o modelo de predição.


Função de custo

Como testei diversos modelos, a função de custo muda para cada um deles. O modelo com 
a melhor acurácia foi o de Random Forest. Para ambos modelos, vinhos tintos e brancos, a função de custo utilizada foi entropia, escolhida através da técnica de grid search. 

Seleção do modelo

O modelo selecionado foi o que obteve melhor acurácia para predizer a qualidade do vinho. Testei diversos modelos e no final escolhi o modelo de Random Forest. Esse modelo obteve a melhor acurácia tanto para os vinhos brancos quanto para os vinhos tintos. Para escolher os melhores hiperparâmetros do modelo para a base de dados analisada utilizei a técnica de grid search onde diversos parâmetros são testados e os melhores são escolhidos.

Validação do modelo

Para validar o modelo separei a base de dados em treinamento e teste. A base de teste consistiu de 20% dos dados que não são utilizados para treinar o modelo. Os 80% restantes são utilizados para treinar o modelos. Para calcular a qualidade do modelo, a base de teste é utilizada. Desse modo, ao testar a predição do modelo com dados que o mesmo não conhece, conseguiremos verificar a verdadeira performance do mesmo.

Qualidade do modelo

O modelo final teve ~68% de acurácia para predizer a qualidade dos vinhos brancos e ~70% para predizer a qualidade dos vinhos tintos.
