# Torch2KerasConverter
Convert torch t7 model to keras model and source

## Convert
```python
from torch_to_keras import TorchToKeras

converter = TorchToKeras((96, 96, 3))  # input shape

converter.torch_to_keras('nn4.small2.v1.t7', 'nn4.small2.v1.keras')
...
```
Two file will be created ```nn4.small2.v1.keras.py``` ```nn4.small2.v1.keras.h5```

## Layers
Currently the converter works for the following Torch layers.

* SpatialConvolution and nn.SpatialConvolutionMM
* SpatialBatchNormalization
* ReLU
* Sequential
* SpatialMaxPooling
* SpatialCrossMapLRN
* SpatialLPPooling
* Square
* SpatialAveragePooling
* MulConstant
* Sqrt
* Reshape and View
* Linear
* Normalize
* DepthConcat
* nn.Inception
