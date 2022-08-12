### A convolutional neural network(CNN) consists of four layers-Convolution, pulling, flattening, full connection(ANN).
 
* In the convolutional layer, the model uses various feature detectors, feature detectors are basically a matrix that finds features that humans may not find easily on those input images to generate various feature maps.
Now we use the ReLU rectifier function to increase non-linearity to the neural network.

* In the 2nd layer, there are various poolings like mean pooling, max pooling, mean pooling. It reduces the size but returns the important features so the model can perform faster. Reducing unuseful features helps in decreasing overfitting.

     https://www.cs.ryerson.ca/~aharley/vis/conv/flat.html (experiment with feature maps)

* In the 3rd layer, pooled feature maps are flattened into a vector which is used as inputs for the ANN used in the next layer.
 
* Finally we use a a fully connected artificial neural network.

![B16326_12_06](https://user-images.githubusercontent.com/85345738/138188862-ff09951a-7ece-4563-a8bf-b4e7d96a0f6f.png)

Loss functions for Neural Networks
----------------------------------
> **Regression**- Mean squared error(mse)

> **Classification** - cross-entropy(when softmax is used), softmax ensures if one class has a probability of x then the other class will have a probability of 1-x.
