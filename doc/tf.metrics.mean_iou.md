## tf.metrics.mean_iou

### [tf.metrics.mean_iou](https://www.tensorflow.org/api_docs/python/tf/metrics/mean_iou)

```python
tf.metrics.mean_iou(
    labels,
    predictions,
    num_classes,
    weights=None,
    metrics_collections=None,
    updates_collections=None,
    name=None
)
```

### [paddle.fluid.layers.mean_iou](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#mean-iou)

```python
paddle.fluid.layers.mean_iou(
    input,
    label,
    num_classes
)
```

### 功能差异

#### 参数种类

TensorFlow：具有weights参数，labels和predictions之间计算出的平均iou，通过设置weights来加权。

PaddlePaddle：没有加权平均的功能，即等同于TensorFlow中weights为None的情况。

#### 返回值

TensorFlow：返回值是元组，（平均IoU，混淆矩阵）

PaddlePaddle：返回值是元组，（平均IoU，每个类别中错误的个数，每个类别中的正确的个数）

