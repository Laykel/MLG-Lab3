# Machine Learning: Practical work 03 - Speaker recognition using Neural Networks and

_Supervised Learning_

_Teacher: Andres Perez-Uribe (Email: andres.perez-uribe@heig-vd.ch)_

_Assistants: Hector Satizabal (Email: hector-fabio.satizabal-mejia@heig-vd.ch), Yasaman Izadmehr (Email: yasaman.izadmehr@heig-vd.ch)_

## Introduction

During the previous practical work sessions, we provided you with a series of notebooksexplore the workings of an artificial neuron (e.g., the Perceptron model), neural networks
(Multi-layer Perceptrons or MLPs) and Backpropagation, which allows those system to
“learn from examples”.

The subsequent practical work consisted on applying a methodology for evaluating the
performance of the trained neural networks on new data (e.g., hold-out validation and
cross-validation), with the aim of selecting a final model to deal with the problem at hand.
The selection of a model consists on finding the model of appropriate complexity (e.g.,
which is related to the number of parameters or synaptic weights) and configuration (e.g.,
type of activation function, learning rate, momentum rate, training iterations, etc).

## Practical work

To evaluate a given neural network topology (e.g., 1 hidden layer, 2 hidden neurons, tanh
as activation function) and configuration (e.g., learning rate = 0.001, momentum = 0.7) we
need to split the dataset in two to define a training and a test subsets, for instance by
randomly choosing 80% of the data for training, and 20% for test.
Then, we train the neural network iterating over the training data several times (e.g.,
number of epochs).

However, performing this only once, might not give a good idea of the generalization
capability of the trained neural network, since the 80%-20% split for training and test is
random. Therefore, we usually split the dataset into two parts several times (e.g.,
N_SPLITS) and compute a mean of error to assess the performance of the trained neural
network.

But, every time we train and test a neural network on a given train dataset, we start with
random weights, thus evaluating it based on a single trial is not enough, therefore, we have
to train several times (N_INITS) the neural network randomly initializing the weights every
time.

