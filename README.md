# Building a COVID-19 Resnet18 PyTorch Image Classifier 

## Detecting COVID-19 using images from COVID-19 Radiography Database from Kaggle

<p align="center">
<img width="1088" alt="Screen Shot 2020-09-28 at 8 59 47 PM" src="https://user-images.githubusercontent.com/53641091/94511215-908cc480-01cd-11eb-8c97-fa0ecd88d56a.png">
</p>

<p align="center">
<img width="407" alt="Screen Shot 2020-09-28 at 9 24 33 PM" src="https://user-images.githubusercontent.com/53641091/94512500-05adc900-01d1-11eb-866a-48437ffc6411.png">
</p>

The purpose of this project was to create a resnet18 convolutional neural network using PyTorch that would be capable of classifying images from the COVID-19 Radiography Database Dataset from Kaggle.com [click here](https://www.kaggle.com/tawsifurrahman/covid19-radiography-database). 

<p align="center">
<img width="620" alt="Screen Shot 2020-09-28 at 9 26 50 PM" src="https://user-images.githubusercontent.com/53641091/94512631-59201700-01d1-11eb-8509-75d380419dcb.png">
</p>

I started the project by first importing all the necessary libraries and modules. We need to make sure we are importing the most up-to-date PyTorch version available. PyTorch is an open source machine learning library based on the Torch library. It is commonly employed for computer vision and natural language processing tasks. PIL will be used to display the images from our training and test sets. We will also be utilizing torchvision to perform the image transformations and augmentations on our training set during the training phase of the project. 

<p align="center">
<img width="589" alt="Screen Shot 2020-09-28 at 9 12 39 PM" src="https://user-images.githubusercontent.com/53641091/94511852-5c1a0800-01cf-11eb-8eb6-c83296c959bb.png">
</p>

Next, came the training and test set preparation along with creating a custom dataset, if need be. It consists of cycling through the relevant folders and deriving the necessary images to create the training and test sets to be used in the project. The class is created from torch.utils.data.Dataset. Below is the framework of the class that will need to be generated. 

<p align="center">
<img width="818" alt="Screen Shot 2020-09-28 at 9 37 08 PM" src="https://user-images.githubusercontent.com/53641091/94513142-ca13fe80-01d2-11eb-8f3d-8e1df3fce0d9.png">
</p>



## Key takeways:

*1. .*

*2. .*

*3. .*
