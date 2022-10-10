Dataset can be found at https://www.kaggle.com/competitions/dogs-vs-cats/data

This model uses two Convolutional layers, with a 3x3 filter and input size of 128x128. These results are then fed into their respective maxpooling layer, which takes a 2x2 patch of the feature map and calculates a respective maxiumum value. This is done to downsample the feature map and allow for the convolutional layer to recongnize paterns.

The feature map is then flatted from say a (3x3x3) shape to 27 x 1 shape. This is done because how we are feeding the signals into a dense layer which is a fully activated layer to analyse the data give to it. We then drop a random half of inputs to 0 to prevent overfitting.

The final Dense layer is the prediction layer, since this is a binary classification problem we will use a sigmoid activation function and 1 output node.

This model after 10 epochs is able to predict whether an image has a cat or dog with an accuracy of ~85%.
