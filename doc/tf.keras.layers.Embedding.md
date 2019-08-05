## tf.keras.layers.Embedding 

### [tf.keras.layers.Embedding](https://www.tensorflow.org/api_docs/python/tf/keras/layers/Embedding?hl=en)

```python
class tf.keras.layers.Embedding(
    input_dim,
    output_dim,
    embeddings_initializer='uniform',
    embeddings_regularizer=None,
    activity_regularizer=None,
    embeddings_constraint=None,
    mask_zero=False,
    input_length=None,
    **kwargs
)
```

### [paddle.fluid.layers.embedding](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#embedding)
```python
paddle.fluid.layers.embedding(
    input,
    size,
    s_sparse=False,
    is_distributed=False,
    padding_idx=None,
    param_attr=None,
    dtype='float32'
)
```

### 功能差异

#### 输入形状
TensorFlow：用2个参数`input_dim`和`output_dim`分别表示词典大小和嵌入向量的大小；    
PaddlePaddle：用1个参数`size`(list|tuple)中的两个参数分别表示词典大小和嵌入向量的大小。  

#### 参数种类1
TensorFlow：具有参数`embeddings_initializer`、`embeddings_regularizer`、`embeddings_constraint`和`mask_zero`；  
PaddlePaddle：不具有上述参数。 

#### 参数种类2
TensorFlow：不具有以下参数；  
PaddlePaddle：具有参数`s_sparse`、`is_distributed`、`padding_idx`、`param_attr`和`dtype`。