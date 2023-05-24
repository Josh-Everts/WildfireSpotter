# WildfireSpotter
## Overview
WildfireSpotter is a lightweight wildfire detection model employing image masking to extract salient features and classify an image as having a wildfire inside it, or not. The model is trained on data from the FLAME dataset, created by Shamsoshoara et al. Their paper which outlines their data creation and modeling approach can be found [here](https://arxiv.org/pdf/2012.14036v1.pdf). 

## Approach
Many others have attempted wildifire detection using deep-learning approaches, but as of yet few lightweight (feature-based) approaches have been tried. In my script I outline different salient features. I find that the averaged masked image redness, and percentage of total pixels masked as red work best. Redness is normalized on a pixel-wise basis: $ Red_Normed = Red/(Blue+Green)$. I then employ simple classifiers (KNN and a logistic model) to perform a binary classification between fire images and non-fire images.

## Results
### Test Accuracy
As outlined in the notebook script, my approach results in a 75.7% accuracy on the included test data, which closely matches the 76% achieved using a CNN (Shamsoshoara et al.). This means that the lightweight features and models WildfireSpotter uses are competitive with even a deep neural approach. 
### True-out-of-sample Accuracy
To further validate my results I also used wildfire data from a Kaggle competition [here](https://www.kaggle.com/datasets/brsdincer/wildfire-detection-image-data). On this true-out-of-sample data, which is visually distinct from the training and validation data WildfireSpotter achieves an 86% accuracy. This indicates the simple features which the model looks at generalize well to a completely different wildfire dataset. Overall, this indicates that the WildfireSpotter could be a good baseline for a lightweight approach to fire detection when hardware resources are limited. 
