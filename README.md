# Firearm Classification
For my final project in the Metis Data Science Bootcamp I have chosen to build a convolutional nerual net for identifying firearm models based on a gunshot. I will be focusing on the Glock 19 and the Sig Sauer P320 as the primary test case as they are two of the most popular handguns in the US and pose a difficult problem given their similarities in design and caliber. In addition, I would like to explore the ability to use the model for classification in real time of streaming audio.

## Collecting Data
The data was collected from various Youtube videos using Audacity at various qualities and environments. After building a set of about 300 clips, I added additional clips from [Freesound Audio](https://www.kaggle.com/c/freesound-audio-tagging-2019) to prevent the model from identifying all sounds a weapons, and make it more generalizable to real world sound scenarios. 
