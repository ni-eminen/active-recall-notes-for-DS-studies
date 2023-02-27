# Active recall for neural network composition

## Perceptron

### What is a perceptron
A perceptron consists of two layers; the input layer and the output layer. A perceptron in itself is an artificial neural network. It is meant to mimic binary configurations of inputs with specific binary outputs. A perceptron is a linear classifier, and can be used to predict outputs on a hyperplane. Provided by chatGPT, here is a Python program for a perceptron, including how it is trained and used to predict.

	import numpy as np

	class Perceptron:
	    def __init__(self, input_size, lr=1, epochs=10):
		self.W = np.zeros(input_size+1)
		self.epochs = epochs
		self.lr = lr
	    
	    def activation_fn(self, x):
		return 1 if x >= 0 else 0
	    
	    def predict(self, x):
		x = np.insert(x, 0, 1)
		z = self.W.T.dot(x)
		a = self.activation_fn(z)
		return a
	    
	    def fit(self, X, d):
		for _ in range(self.epochs):
		    for i in range(d.shape[0]):
			x = np.insert(X[i], 0, 1)
			y = self.predict(X[i])
			e = d[i] - y
			self.W = self.W + self.lr * e * x


	# Training data
	X = np.array([[0, 0], [0, 1], [1, 0], [1, 1]])
	d = np.array([0, 0, 0, 1])

	# Create perceptron object
	p = Perceptron(input_size=2)

	# Train the perceptron
	p.fit(X, d)

	# Test the perceptron
	print(p.predict([0, 0]))  # Output: 0
	print(p.predict([0, 1]))  # Output: 0
	print(p.predict([1, 0]))  # Output: 0
	print(p.predict([1, 1]))  # Output: 1


### How does a perceptron work
A perceptron makes predictions based on weights, that have been adjusted in the training phase of developement. The perceptron is trained by feeding it a number of inputs and target outputs, from which it determines the correct weights based on its loss function. For example, if it was fed an input vector [0, 1], that should return 0 as prediction, yet the perceptron predicts 1 as output, the loss for the prediction is prediction - target = 1 - 0 = 1. Based on the loss, the perceptron can make a correction in its weights. 

### What is a neuron
