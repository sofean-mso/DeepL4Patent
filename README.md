# Deep Learning based Pipeline with Multichannel Inputs for Patent Classification

In this work, we introduce a deep learning pipeline called DeepL4Patent for automatic patent classification with multichannel inputs.   A neural network model is trained with multichannel inputs namely embeddings of different segments of patent texts, and sparse linear input of different metadata. 


![archi](https://github.com/sofean-mso/DeepL4Patent/blob/master/archi.png)


The deep learning architecture has two components: deep, and wide. It feed-forward neural networks with embedding of each segment, and uses them as deep layers for deep neural network model, and the patent metadata on the other hand is used as a wide part for the model. Specifically, the architecture is described as follows: for the wide components of the model, we used one-hot representation for patent metadata features (such as inventors, citations, and assignees), these one-hot vectors are fed into separate sub-networks, and at the end they are represented as deep networks. The right side of Figure above shows the architecture of wide layers since the multi-sparse inputs of patent metadata are feed into separate subnetworks. For the deep components of the model, we create deep layers for the most important patent text segments. These are sequential input to a Long Short-Term Memory (LSTM) network that takes the embedding as inputs. The left side of the Figure shows the architecture of deep layers since we used a pre-trained word embedding model (section IV) to encode each segment texts into vectors, and then we feed them into LSTM layers. To avoid network overfitting and help network stability, we added additional layers for each input channel, dropout layer is used to drop some inputs in order to prevent neural networks from overfitting, and Batch normalization layer is used to normalize the input layer by adjusting and scaling the activations. The exponential linear unit (ELU) is used as activation function. Finally, we concatenated nine components into a fully connected layer with dropout, batch normalization, and activation function.  
Currently the repository contains three examples:

1. [Multi-class Patent Classification with multichannel inputs](https://github.com/sofean-mso/DeepL4Patent/blob/master/DeepL4Patent%20Pipeline%20for%20Multi-class%20Patent%20Classification.ipynb): The Main IPC code is used as a label for the patent document

2. [Multi-label Patent Classification with multichannel inputs](https://github.com/sofean-mso/DeepL4Patent/blob/master/DeepL4Patent%20Pipeline%20for%20Multi-label%20Patent%20Classification.ipynb): The full IPC codes are used as a label for the patent document

3. [Multi-class Patent Classification with a single channel input](https://github.com/sofean-mso/DeepL4Patent/blob/master/single_input/Multi-classification%20with%20a%20single%20Input%20channel.ipynb)



**References**
*Mustafa Sofean. Deep Learning based Pipeline with Multichannel Inputs for Patent Classification. 1st Workshop on Patent Text Mining and Semantic Technologies. PatentSemTech 2019*

