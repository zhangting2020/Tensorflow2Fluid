## tf.keras.preprocessing.sequence.pad_sequences

### [tf.keras.preprocessing.sequence.pad_sequences](https://www.tensorflow.org/api_docs/python/tf/keras/preprocessing/sequence/pad_sequences)

```python
tf.keras.preprocessing.sequence.pad_sequences(
    sequences,
    maxlen=None,
    dtype='int32',
    padding='pre',
    truncating='pre',
    value=0.0
)
```

### [paddle.fluid.layers.sequence_pad](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#sequence-pad)

```python
paddle.fluid.layers.sequence_pad(
    x,
    pad_value,
    maxlen=None,
    name=None
)
```

### 功能差异

#### 参数种类

TensorFlow：提供了dtype，padding和truncating这3个额外的参数。

- dtype：设置输出序列的type
- padding：string类型，可以是“pre”或者“post”，分别表示在每个序列的开头或者结尾进行pad操作
- truncating：string类型，可以是“pre”或者“post”，分别表示在序列的开头或结尾处从大于“maxlen”的序列中删除值。

PaddlePaddle：没有上述额外的参数设置，仅在序列结尾处进行pad。

#### 返回值

TensorFlow：返回对序列进行pad后的结果

PaddlePaddle：返回的是元组（对序列进行pad后的结果，pad前的初始长度）