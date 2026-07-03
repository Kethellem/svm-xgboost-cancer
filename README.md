O projeto tem como objetivo comparar dois modelos de Machine Learning — SVM e XGBoost — aplicados ao diagnóstico de câncer de mama utilizando o conjunto de dados Breast Cancer Wisconsin. Os dados foram carregados diretamente da biblioteca sklearn, que já fornece o dataset limpo, mas ainda assim foram realizados passos de preparação importantes, como padronização das variáveis com StandardScaler, já que o SVM é sensível à escala, e divisão dos dados em treino e teste mantendo o balanceamento das classes com stratify. Também foi aplicada uma análise exploratória usando PCA com dois componentes para visualizar a separação entre tumores benignos e malignos.

Na modelagem, dois algoritmos foram treinados. O SVM foi configurado com kernel RBF e parâmetro C igual a 1, sendo adequado para fronteiras não lineares, mas dependente da padronização dos dados. Já o XGBoost foi treinado com 200 árvores, taxa de aprendizado de 0.1 e profundidade máxima igual a 4, apresentando boa performance sem necessidade de padronização e sendo eficiente para conjuntos maiores. Após o treinamento, foram geradas visualizações como o gráfico PCA, matrizes de confusão para ambos os modelos e a curva ROC comparando o desempenho das duas abordagens.

Os resultados mostraram que ambos os modelos tiveram bom desempenho no diagnóstico, mas o XGBoost apresentou acurácia ligeiramente maior e melhor AUC na curva ROC, indicando maior capacidade de generalização. O SVM também teve excelente performance, porém depende mais do pré-processamento. A análise via PCA reforçou que existe uma separação clara entre as classes, o que explica o bom desempenho dos modelos.

A estrutura do projeto inclui o arquivo README na raiz, o notebook dentro da pasta src, os gráficos gerados dentro da pasta img e uma pasta opcional docs para documentação adicional. Para executar o projeto, basta abrir o notebook no Google Colab, instalar as dependências necessárias e executar as células, que gerarão automaticamente todas as visualizações.

svm-xgboost-cancer/
│
├── README.md
│
├── src/
│   └── projeto_svm_xgboost.ipynb
│
├── img/
│   ├── pca.png
│   ├── matriz_svm.png
│   ├── matriz_xgb.png
│   └── roc.png
│
└── docs/ (opcional)
