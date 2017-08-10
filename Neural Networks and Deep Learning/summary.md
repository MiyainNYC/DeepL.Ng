 ### Neural Networks and Deep Learning
 - Understand the major technology trends driving Deep Learning 
 - Be able to build, train and apply fully connected deep neural networks 
 - Know how to implement efficient (vectorized) neural networks 
 - Understand the key parameters in a neural network's architecture 
----------------------------
**Hightlights**

1. **np.dot(a,b)** performs a matrix multiplication on a and b, whereas **a*b"** performs an element-wise multiplication.

2. A neuron computes a linear function (z = Wx + b) followed by an activation function

3. Logistic Loss: ![Alt text](https://github.com/MiyainNYC/Green-cab-ridership/blob/master/charts/methodology.png)

4. The tanh activation usually works better than sigmoid activation function for hidden units because the mean of its output is closer to zero, and so it centers the data better for the next layer.

5. For forward propagation for layer l, where 1≤l≤L, If to initialize the weights and biases to be zero, Each neuron in the first hidden layer will 
perform the same computation. So even after multiple iterations of gradient descent each neuron in 
the layer will be computing the same thing as other neurons: **initial weights should be non-zero as well as zero.**

6. **hyperparameters**: number of iterations; learning rate α; number of layers L in the neural network; size of the hidden layers;

7. **Weight Dimension**:

