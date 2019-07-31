## tf.nn.elu

### [tf.nn.elu](https://www.tensorflow.org/api_docs/python/tf/nn/elu)

```python
tf.nn.elu(
    features,
    name=None
)
```

### [paddle.fluid.layers.elu](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#elu)

```python
paddle.fluid.layers.elu(
    x,
    alpha=1.0,
    name=None
)
```

### 功能差异

#### 参数差异

TensorFlow：无法设置alpha参数

PaddlePaddle：可以设置alpha参数

#### 计算方式

TensorFlow：if < 0： `exp(features) - 1` , 否则 `features` ，即固定了alpha参数为1。

PaddlePaddle：用户可以设置alpha参数，使用默认值时，与TensorFlow计算结果一致。

