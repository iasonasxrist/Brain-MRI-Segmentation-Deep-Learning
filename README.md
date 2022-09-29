# Segmentation of brain tumours using MR images based on deep learning
 
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


Disclaimer and known issues
These codes are implemented in Tensorflow, Pytorch
All trainings have been executed into kaggle enviroment due to GPU availability.
You can find and fork all my implementation into [my kaggle](https://www.kaggle.com/iasonasxrist).



# CLIP prefix captioning.

<a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg"></a>  
Inference Notebook: <a href="https://colab.research.google.com/drive/1tuoAC5F4sC7qid56Z0ap-stR3rwdk0ZV?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" height=20></a>  





## Official implementation for the paper ["ClipCap: CLIP Prefix for Image Captioning"](https://arxiv.org/abs/2111.09734)




## Description  
Image captioning is a complicated task, where usually a pretrained detection network is used, requires additional supervision in the form of object annotation. We present a new approach that does not requires additional information (i.e. requires only images and captions), thus can be applied to any data. In addition, our model's training time is much faster than similar methods while achieving comparable to state-of-the-art results, even for the Conceptual Captions dataset contains over 3M images. 

In our work, we use the [CLIP](https://github.com/openai/CLIP) model, which was already trained over an extremely large number of images, thus is capable of generating semantic encodings for arbitrary images without additional supervision. To produce meaningful sentences we fine-tune a pretrained language model, which has been proven to be successful for other natural language tasks. The key idea is to use the CLIP encoding as a prefix to the textual captions by employing a simple mapping network over the raw encoding, and then fine-tune our language model to generate a valid caption. In addition, we present another variant, where we utilize a transformer architecture for the mapping network and avoid the fine-tuning of GPT-2. Still, our light model achieve comaparable to state-of-the-art over nocaps dataset.

## COCO Examples

<table>
  <tr>
    <td><img src="Images/COCO_val2014_000000562207.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000165547.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000579664.jpg" ></td>
