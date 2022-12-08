# Making-Signals-Naturally-Difficult-to-Classify-with-Supervised-Learning-Algorithms
# Contributors
Raviteja Avuthu
Raghuveer Pachipulusu
Vijay Srinivas Panchangam
Saipriya Nimmagadda
Varun Potluri
# Abstract

# Goals
1. Classify 24 kinds of signal and get higher accuracy in lower SNR value.
2. Create a substitute model and tarin the model.
3. Identify the most powerful attack that can use (most incorrect classifications for a given power constraint) to attack an unknown, un-queryable classifier.
4. Validate our attack on RML 2018 dataset  forcing it to misclassify. 

## 24 Kinds of signals
'32PSK', '16APSK', '32QAM', 'FM', 'GMSK', '32APSK', 'OQPSK', '8ASK', 'BPSK', '8PSK', 'AM-SSB-SC', '4ASK', '16PSK', '64APSK', '128QAM', '128APSK','AM-DSB-SC', 'AM-SSB-WC', '64QAM', 'QPSK', '256QAM', 'AM-DSB-WC', 'OOK', '16QAM'

# Challenges
1. We should be able to classify signals both in low SNR and high SNR.
2. We use the DeepSig Radio Signal Dataset, this dataset is pretty large (19GB). We will use 1.5 Million variation of signal modulation with respect to the SNR value.
3. Creating and training the model. As the dataset is huge, running in on our system with limited resouce took almost 4hrs for each Epoch. There were 5 Epoch. We face dificulty here as the system would crash in between.
4. Running the attack on 20GB data. As the data is huge, we were not able to perform and test the attack on the given data set since our systesm would allow Tensorflow to use system GPU resources 

# How to Run
1. Download the  RADIOML 2018.01A dataset from DEEPSIG official [website](https://www.deepsig.ai/datasets).If you want to know more, you can click [here](https://www.deepsig.ai/datasets).
2. Create new folder and name it "ExtractDataset", extract all the dataset and put on that folder using the code available named "Extract Dataset.ipynb", the folder structure will be like below:

Making-Signals-Naturally-Difficult-to-Classify-with-Supervised-Learning-Algorithms

    ├── Code
    │   ├── Ectract Dataset.ipynb
    │   ├── Classification-proposed-model-resnet-modified-highest.ipynb
    │   ├──  
    │   ├── ...
    ├── ExtractDataset
    │   ├── part0.h5
    │   ├── part1.h5
    │   ├── part2.h5
    │   ├── ....
