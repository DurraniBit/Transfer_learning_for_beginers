

Transfer Learning Tutorial
==========================

## Overview

In this tutorial, you will learn how to train your network using
transfer learning. 

These two major transfer learning scenarios look as follows:

-  **Finetuning the convnet**: Instead of random initialization, we initialize the network with a pretrained network, like the one that is trained on ImageNet 1000 dataset. Rest of the training looks as usual.
-  **ConvNet as fixed feature extractor**: Here, we will freeze the weights for all of the network except that of the final fully connected layer. This last fully connected layer is replaced with a new one with random weights and only this layer is trained.



Load Data
---------

The problem we're going to solve today is to train a model to classify **ants** and **bees**. We have about 120 training images each for ants and bees. There are 75 validation images for each class. Usually, this is a very
small dataset to generalize upon, if trained from scratch. Since we are using **transfer learning**, we should be able to generalize reasonably well.

This dataset is a very small subset of imagenet.

.. Note ::
   Download the data from  [here](https://download.pytorch.org/tutorial/hymenoptera_data.zip )
 and extract it to the current directory.

And open the notebook by typing in `jupyter notebook` in the root directory. Install it [here](http://jupyter.readthedocs.io/en/latest/install.html) if you haven't  . 

## Credits

The credits for this code go to [Sasank Chilamkurthy](https://pytorch.org/tutorials/beginner/transfer_learning_tutorial.html).