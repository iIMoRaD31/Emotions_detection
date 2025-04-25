# Emotions_detection
This is an implementation of a model that predicts emotions from live webcam 

I used transfer learning in the process. I got the weights of an already trained model (VGG16) which is a a deep convolutional neural network architecture which is very good at feature extraction. I added other layers to it and trained it using the FER-2013 dataset.
Then I used OpenCV for video processing and face detection (using OpenCv's Haar Cascade).
The hardest part about this project, is actually finding the best way to load data and using to train the model without crashing the program. I tried first to train the model with one emotion at a time, but it failed. Then got the idea of cutting the dataset, that is I only used 1070 images from each emotion and train the model with them at once, which still didn't give a high accuracy since I need more epochs, but the even with around 30% accuracy is was working quite fine. The purpose of my project isn't to reach high accuracy but it's to try to deal with this big amount of data and find a way to get acceptable results.

In case you wanted to use this code and you have 16 GB of RAM, I would recommend you to run the training on more epochs and load to x_train and y_train more than 1070 images (you can do 2070).
