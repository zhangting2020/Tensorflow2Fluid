## tf.math.multiply

### [tf.math.multiply](https://www.tensorflow.org/api_docs/python/tf/math/multiply)

```python
tf.math.multiply(
    x,
    y,
    name=None
)
```

### [fluid.layers.elementwise_mul](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#elementwise-mul)

```python
fluid.layers.elementwise_mul(
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

