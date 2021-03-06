# Torch2KerasConverter
Convert torch t7 model to keras model and source

## Convert
```python
from Torch2KerasConverter.torch_to_keras import TorchToKeras

converter = TorchToKeras((96, 96, 3))

converter.torch_to_keras('nn4.small2.v1.new.t7', 'KerasSmall2V1')
...
```
Two file will be created ```KerasSmall2V1.py``` ```KerasSmall2V1.h5```

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
