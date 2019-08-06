## tf.math.pow

### [tf.math.pow](https://www.tensorflow.org/api_docs/python/tf/math/pow)

```python
tf.math.pow(
    x,
    y,
    name=None
)
```

### [paddle.fluid.layers.elementwise_pow](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#elementwise-pow)

```python
paddle.fluid.layers.elementwise_pow(
    x,
    y,
    axis=-1,
    act=None,
    name=None
)
```

### 功能差异

#### 参数类型

TensorFlow：输入的x和y支持int类型

PaddlePaddle：输入的x和y不支持int类型，只能是float32或者float64

#### 参数种类

TensorFlow：没有axis和act参数。

PaddlePaddle：

- axis：将Y传到X上的起始维度索引。
- act：激活函数名称，应用于输出。

#### 其他

TensorFlow支持双向的broadcasting，PaddlePaddle只支持单向的broadcasting。

