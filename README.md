# Handwriting Recognition Project for learning

Special thanks to Mr. Johan Dettmar. Please come and find this awesome for details, he give clear instruction about how to do it.

I am using Tensorflow.js for creating the model, after training in colab based on EMNIST dataset. Find the jupiter notebook for your details.

Let's have fun at : https://tommy-ngx.github.io/hand_words/index.html

Model is buiding in Keras using some kernels, adam for optimizers, loss based on categorical_crossentropy.
All layers are below:

[](https://raw.githubusercontent.com/Tommy-Ngx/hand_words/main/model/tommy-layers.png)
Model: "sequential"
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d (Conv2D)              (None, 28, 28, 16)        416       
_________________________________________________________________
max_pooling2d (MaxPooling2D) (None, 14, 14, 16)        0         
_________________________________________________________________
batch_normalization (BatchNo (None, 14, 14, 16)        64        
_________________________________________________________________
dropout (Dropout)            (None, 14, 14, 16)        0         
_________________________________________________________________
conv2d_1 (Conv2D)            (None, 14, 14, 32)        12832     
_________________________________________________________________
max_pooling2d_1 (MaxPooling2 (None, 7, 7, 32)          0         
_________________________________________________________________
batch_normalization_1 (Batch (None, 7, 7, 32)          128       
_________________________________________________________________
dropout_1 (Dropout)          (None, 7, 7, 32)          0         
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 7, 7, 64)          51264     
_________________________________________________________________
max_pooling2d_2 (MaxPooling2 (None, 3, 3, 64)          0         
_________________________________________________________________
batch_normalization_2 (Batch (None, 3, 3, 64)          256       
_________________________________________________________________
dropout_2 (Dropout)          (None, 3, 3, 64)          0         
_________________________________________________________________
flatten (Flatten)            (None, 576)               0         
_________________________________________________________________
dense (Dense)                (None, 256)               147712    
_________________________________________________________________
batch_normalization_3 (Batch (None, 256)               1024      
_________________________________________________________________
dropout_3 (Dropout)          (None, 256)               0         
_________________________________________________________________
dense_1 (Dense)              (None, 62)                15934     
=================================================================
Total params: 229,630
Trainable params: 228,894
Non-trainable params: 736
___________________________



Cheers,
