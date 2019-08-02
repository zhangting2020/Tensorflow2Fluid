## tf.math.not_equal

### [tf.math.not_equal](https://tensorflow.google.cn/api_docs/python/tf/math/not_equal)

```python
tf.math.not_equal(
    x,
    y,
    name=None
)
```

### [paddle.fluid.layers.not_equal](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/control_flow_cn.html#not-equal)

```python
paddle.fluid.layers.not_equal(
    x,
    y,
    cond=None
)
```

### 功能差异

#### 使用方式

TensorFlow：支持双向的broadcasting

PaddlePaddle：仅支持单向的broadcasting，要求x的dimensions size >= y的dimensions size。

