# Functional outcome prediction for ischemic stroke patients

This repository contains some example code on predicting functional outcome 
for ischemic stroke patients based on clinical variables, diffusion weighted 
imaging (DWI) and a combination of both.

**k_ontram_functions**: We consider ordinal neural network transformation models (ONTRAMs) 
to predict functional outcome in terms of modified Rankin Scale (mRS) three months 
after stroke symptom onset. The functions to define and train the ONTRAMs are 
contained in the folder *k_ontram_functions*.

**callbacks**: We consider three ONTRAMs based on clinical variables (SI-LS<sub>x</sub>), 
DWI (SI-CS<sub>B</sub>) and a combination of both (SI-LS<sub>x</sub>-CS<sub>B</sub>
). Baseline clinical variables and imaging data can not be made available due to 
privacy concerns. However, intermediate results in terms of 
predictions are available in the folder *callbacks*.

**classification_models_3D_master**: The images in the ONTRAMs are modelled with 
3D ResNets that are initialized with pre-trained, transformed 2D weights from ImageNet. 
The code for the models is contained in the folder *classification_models_3D_master* which 
is copied and slightly adapted from the github repository ZFTurbo/classification_models_3D.

**notebooks**: All information on how to define, train and evaluate the ONTRAMs is contained 
in the iPython Notebook *3D_CNN_ONTRAM_Zurich_DWI_mrs_preprocessed_ENSEMBLE_CV_ORDINAL_Resnet.ipynb*.
