### Bias and Variance:

+ **Bias** refers to assumptions in the learning algorithm that narrow the scope of what can be learned. This is useful as it can accelerate learning and lead to stable results, at the cost of the assumption differing from reality.
+ **Variance** refers to the sensitivity of the learning algorithm to the specifics of the training data, e.g. the noise and specific observations. This is good as the model will be specialized to the data at the cost of learning random noise and varying each time it is trained on different data

+ More bias in an algorithm means that there is less variance, and the reverse is also true.
+ Many machine learning algorithms have hyperparameters that directly or indirectly allow you to control the bias-variance tradeoff.


+ Reduce Variance in a Final Machine Learning Model
    + A problem with most final models is that they suffer variance in their predictions.
    + The bias-variance trade-off is a conceptual idea in applied machine learning to help understand the sources of error in models.

+ Sources of variance in a final model:
    1. The noise in the training data.
    2. The use of randomness in the machine learning algorithm,Common Examples.
        + Choice of random split points in random forest.
        + Random weight initialization in neural networks.
        + Shuffling training data in stochastic gradient descent.

**Measure Algorithm Variance:**
The variance introduced by the stochastic nature of the algorithm can be measured by repeating the evaluation of the algorithm on the same training dataset and calculating the variance or standard deviation of the model skill.    

**Measure Training Data Variance:**
The variance introduced by the training data can be measured by repeating the evaluation of the algorithm on different samples of training data, but keeping the seed for the pseudorandom number generator fixed then calculating the variance or standard deviation of the model skill.