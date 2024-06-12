This repository contains data and code to reproduce model evaluation statistics and figures in the paper.


## Stored data:

1. training_preds_gts.pickle <br>
Contains:
a) Ground truth-labeled body part coordinates for the *training* dataset
b) Trained model predictions for the same body part coordinates 
c) Reference threshold distances (average length of half the head, scaled based on image resolution)<br>

2. frames_preds_gts.pickle <br>
Contains:
a) Ground truth-labeled body part coordinates for the *held-out frames* dataset
b) Trained model predictions for the same body part coordinates
c) Reference threshold distances (average length of half the head, scaled based on image resolution)

3. babies_preds_gts.pickle <br>
Contains: 
a) Ground truth-labeled body part coordinates for the *held-out babies* dataset 
b) Trained model predictions for the same body part coordinates 
c) Reference threshold distances (average length of half the head, scaled based on image resolution)

4. training_occlusion.pickle<br>
Contains: 
a) Ground truth status of whether a body part was visible (1 = visible, 0 = occluded) in the *training* dataset 
b) Model predicted confidence that body part was visible for the same body parts<br>

5. frames_occlusion.pickle<br>
Contains:
a) Ground truth status of whether a body part was visible (1 = visible, 0 = occluded) in the *held-out frames* dataset 
b) Model predicted confidence that body part was visible for the same body parts 

6. babies_occlusion.pickle<br>
Contains: 
a) Ground truth status of whether a body part was visible (1 = visible, 0 = occluded) in the *held-out babies* dataset 
b) Model predicted confidence that body part was visible for the same body parts 

7. sedation_model_results.pickle <br>
Contains:
TPR and FPR values for the sedation classifier on held-out frames and babies datasets 

8. cerebral_model_results.pickle <br>
Contains:
TPR and FPR values for the cerebral dysfunction classifier on held-out frames and babies datasets 
9. cross_validation_values_sedation.pickle <br>
Contains:
TPR and FPR values for cross-validation of the sedation classifier model on the training dataset <br>

10. cross_validation_values_cerebral.pickle <br>
Contains: 
TPR and FPR values for cross-validation of the cerebral dysfunction classifier model on the training dataset

11. sedation_features_data_model_results.pickle <br>
Contains:
Sedation classifier feature importance values from 500 iterations of XGBoost cross-validation, computed from built-in gain function <br>

12. cerebral_features_data_model_results.pickle <br>
Contains: 
Cerebral dysfunction classifier feature importance values from 500 iterations of XGBoost cross-validation, computed from built-in gain function <br>

## Dependencies:
Runs with: <br>
Python version 3.11.5<br>

Python Packages:<br>
pandas v2.0.3 <br>
numpy v1.24.3 <br>
seaborn v0.13.2 <br>
matplotlib v3.9.0 <br>
scipy v1.11.1 <br>
scikit-learn v1.3.0 <br>
xgboost v2.0.3


## Instructions for use:
This repository should be cloned to a local location. From there, 'Model Evaluations.ipynb' can be run to generate model evaluation statistics and figures displayed in the paper.
