# Deep-Fakes Forgery Detection

*NOTE*: Download apk file and trained model files from [here](https://drive.google.com/open?id=1TGB4C_XhPj5eqxWBe6VVmBdqH7aLcf_Q).

## About the Dataset

Please download the labeled dataset using the dataset provided by download script(FaceForensicsDownloadScript provided by the official team) for training.
Due to the signed agreement with the FaceForensics team, I am constrained to share only a fraction of it for the demonstration purposes. 

## Model v0.1

This model is built using transfer learning on the inception model. (Although other models got more accuracy, this model was easily integrable with android NDK) 

Run retrain.py to train on images  
```
python retrain.py
```
To save the trouble of collecting/preparing data and training, I am including the trained model [Click-here](https://drive.google.com/open?id=1TGB4C_XhPj5eqxWBe6VVmBdqH7aLcf_Q).

The trained model is included into the android app code to run real-time. It takes the live video frames from the rear camera and classifies whether it is forged or genuine.

You can test it directly without installing the app by just passing the test image through the model.
Just run real_label.py file with the input image for the inference.
```
python real_label.py forged.jpg
```

## Android application 

I am also including the android apk file [here](https://drive.google.com/open?id=1TGB4C_XhPj5eqxWBe6VVmBdqH7aLcf_Q) which is a complete app which showcases the fuctionality of the mentioned neural network model. Try it with forged and genuine videos in the repository.

Other than the classical usage of Android SDK, this app also uses Android NDK for the integration of the model into it.

This app is developed on the official tensorflow android demo app.


### Dependencies:

- Tensorflow and its related dependencies
- Python 
- Android studio 
