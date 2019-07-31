## tf.argsort

### [tf.argsort](https://www.tensorflow.org/api_docs/python/tf/argsort)

```python
tf.argsort(
    values,
    axis=-1,
    direction='ASCENDING',
    stable=False,
    name=None
)
```

### [paddle.fluid.layers.argsort](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/tensor_cn.html#argsort)
```python
paddle.fluid.layers.argsort(
    input, 
    axis=-1, 
    name=None
)
```

### 功能差异

#### 输入参数
TensorFlow：具有`direction`参数，表示排序方向；具有`stable`参数，表示是否是稳定排序，不稳定排序当前没有实现；  
PaddlePaddle：无`direction`和`stable`参数。

#### 输出差异
TensorFlow：只返回排序的索引；  
PaddlePaddle：返回排序的索引和一组已排序的数据变量。
