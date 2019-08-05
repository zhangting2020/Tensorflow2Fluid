## tf.nn.conv3d

### [tf.nn.conv3d](https://www.tensorflow.org/versions/r1.13/api_docs/python/tf/nn/conv3d)

```python
tf.nn.conv3d(
    input,
    filter,
    strides,
    padding,
    data_format='NDHWC',
    dilations=[1, 1, 1, 1, 1],
    name=None
)
```

### [paddle.fluid.layers.conv3d](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#conv3d)

```python
paddle.fluid.layers.conv3d(
    input,
    num_filters,
    filter_size,
    stride=1,
    padding=0,
    dilation=1,
    groups=None,
    param_attr=None,
    bias_attr=None,
    use_cudnn=True,
    act=None,
    name=None
)
```

### 功能差异

#### 数据格式

TensorFlow: 默认输入数据格式为`NDHWC`，表示`(batch，depth, height, width, in_channels)`， 同时也可以将`data_format`参数设为`channels_first`，支持`NCDHW`格式的数据输入。其中输入、输出、卷积核对应关系如下表所示，

| 输入 | 卷积核 | 输出 |
|:--------------------:|:-------------------:|:------------------:|
| NDHWC | (kernel_d, kernel_h, kernel_w, filters_num, in_channels) | (batch, out_d, out_h, out_w, filters_num) |
| NCDHW | (kernel_d, kernel_h, kernel_w, filters_num, in_channels) | (batch, filters_num, out_d, out_h, out_w) |

PaddlePaddle：只支持输入数据格式为`NCDHW`，且卷积核格式与TensorFlow不同，其中输入、输出、卷积核对应关系如下表所示，

| 输入 | 卷积核 | 输出 |
|:-------------------:|:-------------------:|:------------------:|
|NCDHW | (in_channels, filters_num, kernel_d, kernel_h, kernel_w) | (batch, filters_num, out_d, out_h, out_w)|

#### Padding机制

TensorFlow: `SAME`和`VALID`两种选项。
- 当`padding='SAME'`时:

  ```
  output_spatial_shape[i] = ceil(input_spatial_shape[i] / strides[i])
  ```

- 当`padding='VALID'`时：

  ```
  output_spatial_shape[i] = ceil((input_spatial_shape[i] - (spatial_filter_shape[i]-1) * dilation_rate[i]) / strides[i])
  ```

PaddlePaddle：padding表示在输入图像四周填充的大小。如果填充（padding）为元组，则必须包含三个整型数，(padding_D, padding_H, padding_W)。否则， padding_D = padding_H = padding_W = padding。默认：padding = 0

