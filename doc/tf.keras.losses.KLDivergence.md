## tf.keras.losses.KLDivergence

### [tf.keras.losses.KLDivergence](https://www.tensorflow.org/api_docs/python/tf/keras/losses/KLDivergence)

```python
tf.keras.losses.KLDivergence(
    y_true,
    y_pred,
    sample_weight=None
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

#### 使用方式

TensorFlow：首先定义KLDivergence对象，定义对象时可以指定reduction

```python
__init__(
    reduction=losses_utils.ReductionV2.AUTO,
    name='kullback_leibler_divergence'
)
```

- 当`reduction=losses_utils.ReductionV2.AUTO`，大部分场合下等同于`SUM_OVER_BATCH_SIZE`
- 当`reduction=losses_utils.ReductionV2.None`，沿着特定的axis对损失值进行加权求和，结果是一个标量
- 当`reduction=losses_utils.ReductionV2.SUM`，对损失值进行加权求和，结果是一个标量
- 当`reduction=losses_utils.ReductionV2.SUM_OVER_BATCH_SIZE`，损失为：加权损失/batch_size，结果是一个标量

PaddlePaddle：提供op形式的调用接口，可以设置reduction参数，但是与TensorFlow不同：

- 当 `reduction` 为 `none` 时，输出损失与输入（x）形状相同，各点的损失单独计算，不应用reduction 。

- 当 `reduction` 为 `mean` 时，输出损失为[1]的形状，损失值为所有损失的平均值。

- 当 `reduction` 为 `sum` 时，输出损失为[1]的形状，损失值为所有损失的总和。

- 当 `reduction` 为 `batchmean` 时，输出损失为[1]的形状，损失值为所有损失的总和除以批量大小。

#### 参数种类

TensorFlow：有sample_weight参数，该参数可以设置loss的系数，用于对loss进行加权求和。

PaddlePaddle：无法对loss进行加权求和

#### 计算方式

API计算结果不一致。

TensorFlow：计算公式为`y_pred - y_true * log(y_pred)`，其中的对数是自然对数，即`ln`。

PaddlePaddle：计算公式为`l(x,target)=target∗(log(target)−x)`，其中的对数是自然对数，即`ln`