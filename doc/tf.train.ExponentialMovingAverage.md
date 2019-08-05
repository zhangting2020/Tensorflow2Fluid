## tf.train.ExponentialMovingAverage

### [tf.train.ExponentialMovingAverage](https://www.tensorflow.org/api_docs/python/tf/train/ExponentialMovingAverage)

```python
class tf.train.ExponentialMovingAverage(
    decay,
    num_updates=None,
    zero_debias=False,
    name='ExponentialMovingAverage'
)
```

### [paddle.fluid.optimizer.ExponentialMovingAverage](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/optimizer_cn.html#exponentialmovingaverage)
```python
class paddle.fluid.optimizer.ExponentialMovingAverage(
    decay=0.999, 
    thres_steps=None, 
    name=None
)
```

### 功能差异

#### 参数名称
TensorFlow：设置衰减率的参数为`num_updates`；    
PaddlePaddle：设置衰减率的参数为`thres_steps`；

#### 参数种类
TensorFlow：具有参数`zero_debias`；  
PaddlePaddle：不具备上述参数；  

#### 类方法
TensorFlow：具有方法`apply`、`variables_to_restore`、`average`和`average_name`；  
PaddlePaddle：具有方法`apply`、`restore`和`update`，不具有`average`和`average_name`；