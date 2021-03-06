# Caffe-Speaker-Recognition
Convolutional Neural Network to recognize the speaker from a spoken number dataset.

##Dataset
The dataset includes audio spectrogram of 24 different speakers, speaking 0-9 numbers. 
Training set has the total of 3500 records and Testing set includes the total of 1080 records.
Dataset Link http://pannous.net/spoken_numbers.tar

##Model
Convolutional Neural Network consists of 5 convolution layers, 3 fully connected layers with ReLu and Max-Pooling in between. 

##Deep Learning Platform Used
Caffe

##Training Steps
Executed the following command from Caffe root folder to train the model.

build/tools/caffe train --solver = speaker_recognition/solver.prototxt

##Accuracy
Achieved 99% accuracy in 5000 iterations.

##Classification
Executed the following command from Caffe root folder for classification the "0_Karen_160.png" which is a spectrogram of user "Karen" speaking number '0' by using the trained model.

build/examples/cpp_classification/classification.bin speaker_recognition/numbers_deploy.prototxt speaker_recognition/numbers_iter_5212.caffemodel speaker_recognition/train_mean.binaryproto speaker_recognition/synset_numbers.txt speaker_recognition/0_Karen_160.png

##Reference
https://github.com/pannous/caffe-speech-recognition
