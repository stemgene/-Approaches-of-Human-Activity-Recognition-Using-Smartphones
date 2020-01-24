# Approaches-of-Human-Activity-Recognition-Using-Smartphones

Human Activity Recognition (HAR) aims to identify the actions carried out by a person given a set of observations of him/herself and the surrounding environment. Recognition can be accomplished by exploiting the information retrieved from various sources such as environmental or body-worn sensors. Smartphones are bringing up new research opportunities for human-centered applications where the user is a rich source of context information and the phone is the firsthand sensing tool.

In this project, the data from sensors is collected to indicate six activities. In order to distinguish these activities, I implement several approaches of HAR refering the paper from Anguita et al.

Firstly, I apply SVM with three kernels and Random Forest on the dataset to predict the HAR. After fine tuning, the classification accuracy of SVM with Polynomial and Gaussian kernel and Random Forest is 98%-99%, which are better than the results from original paper a little bit.

From the perspective of confusion matrix, all models perform excellent at distinguishing movement from static status, and there isn’t any false positive between these two states. however, they always make a couple of mistakes to tell the difference between “Sitting” and “Standing”.

Then I implement two approaches to reduce the dimension of dataset. For the first method, I sort the features by their importance, and keep 90% of information complement. There are so many correlated features, I omit features of greater than 95% correlation and the dataset is reduced to 76 features. The accuracy of three models is lower than it of full dataset slightly.

The second method of reducing dimension is PCA. Comparing to the previous method, the effectiveness is worse, especially for SVM, the accuracy is 6% lower. Among the accuracy of three models after implementing PCA, the best one is Random Forest.

If we want to achieve the accuracy of 90%, the minimum number of principal component will be around 10-30.

Overall, these models can make excellent classification of HAR, even work on the dataset with compressed dimension.
