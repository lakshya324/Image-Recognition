# Image Recognition System by CNN

This Image Recognition system is based on Convolutional Neural Networks (CNN) and is designed to distinguish between images of cats and dogs. It achieves an accuracy of up to 85.2% when trained on a dataset consisting of images of cats and dogs. The system has also been tested with random images of cats and dogs from the internet and has provided accurate results.

## Dataset
The dataset used for training and testing the model can be downloaded from the following link:
[Download Dataset](https://drive.google.com/file/d/13f0229odj0eBzXMj87H7_EE6dMZcpRQJ/view?usp=sharing)

## Dependencies
- TensorFlow: 2.12.0
- Keras

## Part 1: Data Preprocessing

### Preprocessing Training Set
The training data is preprocessed using the Keras ImageDataGenerator, which performs the following transformations:
- Rescaling: Scales pixel values to be between 0 and 1.
- Shear Range: Applies shear transformations.
- Zoom Range: Applies zoom transformations.
- Horizontal Flip: Randomly flips images horizontally.

### Preprocessing Test Set
The test data is preprocessed in a similar way to the training data, including rescaling.

## Part 2: Building the CNN

### Initializing the CNN
The Convolutional Neural Network (CNN) model is created using the Keras Sequential API.

### Step 1 - Convolution
The first convolutional layer is added to the model with 32 filters, a kernel size of 3x3, and ReLU activation.

### Step 2 - Pooling
Max-pooling is applied after the first convolutional layer to reduce dimensionality.

### Adding Second Convolutional and Pooling Layer
An additional convolutional layer with max-pooling is added to enhance feature extraction.

### Step 3 - Flattening
The pooled feature maps are flattened into a 1D array for input into the fully connected layers.

### Step 4 - Fully Connected Layers
The CNN includes a hidden layer with 128 units and ReLU activation, followed by an output layer with a sigmoid activation function.

## Part 3: Training The CNN

### Compiling CNN
The CNN is compiled with the Adam optimizer and binary cross-entropy loss for binary classification. Accuracy is used as a metric.

### Training CNN Model
The model is trained on the training set and evaluated on the test set for 25 epochs.

## Part 4: Predictions

### Making Predictions
You can use the model to make predictions on new images using the `finder` function provided. Pass the address of the image you want to classify, and it will return 'Dog' or 'Cat' based on the prediction.

Example usage:
```python

if finder('image_url.jpg'):
  print('Dog')
else:
  print('Cat')
```
