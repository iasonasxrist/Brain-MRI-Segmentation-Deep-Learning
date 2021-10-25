# MRI_Brain_Segmentation
 
Hierarchical MRI tumor segmentation with U-Net 3D CNN

![1_BBYuLIsXxmIF3Hafuvfa8g](https://user-images.githubusercontent.com/80000902/138735451-072b41c5-7fa0-4149-8f37-3e53e165a311.gif)

University of West Attica

Table of Contents
Introduction
Citation
Running
Model
Disclaimer and known issues
Results
Introduction
This repository contains the original models (dense24, dense48, no-dense) described in the paper "Hierarchical MRI tumor segmentation with densely connected 3D CNN" (https://arxiv.org/abs/1802.02427). This code can be applied directly in BTRAS2017.


  title     = {{MRI} tumor segmentation with densely connected 3D {CNN}},
  booktitle = {Medical Imaging 2018: Image Processing, Houston, Texas, United States,
	       10-15 February 2018},
  pages     = {105741F},
  year      = {2018},
  crossref  = {DBLP:conf/miip/2018},
  url       = {https://doi.org/10.1117/12.2293394},
  doi       = {10.1117/12.2293394},
  timestamp = {Tue, 06 Mar 2018 10:50:01 +0100},
  biburl    = {https://dblp.org/rec/bib/conf/miip/ChenWDAWX18},
  bibsource = {dblp computer science bibliography, https://dblp.org}
}

Running
Pre-installation:Tensorflow,Keras,nibabel,sklearn,numpy,pandas, PIL

Download and unzip the training data from BTRAS2017

Use N4ITK to correct the data: python n4correction.py /mnt/disk1/dat/lchen63/spie/Brats17TrainingData/HGG

Train the model: python train.py

-gpu: gpu id
-bs: batch size
-mn: model name, 'dense24' or 'dense48' or 'no-dense' or 'dense24_nocorrection'
-nc: n4ITK bias correction,True or False
-e: epoch number
-r: data path
-sp: save path/name
...
For example: python train.py -bs 2 -gpu 0 -mn dense24 -nc True -sp dense48_correction -e 5 -r /mnt/disk1/dat/lchen63/spie/Brats17TrainingData/HGG


Disclaimer and known issues
These codes are implmented in Tensorflow
In this paper, we only use the glioblastoma (HGG) dataset.
I didn't config nipype.interfaces.ants.segmentation. So if you need to use n4correction.py code, you need to copy it to the bin directory where antsRegistration etc are located. Then run python n4correction.py
If you want to train these models using this version of tensorflow without modifications, please notice that:
You need at lest 12 GB GPU memory.
There might be some other untested issues.
Results
Result visualization : visualization visualization
