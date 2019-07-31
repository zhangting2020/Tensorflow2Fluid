## tf.linalg.diag

### [tf.linalg.diag](https://www.tensorflow.org/api_docs/python/tf/linalg/diag)

```python
tf.linalg.diag(
    diagonal,
    name=None
)
```

### [paddle.fluid.layers.diag](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/tensor_cn.html#diag)
```python
paddle.fluid.layers.diag(
    diagonal
)
```

### 功能差异

#### 输入类型
TensorFlow：`diagonal` 是`Tensor`类型；  
PaddlePaddle：`diagonal`是`Variable`或者`numpy.ndarray`类型。  

#### 输入维度
TensorFlow：`diagonal`秩为`k`，`k>=1`；    
PaddlePaddle：`diagonal`秩为1。