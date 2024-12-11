# DeepFakeDetection
With the rise in DeepFake content on the internet with the help of autoencoders, generators, transformers, etc. it proves to be a crucial task to detect such manipulations often present the content to ensure that the technology is not utilised with malicious intent.
DeepFake Detection using Residual Neural Network(ResNet) and Gated Recurrent Unit(GRU).

Dataset utilised: [DFDC dataset](https://www.kaggle.com/competitions/deepfake-detection-challenge) <br/>
A portion of the DFDC dataset was selected and utilised for the creation of a dataset that consists only of the faces extracted from the videoframes. <br/>
Processed Dataset: [Google Drive Link](https://drive.google.com/drive/folders/1gDD9b9mBlsXJjlR6PPZ_6e9po1m0P0Tp?usp=sharing) <br/>
The above dataset could be directly passed on as the input

## Model Architecture
The model comprises of 2 main aspects:
1. Residual Neural Network(ResNet)
2. Gated Recurrent Unit(GRU) <br/>

This ensures that the model captures both the spatial features, which is carried out by ResNet, while also capturing the temporal aspect, which is carried out by GRU, as it would prove to be crucial in a video-based dataset scenario as it is in this case.

## Model Summary

1. ResNet Backbone                * Output Shape: (1, 512, 7, 7) * Number of Parameters: 21284672
2. GRU Layer                      * Output Shape: (1, 7, 256)    * Number of Parameters: 3148800
3. Fully Connected Layer          * Output Shape: (1, 1)         * Number of Parameters: 769       

Total Trainable Parameters: 24434241
