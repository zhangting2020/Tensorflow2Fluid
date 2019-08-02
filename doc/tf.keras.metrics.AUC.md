## tf.keras.metrics.AUC

### [tf.keras.metrics.AUC](https://www.tensorflow.org/api_docs/python/tf/keras/metrics/AUC)

```python
class tf.keras.metrics.AUC(
    num_thresholds=200,
    curve='ROC',
    summation_method='interpolation',
    name=None,
    dtype=None,
    thresholds=None
)
```

### [paddle.fluid.metrics.Auc](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/metrics_cn.html#auc)
```python
class paddle.fluid.metrics.Auc(
    name, 
    curve='ROC', 
    num_thresholds=4095
)
```

### 功能差异

#### 类属性差异
TensorFlow：具有`summation_method`属性，表示求和的方法，如差值法`interpolation`；具有`thresholds`属性，表示阈值；具有`detype`属性，表示返回结果的类型；    
PaddlePaddle：不具有上述提到的3个属性。  