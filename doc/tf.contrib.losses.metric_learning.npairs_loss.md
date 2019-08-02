## tf.contrib.losses.metric_learning.npairs_loss

### [tf.contrib.losses.metric_learning.npairs_loss](https://www.tensorflow.org/api_docs/python/tf/contrib/losses/metric_learning/npairs_loss)

```python
tf.contrib.losses.metric_learning.npairs_loss(
    labels,
    embeddings_anchor,
    embeddings_positive,
    reg_lambda=0.002,
    print_losses=False
)
```

### [paddle.fluid.layers.npair_loss](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#npair-loss)
```python
paddle.fluid.layers.npair_loss(
    anchor, 
    positive, 
    labels, 
    l2_reg=0.002
)
```

### 功能差异

#### 参数维度
TensorFlow：参数`labels`维度是[batch_size/2]，参数`embeddings_anchor`和`embeddings_positive`的维度均是[batch_size/2, embedding_dims]；    
PaddlePaddle：参数`labels`维度是[batch_size]，参数`anchor`和`positive`的维度均是[batch_size/2, embedding_dims]； 