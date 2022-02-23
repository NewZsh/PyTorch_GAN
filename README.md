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
    - 2. I use a linear layer for the label's one-hot encoding, then add it with noise. The linear layer can be viewed as label embedding. Now, the results are as expected.

* [Wasserstein GAN (WGAN)](https://arxiv.org/pdf/1701.07875.pdf)
* [Improved Training of Wasserstein GAN (WGAN-GP)](https://arxiv.org/pdf/1704.00028.pdf)

## Experiment Results

* DCGAN (with conditional)
| epoch 0 | epoch 10 | epoch 20 | epoch 30 | epoch 40 | 
| :---:  | :---: | :---: | :---: | :---: | 
| ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/0.png?raw=true) | ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/10.png?raw=true) | ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/20.png?raw=true) | ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/30.png?raw=true) | ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/40.png?raw=true) |
| epoch 50 | epoch 100 |  epoch 150 |  epoch 199 | - 
| ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/50.png?raw=true) | ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/100.png?raw=true) |  ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/150.png?raw=true) |  ![xxx](https://github.com/wangguanan/Pytorch-Basic-GANs/blob/master/images/cGAN/199.png?raw=true) | - |


to be finished