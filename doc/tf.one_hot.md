## tf.one_hot

### [tf.one_hot](https://www.tensorflow.org/api_docs/python/tf/one_hot)

```python
tf.one_hot(
    indices,
    depth,
    on_value=None,
    off_value=None,
    axis=None,
    dtype=None,
    name=None
)
```

### [paddle.fluid.layers.one_hot](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#one-hot)

```python
paddle.fluid.layers.one_hot(
    input,
    depth
)
```

### 功能差异

#### 参数差异

TensorFlow：indices对应PaddlePaddle API中的input，但TensorFlow对输入的indices限制更少，可以是标量，也可以是多维的tensor。

PaddlePaddle：输入的是tensor，最后一维必须为1。

### 参数种类

TensorFlow：具有额外的可选参数

- on_value，由索引表示的位置取值 on_value，默认为1
- off_value，非索引表示的位置取值off_value，默认为0
- axis，要填充的轴，默认为-1，即一个新的最内层轴
- dtype：设置输出tensor的数据类型