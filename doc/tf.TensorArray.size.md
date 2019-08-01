## tf.TensorArray.size

### [tf.TensorArray.size](https://www.tensorflow.org/api_docs/python/tf/TensorArray#size)

```python
size(
    name=None
)
```

### [paddle.fluid.layers.array_length](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/control_flow_cn.html#array-length)

```python
paddle.fluid.layers.array_length(
    array
)
```

### 功能差异

#### 使用方式
TensorFlow：首先定义`TensorArray`对象，然后调用`size`函数；   
PaddlePaddle：提供op形式的调用接口，输入装饰有`array`(LOD_TENSOR_ARRAY)，返回数组长度。