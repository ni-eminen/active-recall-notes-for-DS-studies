# Neural network architectures

## Hidden layers and back-propagation
The perceptron has limited capability in creating estimations. For example, it is a linear classifier and can't even mimic the XOR operand. While there are other ways to overcome this, such as providing it with a product of the two inputs that represent the XOR input as a third input, this can be overcome with the use of hidden layers. Hidden layers are layers between the input layer (the retina) and the output layer. 
### What is a layer
A layer is a set of neurons that are estimated in parallel.
### What are hidden layers
A hidden layer is a layer in between the input and the output layer. There can be as many hidden layers as the engineer desires. Adding hidden layers dramatically increase the computation power necessary for producing predictions. In the beginning of the research in this field, scientists struggled with setting the weight within the hidden layers to correctly represent the data. That was until back-propagation was introduced. 

### What can hidden layers accomplish
Hidden layers can make the neural networks nonlinear.

### What is back-propagation

## Feed-Forward Neural Network
A feed-forward NN is a neural network that doesn't form cycles between its nodes. It is one of the most simple architectures for neural networks.

## Recurrent neural network
RNN's nodes can form cycles, which allows for an ouput of an earlier input to affect the output of subsequent inputs. RNNs can take an unlimited series of inputs, which makes them particularly applicable to problems like speech recognition and handwriting recognition.
RNN's learn not only during training, but also while processing new inputs.

## Convolutional NN


## Deconvolutional NN

## Modular NN

## Transformers
The transformer model was introduced in Google Brain's paper "Attention is All You Need" in 2017. The transformer model is solely based on multi-head and self attention layers, where no recurrence is needed. The transfomer uses an encoder-decoder architecture. Transformers are significantly faster to train than their predecessors, that used attention in conjunction with convolution and recurrent layers. Since the paper was released, transformers have been used for a wide range of problems from video and audio to text.
