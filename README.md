This repository contains the Google Colab notebooks I wrote as my attempt at this Kaggle challenge on music genre classification: 

https://www.kaggle.com/competitions/kaggle-pog-series-s01e02

The melspec_generator notebook unzips the data from my Google Drive, loads it, and prepares the data for training.

Using the librosa library, I generatr melspectograms for each audio file which I then save in .npy format on my google drive.

The training_pipeline notebook then uses this preprocessed data to train a Recurrent Convolutional Neural Network, with the help of a custom data loader class.

I used tensorflow and keras to build my model however in the future I am thinking of using PyTorch with FastAI as I have seen other people achieve good results with these. 
I was unable to intall the Tensorflow-IO dependency as my version of Python is too recent. 
This, coupled with the limits of my machine (8GB RAM) meant that I found it difficult to train large amounts of data without crashing. I elected to save the model after training smaller
sets of data and the reload the model in a different runtime. As of yet, I have not trained the model on the entirety of the data and as such the model is not very effective.


