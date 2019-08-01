## tf.nn.selu

### [tf.nn.selu](https://www.tensorflow.org/api_docs/python/tf/nn/selu)

```python
tf.nn.selu(
    features,
    name=None
)
```

### [paddle.fluid.layers.selu](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#selu)
```python
paddle.fluid.layers.selu(
    x, 
    scale=None, 
    alpha=None, 
    name=None
)
```

### 功能差异

#### 参数种类
TensorFlow：不具有`scale`和`alpha`参数，只能使用默认值；  
PaddlePaddle：具有`scale`和`alpha`参数，可以订制这两个参数的值； 