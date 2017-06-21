# Cardiac Arrythmia ML
## Machine Learning Engineer Nanodegree

### Install

This project requires **Python 3** and the following Python libraries installed:

- [Keras](http://www.keras.io/)
- [Tensorflow](http://tensorflow.org/)
- [Numpy](http://numpy.org/)
- [Scipy](http://scipy.org/)
- [Matplotlib](https://matplotlib.org/)





You will also need to have software installed to run and execute a [Jupyter Notebook](http://ipython.org/notebook.html)

You could just install [Anaconda](http://continuum.io/downloads) distribution of Python, which already has the above packages and more included. 


### Run

In a terminal or command window, navigate to the top-level project directory  (that contains this README) and run one of the following commands:

```bash
ipython notebook CardiacML\ Final.ipynb
```  
or
```bash
jupyter notebook CardiacML\ Final.ipynb
```

This will open the Jupyter Notebook software and project file in your browser.


## Data

The heartbeat recording can be downloaded from [here](https://physionet.org/physiobank/database/challenge/2016/). The dataset contains about 3500 recording but we will only use about 1000 due to memory and computation constraints. After converting the .wav recordings into spectrogram images, the training dataset has 800 images (of which 400 belong to abnormal and 600 to normal class) and test set contains around 225 images(80 of abnormal and rest belong to normal class).



## About

The focus of this project is to classify whether the patient has “normal” or “abnormal” heart sound from the Phonocardiogram (PCG) or heartbeat recordings to quickly identify patients who would require further diagnosis.  This is a supervised learning problem since we already know if the heart sound in training dataset is normal or abnormal. The basic idea is to convert each heart sound recording(wav file) to a spectrogram image and train a Convolutional Neural Network over those images. Then given a new PCG recording, we will be able to classify it as normal or abnormal.

The model (Convolutional Neural Network) takes images as input. So we first need to convert the recordings into spectrogram images. This is taken care by 'convert_to_spectrogram.py' which is present in the same repostiory as this notebook. Hence before experimenting with this notebook, it is required to run 'convert_to_spectrogram.py'. It will automatically put the images in the following folder structure as shown below. (Note : It is manually required to create empty folders according to structure). The techniques inolved to convert recordings into spectrogram images are discussed in the capstone report.

The dataset used for this capstone is available freely as part of the PhysioNet / Computing in Cardiology Challenge 2016 which focuses on automatic classification of normal / abnormal phonocardiogram (PCG) recording. Along with clean heart sounds, the dataset also contains some noisy recordings. The samples have been obtained from both normal subjects and pathological patients, providing a variety of signal sources

