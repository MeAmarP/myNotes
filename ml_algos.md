### XGBoost:stands for eXtreme Gradient Boosting.

1. XGBoost is an optimized distributed gradient boosting library designed to be highly efficient, flexible and portable.
2. XGBoost is an implementation of __*gradient boosted decision trees*__ designed for speed and performance.
3. XGBoost provides a parallel tree boosting (also known as GBDT, GBM) that solve many data science problems in a fast and accurate way.

* What makes the XGBoost so popular?
    + Speed and Performance.
    + core algorithm is parallelizable.
    + It has both linear model solver and tree learning algorithms. So, what makes it fast is its capacity to do parallel computation on a single machine.
    + state of the art performance in many ML tasks.
    + **Sparsity**: it accepts sparse input for both tree booster and linear booster, and is optimized for sparse input
    + **Speed**: it can automatically do parallel computation on Windows and Linux, with OpenMP. It is generally over 10 times faster than the classical gbm.
    + **Customization**: it supports customized objective functions and evaluation functions.

+ XGBoost dominates structured or tabular datasets on classification and regression predictive modeling problems.
+ Boosting is an ensemble technique where new models are added to correct the errors made by existing models. Models are added sequentially until no further improvements can be made. 

#### Refer:
+ https://medium.com/@imoisharma/gentle-introduction-of-xgboost-library-2b1ac2669680
+ https://machinelearningmastery.com/gentle-introduction-xgboost-applied-machine-learning/


