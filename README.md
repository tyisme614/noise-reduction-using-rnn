#Info
Version : 0.0.2
Developer : Yuan
Environment: Ubuntu 18.04 x64, Tensorflow 1.14.0(with gpu), Python 3.6.8, scipy 1.3.0, numpy 1.17.0, CUDA 10.0, cudnn7.6.2.24
Remark : This project is forked from adityatb/noise-reduction-using-rnn on GitHub.com, the original author/developer is adityatb

# Noise Reduction using RNNs with Tensorflow
Implements python programs to train and test a Recurrent Neural Network with Tensorflow

## Instructions
Before running the programs, some pre-requisites are required. This code is developed for Python 2.7, with numpy, and scipy (v0.19) libraries installed. In addition, Tensorflow v1.1 is required. It is recommended to create a virtualenv with all the dependencies for smooth execution.

This project additionally relies on the MIR-1k dataset, which isn't packed into this git repo due to its large size. It can be downloaded here freely: http://mirlab.org/dataSet/public/MIR-1K_for_MIREX.rar

Once downloaded and unpacked, the '.wav' files are placed in the 'Wavs' directory within the folder containing the scripts.


The program contains 4 scripts, which are run in the following order.
1. 'sumaudio.py' - Creates a training set in the '/Training/NoiseAdded/' directory using the voice data of MIR-1k and the Noises provided in the 'Noises' directory
2. 'CreateTest.py' - Separates 1000 random files from the Training directory and moves them to the test folder for later testing.
3. 'LSTM_Train.py' - Begins to train an LSTM network with the files in the training folder, and saves the tensorflow graphs in the Testing directories.
4. 'LSTM_Testing.py' - Once testing is complete, the graph is saved as 'FINAL' in the '/TF_Checkpoints/' directory, and invoked by this script. Files in the testing directory are now fed into the graph to produce outputs.
