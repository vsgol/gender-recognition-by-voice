# Gender recognition by voice
Test task at huawei 

Due to time constraints there is nothing here yet, but it will be updated over time 

## Preparing Dataset

We will use [Mozilla's Common Voice Dataset](https://www.kaggle.com/mozillaorg/common-voice). Most of the audios are already tagged, so I will only use them for now. Then we can use unlabelled audio for further training

Each audio file is sliced to equal lengths and the main features of the audio section are highlighted, such as mean frequency, standard deviation of frequency, first and third quantile and etc

If the accuracy of the classifier proves insufficient, you can also remove noise from the audio (all frequencies outside 0hz-280hz), and allocate more features from each audio, such as average of fundamental frequency or average of dominant frequency
