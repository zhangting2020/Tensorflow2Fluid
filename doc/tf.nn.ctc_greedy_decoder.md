## tf.nn.ctc_greedy_decoder

### [tf.nn.ctc_greedy_decoder](https://www.tensorflow.org/api_docs/python/tf/nn/ctc_greedy_decoder?hl=en)
```python
tf.nn.ctc_greedy_decoder(
    inputs,
    sequence_length,
    merge_repeated=True
)
```

### [paddle.fluid.layers.ctc_greedy_decoder](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#paddle.fluid.layers.ctc_greedy_decoder)
```python
paddle.fluid.layers.ctc_greedy_decoder(
    input, 
    blank, 
    name=None
)
```

### 功能差异

#### 输入维度
TensorFlow：输入参数`inputs`是三维的`float Tensor`，大小是`sized [max_time, batch_size, num_classes]`；     
PaddlePaddle：输入参数`input`是二维张量。它的形状是`[Lp, num_classes+1]`，其中`Lp`是所有输入序列长度的和。

#### 输入参数
TensorFlow：具有参数`sequence_length`和`merge_repeated`；  
PaddlePaddle：无上述参数，具有`blank`参数。  

#### 输出
TensorFlow：返回一个元组`(decoded, neg_sum_logits)`；  
PaddlePaddle：解码算法返回形状未`(Lp, 1)`的二维张量。 