## Assignment 1 for END2 Course:

The notebook file implemented a neural network with following specs.
- Implements XOR gate functionality
- make sure there are in total 44 parameters
- run it for 2001 epochs

### Contributors:
- Chaitanya Vanapamala
- Pralay
- Pallavi
- Ritambhra Korpal


## 1. What is a neural network neuron?
Neuron is a basic building block of a neural network. The Neurons in an Artificial Neural network are mathematical model of biological neurons in our brain.
A neuron simply takes the inputs which are numbers always, and applies boosting/attenuation mechanism using the weights for each respective input connection.
When we pass input to the neuron it does the weighted sum and then passes the sum to activation function. The activation step makes the output state of neuron. The following diagram illustrates the blocks in a neuron

![Neuron]()

Z = f (X1*W1+X2*W2+X3*W3)  - Where f is the activation function.

## 2. What is the use of the learning rate?
Before knowing the use of learning rate, let’s first know what learning rate is. Learning rate is the step size by which the weights & bias of the neural network are updated in the training process.
Rightly choosing learning rate will help us to find the minima of error. Learning rate also impacts the training time. A neural network learns from training data by gradient decent algorithm, which finds the optimal weights & biases where the error is min.

![Gradient Decent]()

Having small learning rates makes us enormous time to converge and find the optimal weights, on other hand if we choose high learning rate which will make drastic updates to the weights and we might miss out the valley point. So, choosing a right learning rate is crucial.

## 3. How are weights initialized?

The training and convergence of a neural network is dependent on how the weights of each node are initialised. The most proven way is to initialise the weights randomly, and these random numbers will be normally distributed with mean 0 and standard deviation of 1.
Why we have to make random initialisation and why not zeros or constant value. When we initialise weights as zero, the output of all the neurons will be same in each layer and also the gradient which will lead us to a symmetry problem. And we never optimise the weights and never reach the local minima/global minima.

## 4. What is "loss" in a neural network?

The loss is the measure the difference between predicted output of neural network and the original output. In a classification problem the loss can be understood as how many observations are predicted with wrong class compared to the original class.
“Loss” is what we try to minimise the training process. Loss will be calculated after end of each epoch and weights are updated based on the gradient of loss. The function which is used to find the loss is call loss function. Based on our Problem, there are wide verities of loss functions available such as:
- Mean square error.
- Mean absolute error.
- Cross entropy.
- Sparse categorical cross entropy.

## 5. What is the "chain rule" in gradient flow?

In neural network, the gradient of the loss is propagated backwards in order to find out the new values for the weights. This gradient flow is called back propagation.
Lets see a neural network with 2 inputs (x1, x2) and 1 hidden layer with 2 neurons and output layer with 1 neuron.
H – Weighted sum of input and weights associated with the node.
Z – Activated Weighted Sum, i.e., activation function will be applied on weighted sum H.

![Neural Network]()

Lets see the H and Z values at each neuron.

![Network Functions]()

In order to find the error gradient with respect to W111, we have to back propagate error from Z3 to input X1 node (Highlighted lines in above image). The chain rule from calculus helps us to find the gradient easily. As the intermediate H and Z values are composite function. We can use the chain rule.

![Gradient Error]()
