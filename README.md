# FashionMNISTClassifier

## The Neural Network

This convolutional neural network (CNN) classifies an article of clothing based on an image. The model will predict a list of 10 elements (indices zero through nine), where each value in the list represents the probability that the image is a representation of that index number. In other words, given an input image, the model outputs a list [*probability_index_is_zero*, *probability_index_is_one*, *probability_index_is_two*, ... *probability_index_is_eight*, *probability_index_is_nine*]. The element with the highest probability means that the index of that element (an article of clothing mapped to 0 - 9) is the model's prediction. Since the model is a multi-label classifier (it classifies which clothing article an image contains), it uses a sparse categorical crossentropy loss function and has 10 output neurons (one for each class). The model uses a standard Adam optimizer with a learning rate of 0.001 and has an architecture consisting of:
- 1 Flatten layer (with an input shape of [28, 28] since each image is 28 x 28 pixels) 
- 2 Hidden layers (each with 128 neurons and a ReLU activation function)
- 1 Output layer (with 10 output neurons and a softmax activation function)

Feel free to further tune the hyperparameters or build upon the model!

## The Dataset
The dataset is an MNIST included within keras and contains approximately 70,000 (60,000 images in the train set and 10,000 images in the test set) 28 x 28 pixel images of human clothing and is included within the **fashion_classifier.py** file.

## Libraries
This neural network was created with the help of the Tensorflow library.
- Tensorflow's Website: https://www.tensorflow.org/
- Tensorflow Installation Instructions: https://www.tensorflow.org/install

