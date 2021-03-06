# Deep_Learning_HPC
There is a major transformation inside the automotive industry towards Autonomous/ self-driving vehicles. This has caused a transition in the way the cars are developed. To have all the sensors for sensing the environment (Perception problem), path planning (Processing problem), actuating (Response rate problem) the movement though CAN in response with the continuously changing environment (Variability) and communicating(Network strength problem) with other vehicles and infrastructure requires a lot of computation cost at negligible amount of time.




# Tasks

# Task 1. Cluster and Setup
------------------------------------------------------
 

# Task 2. Training a Pytorch deep learning model on Palmetto cluster

GPU usage

![](Images/Image/Picture1.png) 

Plot the accuracy against the number of training Epochs on a Graph.

![](Images/Image/Picture2.png)


# Task 3. Modify the code for better performance (use two GPUs).

torch.cuda.device_count() returned number of GPU available
Output:

![](Images/Image/Picture5.png)



![](Images/Image/Picture6.png)


GPU Usage (Multiple GPU)

![](Images/Image/Picture3.png)

Plot the accuracy against the number of training Epochs on a Graph. 

![](Images/Image/Picture4.png)



Increasing Accuracy : Alexnet pretrained was used for better performance with batch size 256, SGD optimizer and 100 epochs.


![](Images/Image/Picture7.png)

![](Images/Image/Picture8.png)

Plot the accuracy against the number of training Epochs on a Graph. 

![](Images/Image/Picture9.png)

# Task 4. Model inference for a certain image.


![](Images/Image/Picture10.png)

![](Images/Image/Picture11.png)

![](Images/Image/Picture12.png)

# Results
There are 10 total classes, and the top10_inds variable gives me the indices of the 10 classes along with their values in percentage.



# First Result 

The category 5 that belongs to DOG in Cifar 10 was predicted correctly.

![](Images/Image/Picture13.png)

![](Images/Image/Picture14.png)


# Second Result 
Result The category 1 that belongs to CARS was predicted by the model with test accuracy = 90.39%.


![](Images/Image/Picture15.png)

![](Images/Image/Picture16.png)

Test Accuracy 

![](Images/Image/Picture17.png)

# Steps
1. Jupyter Notebook setup https://janakiev.com/blog/jupyter-virtual-envs/

2. Create a Conda virtual environment in the terminal using module add anaconda3/5.1.0

3. environment, once created/modified is saved and can be accessed later through the code:
    conda create -n NAME_OF_ENV python=3.5 # (Create Environment)
    source activate NAME_OF_ENV # (Activate Environment)
    source deactivate NAME_OF_ENV # (Deactivate Environment)
    
4. Install necessary packages in the terminal
    CUDA module add cuda-toolkit/10.0.130
    CuDNN module add cuDNN/10.0v7.4.2
    
 5. CUDA 10.1
conda install pytorch==1.5.1 torchvision==0.6.1 cudatoolkit=10.1 -c pytorch

6. Training deep learning model for Image Classification
   a. Load the training and test datasets from torchvision
  Training Data can be obtained from various online sources, self-procured or can even be imported from a library
  Pytorch. https://pytorch.org/docs/stable/torchvision/datasets.html
  
    b. 	Define a Convolutional Neural Network https://medium.com/@RaghavPrabhu/understanding-of-convolutional-neural-network-cnn-deep-learning-99760835f148
  
   c. Define a loss function https://algorithmia.com/blog/introduction-to-loss-functions
   d.  Train the network on the training data with different number of Epochs https://towardsdatascience.com/epoch-vs-iterations-vs-batch-size-4dfb9c7ce9c9 


7.  Monitor the usage info of GPU and GPU memory: nvidia-smi –l


# Dependencies
1. Multiple GPU
2. CUDA 11
3. Jupyter Notebook
4. Python 3.6
5. pytorch
6. Cifar https://www.cs.toronto.edu/~kriz/cifar.html



# License
Copyright (C) 2020 Shaurya Panthri.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/
