# Deep_Learning_HPC

# TASK

1. Palmetto Cluster and Setup
2. Training a Pytorch deep learning model on Palmetto cluster .
3. Modify the code for better performance (use two GPUs).
4. model inference for a certain image.

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
   a. Load the training and test datasets from torchvision (reference)
  Training Data can be obtained from various online sources, self-procured or can even be imported from a library like      Pytorch. https://pytorch.org/docs/stable/torchvision/datasets.html
  
    b. 	Define a Convolutional Neural Network https://medium.com/@RaghavPrabhu/understanding-of-convolutional-neural-network-cnn-deep-learning-99760835f148
  
   c. Define a loss function https://algorithmia.com/blog/introduction-to-loss-functions
   d.  Train the network on the training data with different number of Epochs https://towardsdatascience.com/epoch-vs-iterations-vs-batch-size-4dfb9c7ce9c9 


7.  Monitor the usage info of GPU and GPU memory: nvidia-smi –l






# License
Copyright (C) 2020 Shaurya Panthri.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/
