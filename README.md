# ensemble-methods-on-breast-cancer-data
I applied the bagging and boosting methods using the decision tree as the base predictor on the sklearn’s breast cancer data set. I experiment with different parameters and report the results obtained.

## Experiments

### Bagging Classifier
I trained and tested various Bagging Classification models. The parameters i.e. n_estimators and max_samples, were different for all these models. Following are the values experimented with:
- n_estimators: 25, 50, and 100
- max_samples: 15, 25, and 50

### AdaBoost Classifier
I trained and tested various AdaBoost Classification models. The parameters i.e. n_estimators and learning_rate, were different for all these models. Following are the values experimented with:
- n_estimators: 10, 30, and 50
- learning_rate: 0.02, 0.03, and 0.04

## Results

### Analysis of the Bagging Classifier
- Five bagging classifier models were trained with different parameters. The parameters that were changed across these classifiers were n_estimators and max_depth.
- From the plot of testing accuracy, it can be observed that the fifth bagging classifier outperformed all the other bagging classifiers even though the training accuracy of the fifth bagging classifier was just around 95%.
- It can be claimed that there is not much change in the testing accuracy when the max_depth across the clssifiers is same. However, the testing accuracy jumps up when the max_depth is increased.
- It can be claimed that there is no change in the testing accuracy when the n_estimators are variated from 25 to 50, but the testing accuracy jumps up when the n_estimators increases to 100.
- The third, fourth, and the fifth bagging classifier have a great performance on the testing set and can be regarded as close to ideal classifiers because the testing set accuracy is either equal to or greater than the training set accuracy. However, the first and the second bagging classifier are slightly overfitting the training data and therefore they are not able to generaliize well.

### Analysis of the AdaBoost Classifier
- Five boosting classifier models were trained with different parameters. The parameters that were changed across these classifiers were n_estimators and learning_rate.
- From the plot of training accuracy, it can be observed that for all the models, 100% training accuracy was achieved.
- From the plot of testing accuracy, it can be observed that the first boosting classifier outperformed all the other boosting classifiers.
- It can be claimed that the accuracy decreases with the increase in the n_estimator.
- It can be claimed that there is no change in the testing accuracy when the learning_rate is slightly increased while keeping the n_estimators constant.
- The boosting classifiers here can be seen as overfitting the training data as there performance is not good on the testing set i.e. models are not able to generalize well.
