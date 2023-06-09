# Network

![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/acd40942-ae2e-4c62-8604-fc52c2f79238)


#### [for excel file click here](https://abc.com)

![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/06d6c5bc-96fb-4394-aa4c-390ecda31376)

<b>Backpropagation</b>  is an algorithm used to train artificial neural networks. It is a key component of gradient-based optimization methods, such as stochastic gradient descent, that enable neural networks to learn from labeled training data.

The goal of backpropagation is to adjust the weights and biases of a neural network's connections in order to minimize the difference between the network's predicted output and the desired output. This difference is quantified by a loss function, which measures the network's performance on the training data.

Backpropagation works by computing the gradient of the loss function with respect to each weight and bias in the network. This gradient represents the direction and magnitude of the change needed to reduce the loss. The algorithm propagates this gradient backward through the network, starting from the output layer and moving towards the input layer.

During the backward pass, the gradient is computed using the chain rule of calculus. At each layer, the gradient is multiplied by the derivative of the activation function applied to the layer's input. This process allows the algorithm to attribute the contribution of each connection to the overall error.

Once the gradients are computed, the weights and biases are updated in the opposite direction of the gradient, thereby minimizing the loss function. This update step is typically performed using an optimization algorithm, such as stochastic gradient descent, which adjusts the parameters based on the gradients and a learning rate.

By iteratively performing forward passes to compute predictions and backward passes to update the parameters, backpropagation enables a neural network to learn from examples and improve its performance over time. It is a fundamental technique in modern deep learning and has been instrumental in the success of various applications, including image recognition, natural language processing, and many others.
Backpropagation is used for training neural networks. It involves two main steps: forward propagation (Loss Calculation) and backward propagation (Step Calculation).


## Steps
### 1. Forward Propagation:
![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/897d333d-c693-4239-93cb-ddb1a3324400)

- We start by feeding an input through the network. In this case, we have an input layer of size 2 where we feed the two inputs i1 and i2.
- Each neuron in the hidden layer takes the weighted sum of its inputs, applies the sigmoid activation function to the sum, and passes the result to the neurons in the output layer.
- Similarly, each neuron in the output layer takes the weighted sum of its inputs (outputs from the hidden layer), applies the sigmoid activation function, and produces the final output values a_o1 and a_o2.
- Ultimately, we compare the network's output to the target output t1 and t2 using the mean squared error loss function.

### 2. Backward Propagation:

![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/12207569-ce57-4192-8b4c-f8e79f86149a)

![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/14f1d310-36f9-4499-ae5d-20f61c8cb4d0)


- Here we calculate the gradients of the loss function with respect to the weights and biases of the network.
- Starting from the output layer, we propagate these gradients backward through the network, updating the weights and biases using a technique called gradient descent.
- The update for each weight and bias is determined by the gradient and a learning rate, which controls the magnitude of the update.
- The process of updating the weights and biases based on the gradients is repeated iteratively for a number of epochs or until the network converges to a satisfactory solution.
- The steps of backpropagation involve calculating the partial derivatives of the loss function with respect to the weights and biases in each layer. These partial derivatives are computed using the chain rule of calculus, which allows us to propagate the gradients backward through the network.

By iteratively adjusting the weights and biases based on the gradients, backpropagation helps the neural network learn the appropriate parameters to minimize the loss function and make accurate predictions.

## Effects of learning rate
- Up to a certain limit increasing learning rate increases convergence rate. It even starts achieving 0 loss after LR=2.

![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/a33c9a3d-7b3e-4850-a176-ee2ef333619d)


- But after that increasing learning rate causes the network to have trouble converging. As you can see for LR=1000, loss is permanently stuck at upper ceiling of 0.25 after first step.

![image](https://github.com/tsdeepak/cnn-mnist/assets/375801/0fe5ba97-e500-4e1a-91b9-b4f74f924d45)
