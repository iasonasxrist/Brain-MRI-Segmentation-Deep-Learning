# Segmentation of brain tumours using MR images based on deep learning
<a href="https://opensource.org/licenses/MIT">
 <img src="https://img.shields.io/badge/License-MIT-yellow.svg"></a>  
 
 
Inference Notebook: <a https://www.kaggle.com/code/iasonasxrist/mri-brain-tumour-segmentation-with-unet-cnn > </a>  


Quantitative analysis of brain MRI is routine for many neurological diseases and conditions and relies on accurate segmentation of structures of interest. Deep learning-based segmentation approaches for brain MRI are gaining interest due to their self-learning and generalization ability over large amounts of data.

Here, 2 pre-trained model architectures: UNet and Unet with ResNext backbone were trained and evaluated for Dice scores on Brain MRI dataset obtained from The Cancer Imaging Archive (TCIA).


Dataset:
Number/Size of Images   : Total      : 3929
                          Training set   : 2947 
                          Validation set : 393 
                          Test set       : 797(approx)
                          
                          
![1_BBYuLIsXxmIF3Hafuvfa8g](https://user-images.githubusercontent.com/80000902/138735451-072b41c5-7fa0-4149-8f37-3e53e165a311.gif)

University of West Attica




Running
Pre-installation:Tensorflow,Keras,nibabel,sklearn,numpy,pandas, PIL

Download and unzip the dataset from [Kaggle](https://www.kaggle.com/mateuszbuda/lgg-mri-segmentation) 

Use N4ITK to correct the data: python n4correction.py /mnt/disk1/dat/lchen63/spie/Brats17TrainingData/HGG

Train the model: python train.py




Results
Result visualization : visualization visualization

![image](https://user-images.githubusercontent.com/80000902/194289022-9bdf1591-1a3a-4741-89fe-d175424e3ecd.png)
![image](https://user-images.githubusercontent.com/80000902/194289026-afc0a18f-1bfb-4c5f-ba33-df61bdb1d93c.png)



Disclaimer and known issues
These codes are implemented in Tensorflow, Pytorch
All trainings have been executed into kaggle enviroment due to GPU availability.
You can find and fork all my implementation into [my kaggle](https://www.kaggle.com/iasonasxrist).


## COCO Examples

<table>
  <tr>
    <td><img src="Images/COCO_val2014_000000562207.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000165547.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000579664.jpg" ></td>
