## tf.pad

### [tf.pad](https://www.tensorflow.org/api_docs/python/tf/pad)

```python
tf.pad(
    tensor,
    paddings,
    mode='CONSTANT',
    name=None,
    constant_values=0
)
```

### [paddle.fluid.layers.pad2d](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#pad2d)

```python
paddle.fluid.layers.pad2d(
    input,
    paddings=[0, 0, 0, 0],
    mode='constant',
    pad_value=0.0,
    data_format='NCHW',
    name=None
)
```

### 功能差异

#### 数据格式

TensorFlow：对输入数据格式没有明确限制。

PaddlePaddle：默认输入格式为`NCHW`，可以通过data_format参数设置输入格式为`NHWC`。

#### 参数差异

TensorFlow：paddings是一个tensor，它的rank和输入的tensor是一致的。padding的shape为(rank, 2)，表示每一维前后padding的长度。

PaddlePaddle：paddings可以是列表、元组或者tensor。如果paddings是元组，它必须包含四个整数， (padding_top, padding_bottom, padding_left, padding_right)。

