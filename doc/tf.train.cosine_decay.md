## tf.train.cosine_decay

### [tf.train.cosine_decay](https://www.tensorflow.org/api_docs/python/tf/train/cosine_decay)

```python
tf.train.cosine_decay(
    learning_rate,
    global_step,
    decay_steps,
    alpha=0.0,
    name=None
)
```

### [paddle.fluid.layers.cosine_decay](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/learning_rate_scheduler_cn.html#cosine-decay)
```python
paddle.fluid.layers.cosine_decay(
    learning_rate,
    step_each_epoch, 
    epochs
)
```

### 功能差异

#### 输入参数

TensorFlow: 有`alpha`参数，表示最小学习率，默认值为0.0；  
PaddlePaddle: 无`alpha`参数；

#### 计算方式

TensorFlow: 学习率中有`alpha`参数，作为学习率的一部分；`cosin`值的计算中，比值部分使用 `pi * global_step/decay_steps`;  
PaddlePaddle: 学习率中没有`alpha`参数；`cosin`值的计算中，比值部分使用 `pi * step_each_epoch/epochs`。