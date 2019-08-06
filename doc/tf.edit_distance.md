## tf.edit_distance

### [tf.edit_distance](https://www.tensorflow.org/api_docs/python/tf/edit_distance)

```python
tf.edit_distance(
    hypothesis,
    truth,
    normalize=True,
    name='edit_distance'
)
```



### [paddle.fluid.layers.edit_distance](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#edit-distance)

```python
paddle.fluid.layers.edit_distance(
    input,
    label,
    normalized=True,
    ignored_tokens=None
)
```

### 功能差异

#### 参数差异

TensorFlow：hypothesis和truth都是SparseTensor

PaddlePaddle：input和label都是LoDTensor；可以通过ignored_tokens参数，设置计算编辑距离前需要移除的token

#### 返回值

TensorFlow：返回rank为 R - 1 的dense Tensor，其中 R 是 SparseTensor 输入 hypothesis和 truth的rank。

PaddlePaddle：[batch_size,1]中序列到序列到编辑距离。

例如：对于dense shape为（2，1）的输入，TensorFlow返回的编辑距离shape为（2，），而PaddlePaddle返回的编辑距离shape则是（2，1）。