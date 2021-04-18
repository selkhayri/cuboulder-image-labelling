# cuboulder-image-labelling
Categorising traffic sign

## Purpose
The goal of this project was to label traffic sign image

## Dataset
The data for this project was contained in two numpy files: X_npy, containing the 32,209 32x32-pixel RGB images, and y_npy containing the image classifications into 42 (0-41) categories.

## Data Munging

The npy files were loaded into the following numpy arrays:

* X_npy, a 4-D array 39,209 x 32 x 32 x 3
* y_npy, a 2-D array 39,209 x 43

Since the predictor dataset consisted of image data, there was no need to check for null values.

## Machine Learning

### Prep

The data was split in three: training, validation, and test datasets.

### Training

The training dataset was used to train Deep Neural Network model which consisted of the following layers:

* A convolutional input layer, using relu activation
* A Dense output layer, consisting of 43 nodes, one for each classification value

And the following hidden layers:

* An additional convolutional layer, using relu activation
* A Maxpooling layer, using relu activation
* A Dropout layer, using relu activation
* 4 Dense layers, using relu activation

Accuracy was used to evaludate the effectiveness of the model.

The following accuracy values were achieved during training:

* Training Data: 99.45%
* Validation Data: 97.68%

### Prediction and Testing

After training was completed, the model was used to predict the test target values with an accuracy of 97.34%.





