# Image-classification
A Convolutional Neural Network(CNN) binary classifier model.

### For this CNN model to work we have ensured proper preprocessing of images, then the images are trained on fully connected CNNs for future prediction.

https://drive.google.com/drive/folders/1DlQouMrGMgGhK-4ZxkVlHdqzp2C9MYr1?usp=sharing - Drive link for Dataset

* First we import TensorFlow libarary and the ImageDataGenerator class from Keras.Preprocessing.image module.

* In the data preprocessing part we transform the the training and test images by using image augmentation method which is done by the the image data generator class.  This reduces overtraining that is overfitting of images while training.


* while building the CNN model, 

  * First we initialise the sequential class of models module.
  * Now we add the convolutional layer with the help of Conv2D class and apply ReLU activation function. 
  * Next we use MaxPool2D class to add pooling layer to the neural network for getting better feature maps. 
  * To enhance our feature maps we add second convolutional and pooing layers then we flatten it and then use a full connection layer by using Dense class of layers module and finally we add an output layer having an sigmoid activation function.


* Before training the CNN model we compile all the layers by using adam optimizer and assign loss and metrics parameters as required. Then we train the CNN model by using the fit method and also define the number of epochs. The CNN model training is little bit different from other ML model's training.


* To make a single prediction,

  * first we import the numpy library and then we import the image class from the the preprocessing submodule from the keras library. 
  * Then load the image and assign a target size same as what we used for training input images and assign loaded image to a variable named test_image.  
  * Now by using image_to_array method we convert the test_image to matrix format. Now we add a fake dimension which corresponds to the batch size i.e.32 on which the model was trained done by using np.expand_dims method.
  * Before predicting the test_image matrix is divided by 255.0 as we applied feature scaling to the training set.

> training_set.set.Class_indices gives the indices (e.g.0/1/2...) of every target classes on which model was trained.
