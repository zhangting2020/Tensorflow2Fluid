## tf.contrib.layers.maxout

### [tf.contrib.layers.maxout](https://www.tensorflow.org/api_docs/python/tf/contrib/layers/maxout)

```python
tf.contrib.layers.maxout(
    inputs,
    num_units,
    axis=-1,
    scope=None
)
```

### [paddle.fluid.layers.maxout](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#maxout)

```python
paddle.fluid.layers.maxout(
    x,
    groups,
    name=None
)
```

### 功能差异

#### 数据格式

TensorFlow：输入的inputs形状为NHWC，表示（batch, height, width, channel）

PaddlePaddle：输入的x为NCHW

#### 参数差异

TensorFlow：

- num_units：表示maxout操作之后要保留的特征数目
- axis：指定了在哪一个dimension进行maxout操作

PaddlePaddle：

- group：指定将输入张量的channel通道维度进行分组的数目。输出的通道数量为通道数除以组数。与TensorFlow的联系是：channel / group = num_uints
- 没有axis参数，即只能在channel维度进行maxout操作