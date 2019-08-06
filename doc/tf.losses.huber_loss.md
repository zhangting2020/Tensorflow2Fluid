## tf.losses.huber_loss

### [tf.losses.huber_loss](https://www.tensorflow.org/api_docs/python/tf/losses/huber_loss)

```python
tf.losses.huber_loss(
    labels,
    predictions,
    weights=1.0,
    delta=1.0,
    scope=None,
    loss_collection=tf.GraphKeys.LOSSES,
    reduction=Reduction.SUM_BY_NONZERO_WEIGHTS
)
```

### [paddle.fluid.layers.huber_loss](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#huber-loss)

```python
paddle.fluid.layers.huber_loss(
    input,
    label,
    delta
)
```

### 功能差异

#### 参数差异

TensorFlow：

- weights参数可以设置loss的系数。如果weights是标量，loss的数值就与该标量值相乘；如果weighs是一个size = batch_size的tensor，则会将weights向量中的相应元素乘以该batch中每个样本的损失；如果weights的shape与predictions的shape一致，则weights与predictions中对应元素的loss相乘。
- reduction参数设置了应用在loss上的reduction类型。
- 输入的labels和predictions只需要具有相同的dimensions

PaddlePaddle：

- 没有相应设置
- 输入的input和label必须具有相同的shape。

#### 返回值

TensorFlow：加权loss。如果reduction为NONE，返回值与labes具有相同shape，否则是一个标量。

PaddlePaddle：形为[batch_size, 1]的huber loss，形状与labels相同。



