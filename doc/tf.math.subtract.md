## tf.math.subtract

### [tf.math.subtract](https://www.tensorflow.org/versions/r1.13/api_docs/python/tf/math/subtract)

```python
tf.math.subtract(
    x,
    y,
    name=None
)
```

### [ fluid.layers.elementwise_sub](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#elementwise-sub)

```python
fluid.layers.elementwise_sub(
    x,
    y,
    axis=-1,
    act=None,
    name=None
)
```

### 功能差异

#### 参数种类

PaddlePaddle：具有axis参数，设置将y传到x上的起始维度索引；act参数设置激活函数名称，应用于输出。

#### 其他

TensorFlow支持双向的broadcasting，PaddlePaddle只支持单向的broadcasting。

