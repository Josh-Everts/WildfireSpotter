# WildfireSpotter
## Overview
WildfireSpotter is a lightweight wildfire detection model employing image masking to extract salient features and classify an image as having a wildfire inside it, or not. The model is trained on data from the FLAME dataset, created by Shamsoshoara et al. Their paper which outlines their data creation and modeling approach can be found [here](https://arxiv.org/pdf/2012.14036v1.pdf). 

## Approach
Many others have attempted wildifire detection using deep-learning approaches, but as of yet few lightweight (feature-based) approaches have been tried. In my script I outline different salient features, and use simple classifiers (KNN and a logistic model) to perform a binary classification between fire images and non-fire images. 

## Results
As outlined in the notebook script, my approach results in a 75.7% accuracy on the included test data, which closely matches the 76% achieved using a CNN (Shamsoshoara et al.). This means that the lightweight features and models WildfireSpotter uses are competitive with even a deep neural approach. 
