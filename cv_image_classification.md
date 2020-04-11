### Fighting Imbalanced class data.
+ Over sampling under represented classes, and under sampling over represented classes are both options, the latter if you have enough data.
+ Another approach is to initially train on an unbalanced dataset and then fine tune with a balanced dataset, though I can’t see that working always.
+ the class_weights argument in model.fit, which you can use to make the model learn more from the minority class.
+ reducing the size of the majority class.
+ **accepting the imbalance. Deep learning can cope with this, it just needs lots more data (the solution to everything, really).**
+ Adaptive synthetic sampling approach for imbalanced learning (ADASYN): ADASYN generates synthetic data for classes with less samples in a way that datasets that are more difficult to learn are generated more compared to samples that are easier to learn.
+ **Synthetic Minority Over-sampling Technique (SMOTE): SMOTE** involves over sampling the minority class and under sampling of the majority class to get the best results.

#### Refer
+ https://forums.fast.ai/t/how-to-deal-with-unbalanced-data-classes-in-image-classification/14343/2
+ https://stackoverflow.com/questions/41648129/balancing-an-imbalanced-dataset-with-keras-image-generator
+ https://medium.com/neuralspace/kaggle-1-winning-approach-for-image-classification-challenge-9c1188157a86