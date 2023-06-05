# Make Circles

Project utilising the Scikit-Learn `make_circles` dataset to classify a multi-class dataset using a simple Neural Network built in TensorFlow 2.X.

## This project uses:
* TensorFlow 2.X to create, train and evaluate the performance of a multi-class classification dataset
* Sequential API to build a simple neural network composed of 3 fully-connected Dense layers with softmax activation
* Decision boundary plotting on the dataset

![image](https://github.com/DavAll22/make_circles/assets/124359152/a57dd78c-1643-4eee-8e20-fd7e97d7e227)


The dataset `make_circles` only has functionality to generate a binary class dataset, however this project combines 2 generated datasets together of different sizes to create one with 3 classes.

The dataset is split in an 80:20 split of training data to test data. The model validates using the test data during the training of the model.

The labels used in the dataset are not one-hot encoded [0, 1, 2] and so in training, `sparce_categorical_crossentropy` is used in the loss function.


## Evaluation

* On the training data, the model achieves a loss of 0.033 and an accuracy of 99.42%
* On the test data, the model achieves a loss of 0.047 and an acucracy of 98.33%

![image](https://github.com/DavAll22/make_circles/assets/124359152/decd2f24-94d0-465e-839f-fddbd8c6a705)
![image](https://github.com/DavAll22/make_circles/assets/124359152/2dc7b58e-e7f8-4f0e-8369-5230428d1a33)

  * The results are dependent on the noise in generating the moons dataset: more noise in the dataset leads to a harder to fit decision boundary and more samples crossing the boundary, increasing loss and reducing accuracy.


## Predictions
* Prediction probabilities for each class is generated from the test data and the corresponding class label is assigned to the maximum prediction from the model
* A confusion matrix is plotted from the predictions
