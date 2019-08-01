## tf.keras.layers.PReLU

### [class tf.keras.layers.PReLU](https://www.tensorflow.org/api_docs/python/tf/keras/layers/PReLU)

```python
__init__(
    alpha_initializer='zeros',
    alpha_regularizer=None,
    alpha_constraint=None,
    shared_axes=None,
    **kwargs
)
```

### [paddle.fluid.layers.prelu](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#prelu)

```python
paddle.fluid.layers.prelu(
    x,
    mode,
    param_attr=None,
    name=None
)
```

### 功能差异

#### 参数差异

TensorFlow：

- alpha_initializer：设置alpha的初始化函数
- alpha_regularizer：设置alpha的正则项
- alpha_constraint：设置alpha的约束项
- shared_axes：设置权重共享模式。如果为None，则每一个元素有一个独立的alpha值；通过设置该参数达到权重共享。

PaddlePaddle：没有关于alpha设置的参数。另外，通过mode指定权重共享模式，mode参数为一个string，可以是“all”、“channel”或“element”。