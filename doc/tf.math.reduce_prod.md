## tf.math.reduce_prod

### [tf.math.reduce_prod](https://www.tensorflow.org/api_docs/python/tf/math/reduce_prod)

```python
tf.math.reduce_prod(
    input_tensor,
    axis=None,
    keepdims=None,
    name=None,
    reduction_indices=None,
    keep_dims=None
)
```

### [paddle.fluid.layers.reduce_prod](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#reduce-prod)
```python
paddle.fluid.layers.reduce_prod(
    input, 
    dim=None, 
    keep_dim=False, 
    name=None
)
```

### 功能差异

#### 参数名称
TensorFlow：使用`axis`表示运算维度；使用`keepdims`表示是否保留减小的维度；参数`reduction_indices`和`keep_dims`将被废弃；    
PaddlePaddle：使用`dim`表示运算维度；使用`keep_dim`表示是否保留减小的维度。  