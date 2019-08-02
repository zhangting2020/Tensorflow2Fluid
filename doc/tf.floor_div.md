## tf.floor_div

### [tf.floor_div](https://www.tensorflow.org/api_docs/python/tf/floor_div)

```python
tf.floor_div(
    x,
    y,
    name=None
)
```

### [paddle.fluid.layers.elementwise_floordiv](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#elementwise-floordiv)
```python
paddle.fluid.layers.elementwise_floordiv(
    x, 
    y, 
    axis=-1, 
    act=None, 
    name=None
)
```

### 功能差异

#### 输入类型
TensorFlow：不具有`axis`参数；    
PaddlePaddle：具有`axis`参数，表示将`y`传到`x`上的起始维度索引。

#### 输入维度
TensorFlow：参数`x`和`y`的维度须相同；    
PaddlePaddle：参数`y`的维度小于等于`x`的维度。