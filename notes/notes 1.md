Scope: slide2 and note1

**key words**: image classification pipeline, NNC algorithm, K-NNC algorithm, validation sets for Hyperparameter tuning.

1. image classification is a concept referring to how to classify an image. There we are given a data set which contains some images and their categories. Our goal is to train a model to predict one category for a new image and measure its accuracy.
2. NNC means Nearest Neighbor classifier. We try to find an image that is nearest to our test image and label it as the same category. To find the nearest image, we can use L1distance or L2 distance.
3. KNN algorithm finds K nearest images and then they vote for the new image's category. NNC and KNN are time-consuming in a test which we can bear.
4. There are some choices such as l1 distance or l2 distance, how large for k. These choices are called Hyperparameters. We can split training data into training data and validation data for we can't use test data to tune them. Cross-validation means we split training data into some(e.g5) folds and then use some folds as training data while others as  validation data. Cross means we then change the training data and validation data to tune hyperparameters.
5. pros and cons.  Obviously,  it's very easy to understand and implement. However, as we said before, it's can spend a lot of time in testing process and this is what we can's bear. Assume that you want to classify a set of images and it can spend a whole day. Moreover, the accuracy of CNN is not very high, in fact it's only near 3 times of wild guess.

 

