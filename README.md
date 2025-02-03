# LyRaCAD
Here is how to perform the inference segmentation using our proposed deep-learning model in "A robust deep-learning model across scanners and ground truth generation masks for fully automatic segmentation on whole-body [18F]FDG PET/CT lymphoma studies".

This model proved to be robust across scanners and ground truth segmentation methods for the fully automatic segmentation of lymphoma lesions in [18F]FDG PET/CT images. 

## Usage
### 1. Install the required libraries : 
You will first need and assure that the [nnU-Net required libraries](https://github.com/MIC-DKFZ/nnUNet) and configure required paths.

### 2. Download weights : 
Weights can be downloaded at the following [link](https://drive.google.com/drive/u/0/folders/1T02D1G6igx9eaFcgxzG0y0QBdp7Qg2gF).

### 3. Inference :
In the PATH_FOLDER every patients should be numbered as patientID_0000 for CT and patientID_0001 for PET in the nifti format where CT should be in hounsfield unit and PET in SUV.

Then, from the terminal type:

nnUNet_predict -i PATH_FOLDER -o ./PATH_OUTPUT -t 1

If you need help with your data preparation to perform inference using nnU-Net, please drop me a line (claudia.constantino@fundacaochampalimaud.pt).
