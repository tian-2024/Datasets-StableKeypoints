# Keypoints-Dataset

Recently, I came across an intriguing project called StableKeypoints, which was published at CVPR 2024.

I attempted to run the project using its dataset but encountered some issues with almost every dataset.

After searching for solutions on the website and experimenting with the code, I managed to resolve most of these problems.

To make it more convenient for myself and others in the future, I am compiling some useful resources here.

There are 5 datasets used in the project:
1. CelebA
2. CUB
3. DeepFashion
4. Taichi
5. Human3.6m

## CelebA

## CUB

## DeepFashion

## Taichi

Taichi is a video dataset.

Previous researchers preprocessed the dataset for keypoints learning.

The preprocessed dataset is an image dataset, containing 5000 images for training and 300 images for testing.

The images can be downloaded from the google drive:

https://drive.google.com/drive/folders/18l3W4tkYWnpPcwMMhy07Tc6R7Ky_ouoJ?usp=sharing

![image](https://github.com/user-attachments/assets/b56c8048-4319-4b84-bb91-ad5ee378a826)

And use the `eval_images.tar.gz`

After unzip, we can use the train and test data here:

![image](https://github.com/user-attachments/assets/494e889a-2aad-4057-933e-7e7270cf62a2)

The landmarks data is in this project:

https://github.com/AliaksandrSiarohin/motion-cosegmentation/tree/master/landmarks



## Human3.6m
