## tf.losses.cosine_distance

### [tf.losses.cosine_distance](https://www.tensorflow.org/api_docs/python/tf/losses/cosine_distance)

```python
tf.losses.cosine_distance(
    labels,
    predictions,
    axis=None,
    weights=1.0,
    scope=None,
    loss_collection=tf.GraphKeys.LOSSES,
    reduction=Reduction.SUM_BY_NONZERO_WEIGHTS,
    dim=None
)
```

### [paddle.fluid.layers.cos_sim](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#cos-sim)
```python
paddle.fluid.layers.cos_sim(
    X, 
    Y
)
```

### 功能差异

#### 参数类型
TensorFlow：具有`axis`和`weights`参数，`axis`表示计算余弦距离所在的维度，`weights`表示计算权重；    
PaddlePaddle：不具备以上参数； 