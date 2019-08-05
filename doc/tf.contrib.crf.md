## tf.contrib.crf

### [tf.contrib.crf](https://www.tensorflow.org/api_docs/python/tf/contrib/crf)

```python

```

### [paddle.fluid.layers.linear_chain_crf](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#linear-chain-crf)
```python
paddle.fluid.layers.linear_chain_crf(
    input, 
    label, 
    param_attr=None
)
```

### 功能差异

#### 算法差异
TensorFlow：实现了linear-chain CRF的前向、反向算法和计算alpha的算法；  
PaddlePaddle：实现了linear chain CRF的前向和反向算法，未实现计算alpha的算法。 