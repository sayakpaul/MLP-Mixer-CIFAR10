# MLP-Mixer-CIFAR10

This repository implements MLP-Mixer as proposed in [MLP-Mixer: An all-MLP Architecture for Vision](https://arxiv.org/abs/2105.01601). The paper introduces an all MLP (Multi-layer Perceptron) architecture for computer vision tasks. Yannic Kilcher walks through the architecture in [this video](https://www.youtube.com/watch?v=7K4Z8RqjWIk). 

Experiments reported in this repository are on CIFAR-10. 



## What's included?

* Distributed training with mixed-precision.
* Visualization of the token-mixing MLP weights.
* A TensorBoard callback to keep track of the learned linear projections of the image patches.

## Notebooks

* [`MLP_Mixer_Training.ipynb`](https://github.com/sayakpaul/MLP-Mixer-CIFAR10/blob/main/MLP_Mixer_Training.ipynb): MLP-Mixer utilities along with model training. 
* [`ResNet20.ipynb`](https://github.com/sayakpaul/MLP-Mixer-CIFAR10/blob/main/ResNet20.ipynb): Trains a ResNet20 for comparison purposes.
* [`Visualization.ipynb`](https://github.com/sayakpaul/MLP-Mixer-CIFAR10/blob/main/Visualization.ipynb): Visualizes the learned projections and token-mixing MLPs.

**Note**: These notebooks are runnable on Colab. If you don't have access to a tensor-core GPU, please disable the mixed-precision block while running the code. 

## Results

MLP-Mixer achieves competitive results. The figure below summarizes top-1 accuracies on CIFAR-10 test set with respect to varying MLP blocks. 

<div align="center">
	<img src="https://i.ibb.co/MSzm7mJ/image.png" width=450/>
</div><br>

The table below reports the parameter counts for the different MLP-Mixer variants:

<div align="center">
	<img src="https://i.ibb.co/GP21JtY/image.png" width=450/>
</div><br>

> ResNet20 (0.571969 Million) achieves 78.14% under the exact same training configuration. Refer to [this notebook](https://github.com/sayakpaul/MLP-Mixer-CIFAR10/blob/main/ResNet20.ipynb) for more details. 

## Models

You can reproduce the results reported above. The model files are available [here](https://github.com/sayakpaul/MLP-Mixer-CIFAR10/releases/download/Models/models.zip). 