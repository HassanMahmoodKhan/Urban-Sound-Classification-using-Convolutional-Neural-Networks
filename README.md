# Urban-Sound-Classification-using-Convolutional-Neural-Networks

Convolutional neural networks are widely used in the fields of image and signal processing, audio classification, document analysis etc. 
Over the years, extensive research has been carried out in the domain of audio classification via implementation of convolutional networks. In this regard, researchers have used a variety of datasets with ESC-10, ESC-50, UrbanSound8k etc., being the prominent ones offering access to a large variety of audio samples. 

In the recent past, it has been observed that pedestrians all over the world are becoming increasingly prone to accidents due to the lack of awareness of incoming obstacles in their nearby surroundings. The project aims to curtail this threat by using sound as a tool of detecting potential hazards, making the accuracy of classification imperative. As a result, pedestrians will be made aware of the approaching threats in the environment.In this regard, the use of convolutional neural networks to effectively distinguish urban sounds from our everyday environment.

## Dataset
The model is implemented on dataset “UrbanSound8K”. The dataset encompasses urban sounds from 10 classes i.e., 8732 labeled sound excerpts (<=4s). These are:
- Air conditioner 
- Car horn 
- Children playing 
- Dog bark 
- Drilling 
- Engine idling 
- Gun shot 
- Jackhammer 
- Siren 
- Street music

## Feature Extraction
Mel-frequency cepstrum (MFC) is a depiction of the power spectrum of sound for limited intervals. It can be computed by taking linear cosine transform of a log power spectrum. The operation is performed on a nonlinear mel scale of frequency. Mel-frequency cepstral coefficients (MFCCs), represent the coefficients that constitute MFC. These are basically features used in speech recognition across a plethora of applications.
MFCCs are commonly derived as follows:
1. First, we calculate the Discrete Fourier transform (DFT) of the input signal.
2. Then magnitude of DFT is wrapped in mel frequency.
3. Take the logs for each of the mel frequencies. 
4. Take the Inverse Discrete Fourier transform (IDFT) at each frequency. 
5. The MFCCs are the amplitudes of the resulting spectrum.

## Convolutional Neural Network (CNN)
Increasingly popular in the field of deep learning as they offer the innovative ability to simultaneously learn a variety of filters pertaining to a dataset.

### Convolutional Layers
Convolutional layers are central to the working principle of CNNs. Inside a convolution layer, arrays of sound data are multiplied with a two-dimensional array of weights referred to as a filter, resulting in a scalar product. Therefore, convolution is a linear operation. CNNs traditionally have a series of convolution layers by which they can extract features from the incoming data and lay them out on a feature map.

### Pooling Layer
Pooling requires the selection of a pooling operation to be applied to feature maps, much like a filter. The size of the filter is much smaller than the size of the feature map; in particular, usually 2×2 pixels are used with a stroke of 2 pixels. One of the key characteristics of the pooling operation is that it is not learned; rather it has to be specified beforehand. Few of the functions used in this process are:
- Average Pooling: This function helps us to compute the mean values on the feature map.
- Maximum Pooling (also known as Max Pooling): This function enables us to compute the ceiling values on the feature map.

The convolutional and pooling layers are aided by the dropout layer which reduces netowork overfitting, and activation functions. Since the problem at hand is a multi-class classifif=cation problem, we employ Softmax function. It transforms a vector of K real values into a vector of K real values that adds to 1, so they can be interpreted as probabilities.

## Data Preprocessing
A  number of preprocessing steps have been employed to transform the dataset into the required format and representation:
1) Label Encoding
2) One-Hot Encoding
3) Train & Test Split

## Model Evaluation
The model has been evaluated using a several metrics: 
1) Accuracy
2) Catergorical-Cross Entropy
3) Confusion Matrix

The deep-learning model consisting of 4 convolutional layers with max-pooling and GlobalAveragePooling2D had been implemented and proven to be efficient enough for further applications with sound classification. The final accuracy achieved by our model defined is 91.57% for the test data, which is at par and better than some reported in literature.


