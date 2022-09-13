# Segmentation of brain tumours using MR images based on deep learning
 
Quantitative analysis of brain MRI is routine for many neurological diseases and conditions and relies on accurate segmentation of structures of interest. Deep learning-based segmentation approaches for brain MRI are gaining interest due to their self-learning and generalization ability over large amounts of data.

Here, 2 pre-trained model architectures: UNet and Unet with ResNext backbone were trained and evaluated for Dice scores on Brain MRI dataset obtained from The Cancer Imaging Archive (TCIA).

![1_BBYuLIsXxmIF3Hafuvfa8g](https://user-images.githubusercontent.com/80000902/138735451-072b41c5-7fa0-4149-8f37-3e53e165a311.gif)

University of West Attica



Running
Pre-installation:Tensorflow,Keras,nibabel,sklearn,numpy,pandas, PIL

Download and unzip the dataset from Kaggle 

Use N4ITK to correct the data: python n4correction.py /mnt/disk1/dat/lchen63/spie/Brats17TrainingData/HGG

Train the model: python train.py




Results
Result visualization : visualization visualization


Disclaimer and known issues
These codes are implemented in Tensorflow, Pytorch
All trainings have been executed into kaggle enviroment due to GPU availability.
You can find and fork all my implementation into my kaggle. (link)
