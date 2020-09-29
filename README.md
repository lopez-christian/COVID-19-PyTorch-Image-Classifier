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

Next, came the training and test set preparation along with creating a custom dataset, if need be. It consists of cycling through the relevant folders and deriving the necessary images to create the training and test sets to be used in the project. The class is created from torch.utils.data.Dataset. Below is the framework of the class that will need to be generated: 

<p align="center">
<img width="818" alt="Screen Shot 2020-09-28 at 9 37 08 PM" src="https://user-images.githubusercontent.com/53641091/94513142-ca13fe80-01d2-11eb-8f3d-8e1df3fce0d9.png">
</p>

DataLoaders need to be created that will aid in populating the sets from the images in each of the folders. These essentially fetch examples to feed the model during the training process. The DataLoaders iterate over the folders containing the images and tell us how many images are in each. Allowing us to correctly segmentate the relevant images into their respective categories.  

### <ins> This is for training: </ins>

<p align='center'>
<img width="974" alt="Screen Shot 2020-09-28 at 9 42 21 PM" src="https://user-images.githubusercontent.com/53641091/94513441-8a99e200-01d3-11eb-9fb5-75607b24d408.png">
</p>

### <ins> This is for testing: </ins>
<p align='center'>
<img width="974" alt="Screen Shot 2020-09-28 at 9 42 31 PM" src="https://user-images.githubusercontent.com/53641091/94513714-4c50f280-01d4-11eb-8287-9f5f8a575fdc.png">
</p>

For reference, this is a visual representation of the training and test batch sizes we will be utilizing:

<p align='center'>
<img width="873" alt="Screen Shot 2020-09-28 at 9 58 19 PM" src="https://user-images.githubusercontent.com/53641091/94514320-bddd7080-01d5-11eb-9845-f9b4da940cb0.png">
</p>

We then proceed to the visualization phase of the project where we create a helper function that forms part of the training loop. This function converts the tensorflow images back to numpy arrays. It also undoes the normalization performed in the previous step using mean and standard deviation (std). The image pixel values are converted back to their orginal values and displayed using subplot. 

<p align='center'>
<img width="576" alt="Screen Shot 2020-09-28 at 10 05 30 PM" src="https://user-images.githubusercontent.com/53641091/94514734-d00bde80-01d6-11eb-8c27-f15cef22a7ec.png">
</p>

<p align='center'>
<img width="576" alt="Screen Shot 2020-09-28 at 10 05 52 PM" src="https://user-images.githubusercontent.com/53641091/94514740-d306cf00-01d6-11eb-8f35-24f4315bfd22.png">
</p>

Then comes the model creation juncture of the project. We use the resnet18 model imported from torchvision.models. It comes ready with pre-trained weights, having been trained on the ImageNet Dataset. This image database is comprised of hundreds and thousands of images. This makes it quite a robust model to play with and serves our purpose perfectly. Not without first adjusting one of the parameters found in the fully-connected layer of the resnet18 model architecture. The resnet18 model comes with a pre-defined out_features parameter of 1000 and we only need 3 (normal, viral, covid). We also set the desired optimization and learning rate.

<p align='center'>
<img width="576" alt="Screen Shot 2020-09-28 at 10 17 53 PM" src="https://user-images.githubusercontent.com/53641091/94515485-7d332680-01d8-11eb-9556-36be2c392982.png">
</p>

The most interesting and fun part is the training phase of the project. Wherein, we witness the runnning of our epochs and the training of our model. We see validation loss and accuracy scores for every 20 steps ran. 

<p align='center'>
<img width="576" alt="Screen Shot 2020-09-28 at 10 21 22 PM" src="https://user-images.githubusercontent.com/53641091/94515717-0f3b2f00-01d9-11eb-844a-9bfa8054037d.png">
</p>

<p align='center'>
<img width="573" alt="Screen Shot 2020-09-28 at 10 21 48 PM" src="https://user-images.githubusercontent.com/53641091/94515733-195d2d80-01d9-11eb-89f9-c6df9ef22898.png">
</p>

## Key takeways:

*1. .*

*2. .*

*3. .*
