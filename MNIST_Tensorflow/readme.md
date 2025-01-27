
# Identificação de Dígitos com MNIST

Este é um projeto de aprendizado em Machine Learning, focado na classificação de dígitos manuscritos usando o conjunto de dados **MNIST**. O objetivo deste trabalho é aprender e entender as etapas fundamentais de construção de um modelo de redes neurais convolucionais (CNN) utilizando o framework **TensorFlow/Keras**.

## Objetivo

O principal objetivo deste projeto foi criar um modelo capaz de identificar corretamente os números manuscritos do conjunto de dados MNIST, um dos conjuntos de dados mais conhecidos na área de Machine Learning.

## Etapas do Projeto

### 1. **Carregamento e Pré-processamento dos Dados**

   - O conjunto de dados MNIST foi carregado diretamente através do TensorFlow.
   - As imagens foram normalizadas para garantir que os valores de pixel estivessem entre 0 e 1.
   - Os rótulos (números de 0 a 9) foram convertidos para **one-hot encoding** para facilitar a classificação.

### 2. **Construção do Modelo**

   O modelo foi construído utilizando uma **Rede Neural Convolucional (CNN)**, que é uma das arquiteturas mais eficazes para classificação de imagens. O modelo consistiu nas seguintes camadas:
   - **Camadas Convolucionais**: Detectam características locais das imagens (como bordas, texturas, formas).
   - **Camadas de Pooling**: Reduzem a dimensionalidade das imagens para acelerar o processo e reduzir a sobrecarga computacional.
   - **Camada densa**: Combina as características extraídas pelas camadas convolucionais e realiza a classificação final.

### 3. **Compilação e Treinamento**

   O modelo foi compilado com a função de perda **categorical crossentropy**, e o otimizador **Adam** foi utilizado para otimizar os pesos do modelo durante o treinamento.

   O treinamento foi realizado por **5 épocas**, com o conjunto de dados dividido em lotes (batches) de 64 imagens, utilizando o método **fit()** do Keras.

### 4. **Avaliação do Modelo**

   O modelo foi avaliado com o conjunto de teste, alcançando uma alta precisão de **99.1%**, o que indica que o modelo está bem ajustado para a tarefa de classificação de dígitos manuscritos.

### 5. **Previsões e Análises**

   Após o treinamento, o modelo foi utilizado para prever as classes dos dígitos no conjunto de teste. As previsões foram comparadas com as classes reais para verificar a performance.

### 6. **Salvar o Modelo**

   O modelo final foi salvo utilizando o formato **.keras**, que é o formato recomendado pelo TensorFlow/Keras para salvar modelos treinados.


## Conclusão

A construção do modelo de CNN é bem extensa e cheia de hyperparametros, da pra calibrar de diferentes formas dando grande versatilidade e complexidade, acabei não abordando um tunning ou grid-search para um valor ótimo nesse trabalho para não extender muito, pois o intuito era dar um chute inicial e deixar bem detalhado para possíveis estudos, consultdas.

Ao verificar os erros foi possível perceber o quanto pequenos detalhes podem fazer falta ao dar a correta resposta, isso vai ser feito futuramente em um trabalho a parte de tunning de CNN, provavelmente adicionando mais camadas, neurônios, dando mais opções de função de ativação ou de otimizador, dentre outras alterações.
