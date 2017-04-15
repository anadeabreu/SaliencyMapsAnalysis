# SaliencyMapsAnalysis
Data post-processing for "Look Around You: Saliency Maps for Omnidirectional Images in VR Applications" QoMex 2017.
Ana De Abreu, Cagri Ozcinar, Aljosa Smolic


## General description

Python 2.7 code (Jupyter notebook) to process the collected points saved in the CSV file, representing the location (stored UV coordinates) and duration (stored time stamp) of the participants FOVs centers. We Use a threshold to cluster the collected center points. Each cluster is assumed to be a fixation point if it has a number of points equivalent to at least 150ms, a commonly used lower threshold.  In addition, to account for the gradually decreasing accuracy from the center point of focus, the fixations are further filtered using a Gaussian kernel resulting in the final saliency map.

## Content

This folder contains the following jupyter notebook files:

(1) ParsingStats_DBSCAN.ipynb -- Process the csv file into saliency maps. In addition, data is studied through visualizations.  
(2) ScanPaths.ipynb -- Data visualization: Plots user scan path on top of the studied image.  
(3) ContourPlot.ipynb -- Data visualization: Plots a contour graph of the fixations distribution.  
(4) StandardDeviationModel.ipynb -- Distortion due to spherical to planar projection (Proof-of-concept).  
(5) ComparingSaliencyMaps.ipynb -- Evaluates the performance of a modeled saliency map, using ROC, NSS and correlation.  

## Getting started

Each file is an independent code. Note that the different paths need to be modified. Jupyter notebook need to be installed 
