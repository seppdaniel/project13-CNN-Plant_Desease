## Projeto 13: Deep Learning - Convolutional Neural Network - Plan Desease System

Neste projeto, criarei uma rede neural convolucional que será capaz de prever se uma planta está sofrendo de alguma doença. Usaremos diferentes 'Layers' e outros hiperparâmetros para construir, treinar e testar este modelo de classificação. 

Usarei Python, Tensorflow e Keras para este projeto.

Passo a passo:
- Neste projeto, criaremos uma rede neural convolucional que será capaz de prever se uma planta está sofrendo de alguma doença. 
- Usaremos diferentes camadas e outros hiperparâmetros para construir, treinar e testar este modelo de classificação. estaremos usando tensorflow e Keras para este projeto
- Processo de importação de todas as bibliotecas necessárias. Como estamos fazendo um modelo CNN, importaremos todas as camadas necessárias, ativações, otimizadores, etc.

1 - Visualizando as imagens que iremos trabalhar
  - Agora vamos observar algumas das imagens que estão em nosso conjunto de dados. Vamos plotar 12 imagens aqui usando a biblioteca matplotlib.
  
2 - Descobrir a média das dimensões e redimensionar todas as imagens de acordo
  - Depois de visualizar as imagens, vamos avançar e criar uma função que converterá as imagens em um array numpy. É necessário porque normalizaremos nosso conjunto de dados depois disso.
3 - Convertendo as imagens em um array Numpy e normalizando-as
  - A gora vamos converter todas as imagens em array numpy.
    
4 - Verificando o desequilíbrio da classe
  - Também observaremos o número de imagens em diferentes classes para ver se o conjunto de dados está balanceado ou não
  - Em seguida, observaremos a forma da imagem
  - Verificando o número total de imagens que é o comprimento da lista de labels.

5 - dividindo os dados e realizando 'one hot encoding'
  - Em seguida, usaremos sklearn train_test_split para dividir o conjunto de dados em dados de teste e treinamento. Aqui, tomei o tamanho do teste como 0,2, então meus dados serão divididos em 80% de treinamento e 20% de dados de teste.
  - Agora vamos normalizar o conjunto de dados de nossas imagens. Como os valores de pixel variam de 0 a 255, dividiremos cada pixel da imagem por 255 para normalizar o conjunto de dados.
 
6 - Criando a arquitetura do modelo, compilando o modelo e depois ajustando
  - Em seguida, criaremos uma arquitetura de rede para o modelo. Usamos diferentes tipos de camadas de acordo com suas características, nomeadamente Conv_2d (É usado para criar um kernel convolucional que é convoluído com a camada de entrada para produzir o tensor de saída), max_pooling2d (É uma técnica de downsampling que tira o valor máximo sobre a janela definida pelo poolsize), flatten (achata a entrada e cria uma saída 1D), Dense (a camada densa produz a saída como o produto escalar da entrada e do kernel).
  
7 - plotando a precisão e perda contra cada época/geração
  - Nessa parte, salientar que usamos computação evolucionária para simular 50 épcas/gerações, o que nos resultou numa acurácia de 0.70
  - Ao compilar o modelo, precisamos definir o tipo de perda que será Binary Crossentropy para o nosso modelo, juntamente com isso, também precisamos definir o otimizador e as métricas, respectivamente.
  - Ajustar o modelo com os dados e descobrir a precisão em cada época para ver como nosso modelo está aprendendo. Agora vamos treinar nosso modelo em 10 épocas e um tamanho de lote de 128. Você pode tentar usar mais número de épocas para aumentar a precisão, mas aqui podemos ver que o modelo já alcançou uma precisão muito alta, então não precisamos executar isso por mais. Durante cada época, podemos ver o desempenho do modelo, visualizando a precisão do treinamento e da validação.
 
8 - Pré-processar os dados de teste e fazer previsões sobre eles
  - Salvando o modelo usando diferentes técnicas.
  - Avaliar o modelo para saber a precisão do modelo.
  
9 - Visualizando os rótulos originais e previstos para as imagens de teste
  - Em seguida, usaremos nosso modelo para prever o rótulo do conjunto de dados de teste.
  - Imprimindo a classificaão original e a classificação prevista para avaliação

Conclusão
A humananidade precisa aumentar a produção de alimentos em cerca de 70% até 2050 para alimentar uma população estimada em mais de 9 bilhões de pessoas. Atualmente, as doenças infecciosas em plantas reduzem o rendimento potencial em uma média de 40%, com muitos agricultores no mundo em desenvolvimento experimentando perdas de rendimento de até 100%. A ampla distribuição de smartphones entre produtores agrícolas em todo o mundo, com a expectativa de 5 bilhões de smartphones, se tornou uma ferramenta valiosa para diversas comunidades que cultivam alimentos. Uma aplicação potencial é o desenvolvimento de diagnósticos de doenças por meio de Machine Learning.
