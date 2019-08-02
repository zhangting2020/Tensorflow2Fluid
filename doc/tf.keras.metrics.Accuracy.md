## tf.keras.metrics.Accuracy

### [tf.keras.metrics.Accuracy](https://www.tensorflow.org/api_docs/python/tf/keras/metrics/Accuracy#top_of_page)
```python
class tf.keras.metrics.Accuracy(
    name='accuracy',
    dtype=None
)
```

### [paddle.fluid.metrics.Accuracy](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/metrics_cn.html#accuracy)
```python
class paddle.fluid.metrics.Accuracy(
    name=None
)
```

### 功能差异

#### 类方法
TensorFlow：具有`result`、`reset_states`和`update_state`方法；
    
>`reset_states()`：重置计算结果；     
>`result()`：返回计算结果；  
>`update_state(y_true, y_pred, sample_weight=None)`：累计统计结果。
  
PaddlePaddle：具有  
> `update(value, weight)`：更新`mini batch`的结果，是将mini batch的准确率结果累计，功能与tensorflow的`update_state`函数相同；    
> `eval()`：返回所有累计结果的平均准确率（float或numpy.array）。

#### `update_state()`与`update()`的输入  
TensorFlow：`update_state()`函数输入真实值`y_true`与预测值`y_pred`，而不是争取率；同时，输入样本权重`sample_weight`； 
PaddlePaddle：`update()`函数输入每个mini batch的正确率`value`；同时输入batch大小表示权重`weight`。  