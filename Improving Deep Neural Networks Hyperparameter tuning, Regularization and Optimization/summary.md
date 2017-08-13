#### Improving Deep Neural Networks: Hyperparameter tuning, Regularization and Optimization
- Be able to effectively use the common neural network "tricks", including initialization, L2 and dropout regularization, 
Batch normalization, gradient checking, 
- Be able to implement and apply a variety of optimization algorithms, such as mini-batch gradient descent, Momentum, RMSprop and Adam, and check for their convergence. 
- Understand new best-practices for the deep learning era of how to set up train/dev/test sets and analyze bias/variance 
- Be able to implement a neural network in TensorFlow.

----------------------------
**Hightlights**

1. Zeros initialization -- setting initialization = "zeros" in the input argument.
2. Random initialization -- setting initialization = "random" in the input argument. This initializes the weights to large random values.
initializing with overly large random numbers slows down the optimization.
3. He initialization -- setting initialization: sqrt(2./layers_dims[l-1]).)
4. Different initializations lead to different results
5. Random initialization is used to break symmetry and make sure different hidden units can learn different things
6. Don't intialize to values that are too large
7. He initialization works well for networks with ReLU activations.
8. one epoch (one pass through the training set)
9. Adam is one of the most effective optimization algorithms for training neural networks. It combines ideas from RMSProp (described in lecture) and Momentum.
10. Momentum usually helps, but given the small learning rate and the simplistic dataset, its impact is almost negligeable. Also, the huge 
**oscillations** you see in the cost come from the fact that some minibatches are more difficult thans others for the optimization algorithm.
Adam on the other hand, clearly outperforms mini-batch gradient descent and Momentum. If you run the model for more epochs on this simple dataset, all three methods will lead to very good results. However, you've seen that Adam converges a lot faster.
Some advantages of Adam include:
Relatively low memory requirements (though higher than gradient descent and gradient descent with momentum)
Usually works well even with little tuning of hyperparameters (except $\alpha$)
11. During hyperparameter search, whether you try to babysit one model (“Panda” strategy) or train a lot of models in parallel (“Caviar”) is largely determined by:The amount of computational power you can access
12. After training a neural network with Batch Norm, at test time, to evaluate the neural network on a new example you should:Perform the needed normalizations, use μ and σ2 estimated using an exponentially weighted average across mini-batches seen during training.
13. L2 regularization makes your decision boundary smoother. If $\lambda$ is too large, it is also possible to "oversmooth", resulting in a model with high bias.
14. L2-regularization relies on the assumption that a model with small weights is simpler than a model with large weights. Thus, by penalizing the square values of the weights in the cost function you drive all the weights to smaller values. It becomes too costly for the cost to have large weights! This leads to a smoother model in which the output changes more slowly as the input changes.
15. The cost computation: A regularization term is added to the cost
16. The backpropagation function: There are extra terms in the gradients with respect to weight matrices
17. Weights end up smaller ("weight decay"):Weights are pushed to smaller value
18. dropout is a widely used regularization technique that is specific to deep learning. It randomly shuts down some neurons in each iteration. 
19. A common mistake when using dropout is to use it both in training and testing. You should use dropout (randomly eliminate nodes) only in training.
20. Apply dropout both during forward and backward propagation.
21. Tensorflow is a programming framework used in deep learning
22. The two main object classes in tensorflow are Tensors and Operators.
23. When you code in tensorflow you have to take the following steps:
* Create a graph containing Tensors (Variables, Placeholders ...) and Operations (tf.matmul, tf.add, ...)
* Create a session
* Initialize the session
* Run the session to execute the graph
* You can execute the graph multiple times as you've seen in model()
* The backpropagation and optimization is automatically done when running the session on the "optimizer" object.
