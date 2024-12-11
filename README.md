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

1. **ResNet Backbone**
   * _Output Shape:_ (1, 512, 7, 7)
   * _Number of Parameters:_ 21284672
2. **GRU Layer**
   * _Output Shape:_ (1, 7, 256)
   * _Number of Parameters:_ 3148800
3. __Fully Connected Layer__
   * _Output Shape:_ (1, 1)
   * _Number of Parameters:_ 769       

**_Total Trainable Parameters:_** 24434241

## Evaluation

On the test dataset, the following was achieved by the model described:
* Accuracy: 0.75
* Precision: 0.73
* Recall: 0.79
* F1 Score: 0.76

It can described as a good and moderately effective model and further improvements could be made by focusing on boosting the precision by reducing false positive scenarios and recall by ensuring fewer deepfakes being missed by the model.
