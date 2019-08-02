# tf.nn.avg_pool3d

### [tf.nn.avg_pool3d](https://www.tensorflow.org/api_docs/python/tf/nn/avg_pool3d)

```python
tf.nn.avg_pool3d(
    input,
    ksize,
    strides,
    padding,
    data_format='NDHWC',
    name=None
)
```

### [paddle.fluid.layers.pool3d](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#pool3d)

```python
paddle.fluid.layers.pool3d(
    input,
    pool_size=-1,
    pool_type='max',
    pool_stride=1,
    pool_padding=0,
    global_pooling=False,
    use_cudnn=True,
    ceil_mode=False,
    name=None,
    exclusive=True
)
```

### 功能差异

#### 数据格式

TensorFLow：默认输入数据格式为`NDHWC`，表示`(batch，depth, height, width, channel)`。如果将 `data_format`参数设置为`channels_first`，支持`NCDHW`格式的数据输入。

PaddlePaddle：只支持`NCDHW`格式的数据输入。

#### Padding机制

Tensorflow: 存在`SAME`和`VALID`两种padding方式

- 当`padding='SAME'`时:

  ```
  output_spatial_shape[i] = ceil(input_spatial_shape[i] / strides[i])
  ```

- 当`padding='VALID'`时：

  ```
  output_spatial_shape[i] = ceil(input_spatial_shape[i] - spatial_filter_shape[i] + 1) / strides[i])
  ```

PaddlePaddle：通过`pool_padding`设置对输入的填充大小，通过ceil_mode设置输出的shape计算方式，可实现Tensorflow中的`SAME`和`VALID`方式。

#### 使用方式

TensorFlow：只能实现average-pooling

PaddlePaddle：通过设置`pool_type='avg'`实现average-polling

