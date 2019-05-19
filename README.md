# DD2424-Semantic-Segmentation-For-XRay-Images

Keras implementation of InvertedNet on chest X-ray images for semantic segmentation

This project was developed on the scope of the KTH course DD2424 Deep Learning in Data Science. The authors are Mathilde Aubret, Osheen Sharma and Blanca Cabrera.

## Abstract:

In the past few years, Deep Learning has contributed in the clinical applications making it easier for early diagnosis and treatment of the diseases. The success of deep convolutional neural network relies on big data and large sets of training examples. This project focuses on the semantic segmentation of chest X-ray images using InvertedNet architecture which relies on the use of data augmentation technique [1]. The dataset used for the project comprises of 246 chest X-ray images acquired from JSRT along with ground truth segmentation masks available on SCR. The network is trained with AdaDelta optimizer, and the loss is computed as the sum of the categorical cross entropy and the Dice coefficient. The network acquired an accuracy of 96% on training set,  93% on validation set and  95% on testing set.
Keyworkds: diagnosis, segmentation, InvertedNet, data augmentation, accuracy. 
  
## Dataset
The dataset used in the project comprises of 246 chest X-ray images and their corresponding masks taken from SCR Database (https://www.isi.uu.nl/Research/Databases/SCR/) and JSRT database (https://www.jsrt.or.jp/data/english/) respectively.  For each chest radiography images, a total 5 masks are available: 2 for lungs, 2 for clavicle and 1 for heart.

## Results
The network is trained for 1000 epoch, but the training stops after 491 epoch due to early stopping with a patience of 100 epoch. The model achieves a test accuracy of 95% and loss of 0.25.

## Repository
The repository contains the original images from the JSRT database in All247images folder and the masks from SCR database in Masks_gif folder. The converted images from IMG to PNG format are stored in Converted_Images_PNG. The converted masks from GIF to PNG format are stored in Converted_Masks_PNG. Finally the the merged and labelled masks are located in Merged_Masks_PNG. 
The file called Data_Pre-processing.ipynb corresponds to the data pre-processing of the images and masks. The main code consisting on the building, training and testing of the model can be found in Main_Code.ipynb.

## References
[1] David Major Jirı Hladuvka Maria Wimmer Alexey A. Novikov, Dimitrios Lenis and Katja Buhler. Fully convolutional architectures for multi-class segmentation in chest radiographs. 2018.