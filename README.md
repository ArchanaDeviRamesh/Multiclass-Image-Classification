# Multiclass-Image-Classification

Multiclass Image Classification in predicting the type of shoe using Convolutional Neural Network(CNN) with transfer learning

# Repository folders 

* "data" folder contains the following 

  -- train dataset with 711 images 
  
  -- test dataset with 114 images
  
  -- Each folder has 3 subfolders for the classes of shoes namely Adidas, Converse, and Nike

* "code" folder contains the .py and .ipython files of the implementation

* Please create a folder "Metaverse" in google drive and place the zipped files of train and test data set and run the code 

# Design decisions

* The over all approach:
    * CNN with transfer learning is used with VGG16 being one of the most popular pretrained models trained on the large dataset called Imagenet. 
    * Since the initial layers of a CNN train on only low-level and mid-level features such as edges, lines, borders, etc., these characteristics of a pre-trained         CNN can be used here using the method of transfer learning. 
    * Therefore instead of creating a neural network from scratch we transfer the learned features that is the weights of the network 
    * Initially the class distribution of both training and test dataset is plotted, from which it can be seen that the classes are evenly distributed
    * More details are mentioned as comments within the code 

* Preprocessing 
    *  For preprocessing of images, the blog https://blog.keras.io/building-powerful-image-classification-models-using-very-little-data.html was referred. 
    *  Since the dataset has less amount of images, data augmentation of images can be performed inorder to improve the performance of the model
    *  This blog describes about the ImageDataGenerator class which is the Keras API to perform data augmentation and it has various parameters for doing different types of transformations like randomly rotate pictures, randomly translate pictures vertically or horizontally, randomly zooming inside pictures etc. 
  
 * Training and Evaluation 
    * The training dataset is split as 80% for training and 20% for validation and the model is run for 30 epochs. 
    * Optimization method used is Adam with learning rate 0.01, loss function is categorical cross entropy as evaluation metric used is accuracy
    * The training and validation loss and accuracy are plotted. 
    * From the graphs it can be seen that both training and validation loss decreases with the number of epochs, therefore overfitting is not there
 
 * Testing
    *  The test dataset is used to calculate the testing acuuracy of the model
    *  Predictions are calculated and the accuracy is reported

