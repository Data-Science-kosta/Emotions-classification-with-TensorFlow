# Emotions Classification with TensorFlow
![emotions](https://github.com/Data-Science-kosta/Emotions-classification-with-TensorFlow/blob/master/garbage/emocije.gif)
##### This is a fully convolutional neural network that classifies 8 different emotions from a given images.
##### The program works in real time through the desktop camera.
### DATA:
For training this network 2 datsets were used:

1: https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data

2: https://www.pitt.edu/~emotion/ck-spread.htm
### TRAINING:
The network was first trained on the CK dataset. Images in that set are all taken in the perfect environment, camera position, lights, contrast... On that dataset model easily achieves 99% accuracy on the test set, but when you test it in the real environment (through the desktop camera) it fails to predict half of the emotions accurately. That was espected because distribution of the data used for training is way too different from the distribution used for testing. One more downside of this dataset is that it is quite small. So the next step was to get more data which has similar distribution as the data in the real environment. So FER datset was joined with CK dataset and the model was trained. The accuracy improved greatly, but unfortunately not enough because the FER datset contains a lot of wrongly labeled examples and a lot of images which are not even a faces. 
Next steps would be creating my own dataset that consits of images taken in the real environment and retraining the network.
### RUN:
Run the **main.py** and choose what you want to do:
"1" to extract the faces from images and to drop images with unclear emotion (CK dataset)
"2" to split the data into the train,test and validation (CK dataset)
"3" to process and split fer 2013 dataset
"4" to load the CK dataset
"5" to load the FER dataset
"6" to start training
"7" to load both datasets and to start training
"8" to load pretrained weights, and test them on the desktop camera
"e" to exit
### NOTE:
Datasets and pretrained network weights were to big to push them on the Github.
