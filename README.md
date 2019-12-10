# ECE285_Final_Project

## Gatys Neural Style Transfer

Go to folder NeuralStyleTransfer. The provided Jupyter notebook will be almost ready to run with the given Images; however, the model must be downloaded using the following command inside the Models directory:

wget -c --no-check-certificate https://bethgelab.org/media/uploads/pytorch_models/vgg_conv.pth

We first define the VGG class with its layers and outputs and other classes necessary for training. The "optimal" image is initialized as the content image and the iterative update process is started. At the end of the specified number of iterations, the optimal image should now exhibit the style of the style image and the content of the content image.

The next sections replicate the training operation above. It is ran twice each with the content loss taken at a different convolutional layer. The first iteration calculates the convolutional loss at layer 2 while the second iteration calculates the loss at layer 4.

The final section once again runs training multiple times for different ratios of content versus style loss.

## Cycle GAN
