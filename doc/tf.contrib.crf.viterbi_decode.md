## tf.contrib.crf.viterbi_decode

### [tf.contrib.crf.viterbi_decode](https://www.tensorflow.org/api_docs/python/tf/contrib/crf/viterbi_decode)

```python
tf.contrib.crf.viterbi_decode(
    score,
    transition_params
)
```

### [paddle.fluid.layers.crf_decoding](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#crf-decoding)

```python
paddle.fluid.layers.crf_decoding(
    input,
    param_attr,
    label=None
)
```

### 功能差异

#### 参数差异

TensorFlow：输入score是一个shape为 `[seq_len, num_tags]`的一元势函数矩阵。输入transition_params是shape为`[num_tags, num_tags]`的二元势函数矩阵。

PaddlePaddle：输入input 是一个形为 [N x D] 的LoDTensor，其中 N 是mini-batch的大小，D是标注（tag) 的总数，该输入是 linear_chain_crf 的 unscaled emission weight matrix （未标准化的发射权重矩阵）。param_attr 是参与训练的参数的属性。

#### 返回值

TensorFlow：**viterbi**：一个形状为`[seq_len]` 包含最高分标签索引的列表；**viterbi_score**：一个浮点数，代表了viterbi序列的分数。

PaddlePaddle：Label 非None的情况，会返回一行形为[N X 1]的向量，其中值为0的部分代表该label不适合作为对应结点的标注，值为1的部分则反之。当没有 Label 时，返回一个形为 [N X 1]的向量，其中元素取值范围为 0 ~ 最大标注个数-1，分别为预测出的标注（tag）所在的索引。

