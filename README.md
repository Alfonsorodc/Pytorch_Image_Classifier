# Pytorch_Image_Classifier
Image Classifier with PyTorch (Python)

This is the code (image classifier_final.ipynb) to classify flower images between 102 classes (you can download de dataset from http://www.robots.ox.ac.uk/~vgg/data/flowers/102/index.html). The code is structured like follow:

Install Pytorch (is necessary install every time with you start your code)
Import necessaries libreries
Mount our Drive unity (is necessary upload our image folders like validation, test or train folders at google drive) Google Colab works over Google Drive
Load and Transform the data (images), to train, validate and pass the images through our Neural Network or Model you must transform before the images.
Load in a mapping from category label to category name. With cat_to_name.json
Load a pre-trained network from ImageNet framework, in my case I used "Adam"
Define a untrained feed-forward network as a classifier, using ReLU activations and dropout, the we need specify the Loss and the Optimizer
Attach the untrained FF network to Adam = Model
Train, validate and Test our model (only the part untrained (FF)). I only calculate the accuracy over the validation.
Save our model totally trained (checkpoint.pth) Is over 25 Mb isn't uploaded in this repository
Load the model trained Now you'll write a function to use a trained network for inference. That is, you'll pass an image into the network and predict the class of the flower in the image. Write a function called predict that takes an image and a model, then returns the top K most likely classes along with the probabilities 12)Take an image of the test or validation folder
Process and show the image processed
Search the TopK most probable classes
Plot the most probable class
