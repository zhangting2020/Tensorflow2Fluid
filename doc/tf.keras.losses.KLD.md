## tf.keras.losses.KLD

### [tf.keras.losses.KLD](https://www.tensorflow.org/api_docs/python/tf/keras/losses/KLD)

```python
tf.keras.losses.KLD(
    y_true,
    y_pred
)
```

### [paddle.fluid.layers.kldiv_loss](https://www.paddlepaddle.org.cn/documentation/docs/en/1.5/api/layers/nn.html#kldiv-loss)

```python
paddle.fluid.layers.kldiv_loss(
    x,
    target,
    reduction='mean',
    name=None
)
```

### 功能差异

#### 参数种类

TensorFlow：没有reduction参数设置

PaddlePaddle：可以通过reduction参数设置输出的损失值

- 当 `reduction` 为 `none` 时，输出损失与输入（x）形状相同，各点的损失单独计算，不应用reduction 。

- 当 `reduction` 为 `mean` 时，输出损失为[1]的形状，损失值为所有损失的平均值。

- 当 `reduction` 为 `sum` 时，输出损失为[1]的形状，损失值为所有损失的总和。

- 当 `reduction` 为 `batchmean` 时，输出损失为[1]的形状，损失值为所有损失的总和除以批量大小。

#### 计算方式

二者计算公式均为`y_pred - y_true * log(y_pred)`，但是其中的对数函数不同

TensorFlow：源码中调用的是math_ops.log，实际是自然对数，即`ln`

```python
return math_ops.reduce_sum(y_true * math_ops.log(y_true / y_pred), axis=-1)
```

PaddlePaddle：使用的对数函数是log，即以10为底的对数。

