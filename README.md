## GANs
Pytorch implementations of most used Generative Adversarial Network (GAN) varieties. (Support both GPU and CPU.)

## Dependencies
* [PyTorch 1.8.1](http://pytorch.org/)

## Table of Contents
* [Vanilla GAN (GAN)](https://arxiv.org/pdf/1406.2661.pdf)
* [Conditonal GAN (cGAN)](https://arxiv.org/pdf/1411.1784.pdf)
* [Deep Convolutional GAN (DCGAN)](https://arxiv.org/pdf/1511.06434.pdf)
    Original DCGAN does not use label as conditions of generator. This leaves a question how to combine label information in deconvolutional layer? I have tried two methods:

    - 1. Firstly, like what cGAN does, concat the label's one-hot encoding and input noise. Then, do the same things with original DCGAN. However, the generated images are nothing to do with labels.
    - 2. I use a linear layer for the label's one-hot encoding, then add it with noise. The linear layer can be viewed as label embedding. Now, the results are as expected (despite of the disorder).

* [Wasserstein GAN (WGAN)](https://arxiv.org/pdf/1701.07875.pdf)
* [Improved Training of Wasserstein GAN (WGAN-GP)](https://arxiv.org/pdf/1704.00028.pdf)

## Experiment Results

* DCGAN (with conditional)

| epoch 10 | epoch 50 | epoch 100 | epoch 200 | 
| :---:  | :---: | :---: | :---: | 
| ![image](https://github.com/NewZsh/PyTorch_GAN/blob/main/images/DCGAN_10.png) | ![image](https://github.com/NewZsh/PyTorch_GAN/blob/main/images/DCGAN_50.png) | ![image](https://github.com/NewZsh/PyTorch_GAN/blob/main/images/DCGAN_100.png) | ![image](https://github.com/NewZsh/PyTorch_GAN/blob/main/images/DCGAN_200.png) |

to be finished