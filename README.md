# Genetic Algorithm to Optimize an Artificial Neural Network

[![Genetic Algorithm and Artificial Neural Network Article](https://ieeexplore.ieee.org/document/5614106)]

The goal these implementations are show the matter of a genetic algorithm to optimizating. The file was done in [![Colab](https://colab.research.google.com)]  plataform. The use of an artificial neural network with some layers hidden to classified some thing is relevant. It was done a study about some approaches to artificial neural network architecture that it is important, for instance the values that are predict cannot to be different them: 

- Depth = [1,2,3,4,5,6,7,8,9,10]

- Neurons_per_layer = [16,32,64,128,256,512,1024]

- Activations = ["tanh","softmax","relu","sigmoid"]

- Optimizer = ["sgd","rmsprop","adagrad","adadelta","adam","adamax","nadam"],

- Losses=[ "mean_squared_error","mean_absolute_error","mean_absolute_percentage_error","mean_squared_logarithmic_error","squared_hinge","hinge","categorical_hinge","logcosh","categorical_crossentropy","sparse_categorical_crossentropy","binary_crossentropy","kullback_leibler_divergence","poisson","cosine_proximity"]



However,the utilizing the genetic algorithm refered in the implementation as "DNA" have the intuite of optimize the architecture parameters. The parameters that were consideraded: 

```sh
- DNA[0] = Depth

- DNA[1] = Neurons_per_layer

- DNA[2] = Activations

- DNA[3] = Optimizer

- DNA[4] = Losses 
```

In which, each array position represent an network parameter. Another relevant methodology is the mean of every array component about "architecture_DNA" variable. 

```sh
architecture_DNA[0] = Depth

architecture_DNA[1] = Input_layer with: [0] = neurons, [1] = activation

architecture_DNA[2 to Depth-1*] = Hidden layer with: [0] = neurons, [1] = activation  

architecture_DNA[Depth] = Output layer activation

architecture_DNA[-1] = Hyperparameter with: [0] = loss, [1] = optimizer
     
Depth-1 last hidden layer since last layer is output layer*
```

# Use of genetic Algorithm in action 

After of you do run evolution execution, you will look some genetic algorithm approach, for instance: 

### Mutation will hapeness now!

```sh
 After mutation  [9, [32, 'relu'], [512, 'selu'], [32, 'softsign'], [512, 'softplus'], [32, 'elu'], [256, 'elu'], [512, 'relu'], [1024, 'selu'], 'sigmoid', ['mean_squared_error', 'nadam']]
 ```

### Mutation will hapeness now!

Every time that happeness this is because the genetic operates are optimizating the network parameters. 

## WARNING! 

The following parameters have convergence direct about network: 

```sh
 population_size 
 mutation_rate 
 generations 
 Epochs=2
 batch_size
 verbose

```

Good luck to understood this implementation. 
