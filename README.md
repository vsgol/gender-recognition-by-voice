# Gender recognition by voice
Test task at huawei 

Due to time constraints there is nothing here yet, but it will be updated over time 

## Preparing Dataset

We will use [Mozilla's Common Voice Dataset](https://www.kaggle.com/mozillaorg/common-voice). Most of the audios are already tagged, so I will only use them for now. Then we can use unlabelled audio for further training

Each audio file is sliced into 5-second segments and the main characteristics of the audio segment, such as average frequency, standard deviation of frequency, first and third quantiles, etc., are highlighted. To increase the accuracy, only the frequencies 40hz-280hz are kept, as these are the frequencies of the human voice. 

If the classifier accuracy proves insufficient, more features can be extracted from each audio, such as the average value of the fundamental frequency or the average value of the dominant frequency. It is also possible to change the length of the segments into which each segment is divided

## Training models

I balanced the number of female and male voice examples and trained the following patterns

* Decision Tree
* Random Forest
* Gradient Boosting
* Support Vector Machine
* Multilayer Perceptron

Currently 84% accuracy is achieved on Multilayer Perceptron and Support Vector Machine. More accuracy (90%-95%) can probably be achieved with better sampling of parameters from datasets, but dataset processing takes too much time

Next, it is necessary to compare type I and type II errors, and see the importance of each parameter. 
