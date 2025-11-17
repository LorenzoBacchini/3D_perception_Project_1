# Introduction
This repo contains the code developed for the first project of my 3D perception university course

# Content
In the notebook "U-Net" you can find the implementation of a U-Net to perform semantic segmentation on the famous Cityscape dataset
> [!IMPORTANT]
> The notebook was developed on Kaggle environment so all the folder path refers to the Cityscapes dataset that you can simply upload on Kaggle, link to the used dataset: https://www.kaggle.com/datasets/electraawais/cityscape-dataset

At the end of the notebook you can find some test (IoU and visual tests) to assess the network performances

# Weights
If you want to start with a pretrained network you can load the weight I uploaded in the 'trained weight' folder
1. U-Net-Cityscapes_1 = first version of the net, the first convolutional layer apply only 32 filter and not 64 as the original proposed U-Net, and the network was trained for 20 epoch with batch_size=64
2. U-Net-Cityscapes_2 = second version of the net, the number of filters applied by the first convolutional layer were increased to 64 and the network was trained for 5 epoch with batch_size=64
3. U-Net-Cityscapes_3 = third version of the net, the images and the masks passed to the net was resized to 128x256 in order to maintain the original aspect ratio, the network was trained for 20 epoch with batch_size=64
4. U-Net-Cityscapes_4 = fourth version of the net, geometric augmentation were added to both the images and the masks simultaneously, the network was trained for 20 epoch with batch_size=64
5. U-Net-Cityscapes_5 = fifth version of the net, photometric augmentation were added to the images, the network was trained for 20 epoch with batch_size=64

> [!NOTE]
> The best result was obtained with the third version of the net
