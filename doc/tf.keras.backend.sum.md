## tf.keras.backend.sum

### [tf.keras.backend.sum](https://www.tensorflow.org/api_docs/python/tf/keras/backend/sum)

```python
tf.keras.backend.sum(
    x,
    axis=None,
    keepdims=False
)

```

### [paddle.fluid.layers.sum](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#sum)
```python
paddle.fluid.layers.sum(
    x
)
```

### 功能差异

#### 参数种类
TensorFlow：具有`axis`参数，表示需要加和的轴；具有`keepdims`参数，表示是否保留原尺寸；  
PaddlePaddle：没有`axis`参数，无法沿指定轴加和；无`keepdims`参数。 

#### 输入类型
TensorFlow：参数`x`类型是`Tensor`；  
PaddlePaddle：参数`x`类型是`list`，其元素是`Tensor`。


#### 其他
TensorFlow：本质上是和`reduce_sum()`功能一致；  
PaddlePaddle：输入`x`中多个`Tensor`的求和。  