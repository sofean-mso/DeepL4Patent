# Deep Learning based Pipeline with Multichannel Inputs for Patent Classification

Patent document classification as groundwork has been a challenging task with no satisfactory performance for decades.  In this work, we introduce a deep learning pipeline for automatic patent classification with multichannel inputs.   A neural network model is trained with multichannel inputs namely embeddings of different segments of patent texts, and sparse linear input of different metadata.


![arch_0000](https://user-images.githubusercontent.com/52244944/60329845-742e2680-9991-11e9-8d43-65311eb837a9.png)

Currently the repository contains three examples:

1. [Multi-class Patent Classification with multichannel inputs](https://github.com/sofean-mso/DeepL4Patent/blob/master/Deep4Patent%20Pipeline%20for%20Multi-class%20Patent%20Classification.ipynb): The Main IPC code is used as a label for the patent document

2. [Multi-label Patent Classification with multichannel inputs](https://github.com/sofean-mso/DeepL4Patent/blob/master/Deep4Patent%20Pipeline%20for%20Multi-label%20Patent%20Classification.ipynb): The full IPC codes are used as a label for the patent document

3. [Multi-class Patent Classification with a single channel input](https://github.com/sofean-mso/DeepL4Patent/blob/master/single_input/Multi-classification%20with%20a%20single%20Input%20channel.ipynb)

