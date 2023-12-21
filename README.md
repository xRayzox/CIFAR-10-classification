# CIFAR-10-classification
Classification dataset CIFAR-10 classification 



## Importing Libraries
- TensorFlow library and Keras API are imported for creating the neural network model.
- matplotlib, numpy, and math libraries are imported for plotting images, handling multi-dimensional arrays, and performing mathematical operations respectively.

## Loading and preparing the data
- The CIFAR-10 dataset is loaded using the datasets module from keras.
- The dataset is divided into training and testing set.
- The image arrays are rescaled by dividing by the maximum RGB value (255.0) to normalize the pixel values in the range 0-1.

## Creating the model
- A Sequential model is defined, which allows layers to be added to it in sequential order.
- Convolutional layers, applying the mathematical operation of convolution, are added to the model to allow it to find patterns in image data.
- MaxPooling layers are included to reduce the spatial dimensions (width and height), while retaining the important information.
- The Flatten layer is used to convert the multidimensional output into a vector by applying mathematical flattening process.
- Dense layers, a type of fully connected layer applying linear transformation and followed by a non-linear activation function, are added.

## Configuring the model
- 'adam' optimizer is used. It implements the Adam algorithm—an extension of stochastic gradient descent, mathematically designed for rapid and efficient training.
- 'sparse_categorical_crossentropy' is used as the loss function, a specific mathematical function suitable for multiclass classification problems.

## Training the model
- The model is trained on the training set, with the number of epochs set to 5. The choice of 5 epochs makes the trade-off between accuracy and computational time.

## Evaluating the model
- After the model is trained, it is applied to the testing data to generate predictions. This process involves matrix multiplication fused with activation function—a non-linear transform—for each layer.
- The sklearn library's classification_report function is used to provide precision, recall, f1-score and support—key metrics to evaluate performance.
- Then, a plot of one of the testing samples is generated to visualize the model's prediction using matplotlib's imshow function.

## Prediction
- Determining the class for a specific instance from the test set involves feeding the instance into the model and obtaining the output probabilities. These are then transformed with the argmax function—a fundamental mathematical operation, which outputs the class with the highest probability.
