## tf.keras.losses.KLD

### [tf.keras.losses.KLD](https://www.tensorflow.org/api_docs/python/tf/keras/losses/KLD)

```python
tf.keras.losses.KLD(
    y_true,
    y_pred
)
```

### [paddle.fluid.layers.kldiv_loss](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#kldiv-loss)

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

TensorFlow：没有reduction参数设置，返回的是各点的损失

PaddlePaddle：可以通过reduction参数设置输出的损失值

- 当 `reduction` 为 `none` 时，输出损失与输入（x）形状相同，各点的损失单独计算，不应用reduction 。

- 当 `reduction` 为 `mean` 时，输出损失为[1]的形状，损失值为所有损失的平均值。

- 当 `reduction` 为 `sum` 时，输出损失为[1]的形状，损失值为所有损失的总和。

- 当 `reduction` 为 `batchmean` 时，输出损失为[1]的形状，损失值为所有损失的总和除以批量大小。

#### 计算方式

API计算结果不一致。

TensorFlow：计算公式为`y_pred - y_true * log(y_pred)`，其中的对数是自然对数，即`ln`。

PaddlePaddle：计算公式为`l(x,target)=target∗(log(target)−x)`，其中的对数是自然对数，即`ln`

