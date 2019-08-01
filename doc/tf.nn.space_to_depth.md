## tf.nn.space_to_depth

### [tf.nn.space_to_depth](https://www.tensorflow.org/versions/r1.12/api_docs/python/tf/nn/space_to_depth)

```python
tf.nn.space_to_depth(
    input,
    block_size,
    name=None,
    data_format='NHWC'
)
```

### [paddle.fluid.layers.space_to_depth](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#space-to-depth)

```python
paddle.fluid.layers.space_to_depth(
    x,
    blocksize,
    name=None
)
```

### 功能差异

#### 数据格式

TensorFlow：输入默认是NHWC格式，即（batch，Height，Width，Channel）。

PaddlePaddle：输入只能是NCHW的格式。

#### 参数种类

TensorFlow：具有data_format参数，可以通过该参数设置输入和输出tensor的数据格式，支持“NHWC”，“NCHW”，“NCHW_VECT_C”：qint8 [ batch，channels / 4，height， width,4 ]。

PaddlePaddle：没有data_format参数。