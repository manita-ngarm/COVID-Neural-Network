# COVID-Neural-Network

Predicting Covid-19, Normal and Viral Pneumonia Cases Using Convolutional Neural Networks and Radiography by 
Shane Corson, 
Shane Calla, 
Yibo Li, 
Wenhui Liu, 
Manita Ngarmpaiboonsombat 
Each section wrote their own readme in their individual sets of files.

https://github.com/monkeyweather/COVID-Neural-Network

Method

  - We did the data augmentation by using an image datagenerator to rotate, shift, shear, scale changes, and flip images to get the overall increment in the
  generalization of the model. 
  
  - After that, we trained the dataset on the GoogleLenet and VGG16 model as our original plan. 
  
  - Moreover, we also experimented on Inceptionv3+ResNet, VGG19, and transfer learning and fine tuning on Inception v3 model with the same setting in order to  compare the model performance
  
  - GoogleLenet
  
    - Used the inception v3 pre-trained model from keras library
    
    - Trained the last 20 layers of the module (considering t-learning first, then apply fine-tuning with a small learning-rate) with 30 epochs 
    
    - Added GlobalAveragePooling2D and dense layer
    
    - Used the categorical-crossentropy as loss function with softmax activation function in the last layer of CNN
    
  - VGG16
    - Used the VGG16 pre-trained model from keras library
    
    - Trained model with 10 epochs
    
    - Added average pooling operation for spatial data
    
    - Flattened input
    
    - Set up densely connected layer with relu activation function
    
    - Applied dropout layer
    
    - Used the categorical-crossentropy as loss function with softmax activation function in the last layer of CNN
