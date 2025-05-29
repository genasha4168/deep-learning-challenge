#
# Deep Learning Challenge: Charity Funding Predictor

#
# Overview:
The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not \
applicants for funding will be successful. With knowledge of machine learning and neural \
networks, we must use the features in the provided dataset to create a binary classifier that is \
capable of predicting whether applicants will be successful if funded by Alphabet Soup. 

**Results:** \
To begin the data processing we removed any irrelevant information. After dropping EIN and \
NAME the remaining columns were to be considered features for the model. Name was added \
back into the second test for binning purposes. The data was then split for training and testing \
sets. The target variable for the model was labeled “IS_SUCCESSFUL” and has the value of 1 \
for yes and 0 for no. APPLICATION data was analyzed and “CLASSIFICATION value was used \
for binning. We used several data points as a cutoff to bin “rare” variables together with the new \
value of “Other” for each unique value. Categorical variables were encoded by `get_dummies()` \
after checking to see if the binning was successful. 

# 
# Compiling, Training, and Evaluating the Model:
There were three layers total for each model after applying Neural Networks. The number of \
hidden nodes were dictated by the number of features. \
![alt text](Images\image.png)
477 parameters were created by a three-layer training model. The first attempt was just over \
73% accuracy which was under a desired 75% but not too far off. \

![alt text](Images\image1.png)

![alt text](Images\image2.png)

**Optimization:** \
The second attempt with the “NAME” column in the dataset, achieved an accuracy of more than \
79%. This is 4% over the target 75% with 3,298 parameters.
![alt text](Images\image3.png)

Multiple layers should be used for deep learning models since it learns how to predict and \
classify information based on computer filtering inputs through layers.

![alt text](Images\image4.png)