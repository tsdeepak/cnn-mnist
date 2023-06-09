
##### Model
|     Layer (type)    |  Output Shape  | Param # |
| ------------------- | -------------- | ------- |
|    Conv2d-1         | [-1, 8, 28, 28] |    72   |
|   Dropout-2         | [-1, 8, 28, 28] |    0    |
|    ReLU-3           | [-1, 8, 28, 28] |    0    |
| BatchNorm2d-4       | [-1, 8, 28, 28] |    16   |
|    Conv2d-5         | [-1, 8, 28, 28] |   576   |
|   Dropout-6         | [-1, 8, 28, 28] |    0    |
|    ReLU-7           | [-1, 8, 28, 28] |    0    |
|   MaxPool2d-8       | [-1, 8, 14, 14] |    0    |
| BatchNorm2d-9       | [-1, 8, 14, 14] |    16   |
|   Conv2d-10         | [-1, 16, 14, 14] |  1,152  |
|  Dropout-11         | [-1, 16, 14, 14] |    0    |
|    ReLU-12          | [-1, 16, 14, 14] |    0    |
| BatchNorm2d-13      | [-1, 16, 14, 14] |    32   |
|   Conv2d-14         | [-1, 16, 14, 14] |  2,304  |
|  Dropout-15         | [-1, 16, 14, 14] |    0    |
|    ReLU-16          | [-1, 16, 14, 14] |    0    |
|  MaxPool2d-17       | [-1, 16, 7, 7]   |    0    |
| BatchNorm2d-18      | [-1, 16, 7, 7]   |    32   |
|   Conv2d-19         | [-1, 32, 7, 7]   |  4,608  |
|  Dropout-20         | [-1, 32, 7, 7]   |    0    |
|    ReLU-21          | [-1, 32, 7, 7]   |    0    |
| BatchNorm2d-22      | [-1, 32, 7, 7]   |    64   |
|   Conv2d-23         | [-1, 32, 7, 7]   |  9,216  |
|  Dropout-24         | [-1, 32, 7, 7]   |    0    |
|    ReLU-25          | [-1, 32, 7, 7]   |    0    |
| BatchNorm2d-26      | [-1, 32, 7, 7]   |    64   |
|   Conv2d-27         | [-1, 32, 7, 7]   |   1,024 |
|  Dropout-28         | [-1, 32, 7, 7]   |    0    |
|    ReLU-29          | [-1, 32, 7, 7]   |    0    |
| BatchNorm2d-30      | [-1, 32, 7, 7]   |    64   |
|   Conv2d-31         | [-1, 10, 7, 7]   |   330  |
|    ReLU-32          | [-1, 10, 7, 7]   |    0   |
|  AvgPool2d-33       | [-1, 10, 1, 1]   |    0   |
|    Flatten-34       |      [-1, 10]     |    0   |
| LogSoftmax-35       |      [-1, 10]     |    0   |

##### Features
- The network has a total of 35 layers, including convolutional layers, dropout layers, activation functions (ReLU), batch normalization layers, max pooling layers, average pooling layers, and the final flatten and log softmax layers.
- Total number of parameters is 19570.
- Network is divided into 3 Convolution blocks and 1 output block.
- Number of channels steadily increased to 32. Batch size fixed to 64
- MaxPool used after first 2 convolution blocks only.
- Max receptive field reached is 32.
- Batch normalisation and dropouts (5%) are used in all convolution layers except near output.
- The output layer uses 1x1 convolution before GAP layer
