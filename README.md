# CancerPrediction
The purpose of this project is to create a machine learning model that can learn and predict whether the breast cancer tumours would become malignant through a large dataset provided (https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+%28Diagnostic%29). The dataset comprises various observable parameters of the breast cancer tumours, such as the radius, smoothness, concavity of the tumours and others. The logistic regression, a machine learning model that can be applied to predict a classifcation problem has been selected for this case. 

In order to speed up the training process, the correlation between the parameters was examined via pair plot and correlation table as shown follows.
![image](https://user-images.githubusercontent.com/69382649/186183614-076ad023-4d1c-4c5c-a604-4b026f17c2f9.png)
Figure 1: pair plot
![image](https://user-images.githubusercontent.com/69382649/186183928-76700491-7b29-49ad-8f1d-afcb9a1f83fe.png)
Figure 2: correlation table heat map

It was found that the parameter, radius was highly correlated with perimeter and area while the parameter, concavity was highly correlated with concave. Thus, one parameter from each of two highly correlated groups abovementioned was selected while the remaining were eliminated to reduce the burden for machine learning. Thus, the new correlation table was shown as follows.
![image](https://user-images.githubusercontent.com/69382649/186184993-77fbf3af-dacd-4735-96ff-01a30f93b0a5.png)
Figure 3: correlation table heat map

The model was eventually trained using the functions provided from the library of Scikit-learn, and eventually produced the accuracy of 95.6%!

The code can be found in the file 'cancer_prediction'.
