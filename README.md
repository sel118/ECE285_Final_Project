# ECE285_Final_Project

## Gatys Neural Style Transfer

Go to folder NeuralStyleTransfer. The provided Jupyter notebook will be almost ready to run with the given Images; however, the model must be downloaded using the following command inside the Models directory:

wget -c --no-check-certificate https://bethgelab.org/media/uploads/pytorch_models/vgg_conv.pth

We first define the VGG class with its layers and outputs and other classes necessary for training. The "optimal" image is initialized as the content image and the iterative update process is started. At the end of the specified number of iterations, the optimal image should now exhibit the style of the style image and the content of the content image.

The next sections replicate the training operation above. It is ran twice each with the content loss taken at a different convolutional layer. The first iteration calculates the convolutional loss at layer 2 while the second iteration calculates the loss at layer 4.

The final section once again runs training multiple times for different ratios of content versus style loss.

## Cycle GAN

Go to folder CycleGAN. The dataset required to run the provided notebook file is extremely large so we have attached a Google Drive link to retrieve it. The zip files should be unpacked in the datasets directory. Once that has been completed, the notebook is ready to run. 

https://drive.google.com/open?id=18Rluyjy5to81Paz7O90NcvBha79nD0nk

There are some requirements to be installed, for which we have included a simple line to download the necessary software. The training script will train the forward and inverse mapping functions. Use the example line given to train the necessary model for the artists monet, vangogh, cezanne, and ukiyoe. Adjust the name and dataset as necessary. This will take an extremely long time to run so we have provided pretrained models for testing purposes.

The testing script will run the entire test set through the network to map photographs to the painting domain. However, the first test line will also implement the inverse transform to return a transformed image to the photograph domain. The output images are stored in the results directory. The suffix _fake denotes forward passed images, the suffix _real denotes its respective test image, and the suffix _rec denotes an image recovered from the transformed domain.

A few images are displayed to compare the results of translating the style of the four artists.
