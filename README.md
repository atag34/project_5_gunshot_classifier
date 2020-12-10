# Firearm Classification
For my final project in the Metis Data Science Bootcamp I have chosen to build a convolutional nerual net for identifying firearm models based on a gunshot. I will be focusing on the Glock 19 and the Sig Sauer P320 as the primary test case as they are two of the most popular handguns in the US and pose a difficult problem given their similarities in design and caliber. In addition, I would like to explore the ability to use the model for classification in real time of streaming audio.

`model_final.ipynb` contains a notebook showing the structure and results of the final model
`preprocessing_final.ipynb` shows how the preprocessing and augmentation was done, including a pickle of the final dataset in the format we need to the CNN. The end result is our 64 Mel features for each clip.
`scratch_work` contains many of the models tested including a VGG-sh pretained model using the google audioset data. The input restrictions for the model however proved to be diffiult to overcome and return useful predictions or features. 

## Collecting Data
The data was collected from various Youtube videos using Audacity at various qualities and environments. After building a set of about 300 clips, I added additional examples from [Freesound Audio](https://www.kaggle.com/c/freesound-audio-tagging-2019) to prevent the model from identifying all sounds a weapons, and make it more generalizable to real world sound scenarios.

The audio then goes through an augmentation process where gaussian noise is added, each sample is then clipped into half-second chunks and saved as additional observations to help the model work with various audio qualities and learn to identify sections of gunshots without the whole sound.

## Convolutional Neural Network
The model is then built using a similar architecture outlined in a talk [found here.](https://github.com/jonnor/ESC-CNN-microcontroller/blob/master/presentation/presentation.md)

## Live Streaming Audio

