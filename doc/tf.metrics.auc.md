## tf.metrics.auc

### [tf.metrics.auc](https://www.tensorflow.org/api_docs/python/tf/metrics/auc)

```python
tf.metrics.auc(
    labels,
    predictions,
    weights=None,
    num_thresholds=200,
    metrics_collections=None,
    updates_collections=None,
    curve='ROC',
    name=None,
    summation_method='trapezoidal',
    thresholds=None
)
```

### [paddle.fluid.layers.auc](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/metric_op_cn.html#auc)
```python
paddle.fluid.layers.auc(
    input, 
    label, 
    curve='ROC', 
    num_thresholds=4095, 
    topk=1, 
    slide_steps=1
)
```

### 功能差异

#### 输出差异

TensorFlow: 返回`auc`和`update_op`，`update_op`适当增加`true_positives`,`true_negatives`,`false_positives` 和 `false_negatives`，其值与AUC匹配；  
PaddlePaddle: 只返回`auc`，无`update_op`。
