# Multilayer Perceptron

A Multilayer Perceptron (MLP) was implemented directly in numpy to classify the data of the three classes in the Iris Database.

The perceptron has a hidden layer, that is, it is made up of:

* the input layer (the data in R^4),

* a hidden layer with at least 40 neurons, and

* the output layer that has 3 outputs (three neurons).


The output y_pred is a three-dimensional vector with values between [0,1] and sum to one. y_pred[k] can be interpreted as the probability that data x in R^4 belongs to class k.

The true labels "y" were coded "one-hot" and the cost function between the predictions vector y_pred and the actual label vector is the Cross Entropy.

The training algorithm implemented stochastically and with a sample size (lots) equal to at least one was the descending gradient with fixed step size. That is, if you use batch size size 1, a piece of data is passed through the network, the gradient with the loss is calculated, and the weights are updated. If you use samples larger than size 1, the gradients corresponding to each data item in the sample that passes through the network are averaged.

Apart from this, an elastic net regulation method was implemented. Also added a method which adds bias to the neurons in each layer
