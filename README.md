# ERA-S6-Assignment-Solution

### Model Summary
```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1            [-1, 8, 28, 28]              72
       BatchNorm2d-2            [-1, 8, 28, 28]              16
           Dropout-3            [-1, 8, 28, 28]               0
         MaxPool2d-4            [-1, 8, 14, 14]               0
            Conv2d-5           [-1, 16, 14, 14]           1,152
       BatchNorm2d-6           [-1, 16, 14, 14]              32
           Dropout-7           [-1, 16, 14, 14]               0
         MaxPool2d-8             [-1, 16, 7, 7]               0
            Conv2d-9             [-1, 16, 7, 7]           2,304
      BatchNorm2d-10             [-1, 16, 7, 7]              32
          Dropout-11             [-1, 16, 7, 7]               0
           Conv2d-12             [-1, 32, 7, 7]           4,608
      BatchNorm2d-13             [-1, 32, 7, 7]              64
          Dropout-14             [-1, 32, 7, 7]               0
           Conv2d-15             [-1, 16, 7, 7]           4,608
      BatchNorm2d-16             [-1, 16, 7, 7]              32
          Dropout-17             [-1, 16, 7, 7]               0
           Conv2d-18             [-1, 10, 7, 7]             160
           Conv2d-19             [-1, 10, 1, 1]           4,900
================================================================
Total params: 17,980
Trainable params: 17,980
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.31
Params size (MB): 0.07
Estimated Total Size (MB): 0.38
----------------------------------------------------------------
```
### Changes Performed:
 - After every convolution layer Batch Normalization is applied except for last 2 convolutional layers.
 - A small dropout value is added after Batch Normalization upto conv5 layers.
 - 2x2 Max Pooling is added at initial convolutional layers.
 - Learning rate has been reduced from 0.1 to 0.01

### Results Observed:
 - After multiple iterations and changing architecture, maximum test accuracy that was achieved was 99.34%
 - ![image](https://github.com/RaviNaik/ERA-S6-Assignment-Solution/assets/23289802/e97f982e-23d3-4f9b-960f-23265a4d737e)

