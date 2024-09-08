# DeepFake Detector using Convolutional Neural Networks. 
## Dataset 

https://www.kaggle.com/robikscube/kaggle-deepfake-detection-introduction

## Model

###  Feature Selection
In the convolutional neural network, there were 2 variables that had to be selected and varied in
an attempt to optimize the results: image size and epochs/iterations. The images loaded in the
model were square in shape, and 4 different sizes for the length of the square were chosen: 32,
64, 128, and 256 pixels.

Layer Number | Layer
--- | ---
1 | Input Layer
2 | Conv2D. layer, kernel = 55, stride = 2, #filters=32
3 | MaxPool2D, pool size = 22
4 | Conv2D. layer, kernel = 3, stride = 2, #filters=64
5 | Flatten Layer
6 | Sigmoid Layer

* Optimizer: Adam
* Loss Function: Binary Crossentropy
* Metrics: Accuracy, Precision and Recall

##  Evaluation Across Image Sizes

Image Size of Detector (px) | Accuracy | Precision | Recall
--- | --- | --- | ---
32 | 0.655 | 0.631 | 0.641
64 | 0.655 | 0.632 | 0.635
128 | 0.682 | 0.648 | 0.708
256 | 0.597 | 0.552 | 0.745
