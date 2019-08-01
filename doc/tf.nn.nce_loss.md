## tf.nn.nce_loss

### [tf.nn.nce_loss](https://www.tensorflow.org/api_docs/python/tf/nn/nce_loss)

```python
tf.nn.nce_loss(
    weights,
    biases,
    labels,
    inputs,
    num_sampled,
    num_classes,
    num_true=1,
    sampled_values=None,
    remove_accidental_hits=False,
    partition_strategy='mod',
    name='nce_loss'
)
```

### [paddle.fluid.layers.nce](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#nce)

```python
paddle.fluid.layers.nce(
    input,
    label,
    num_total_classes,
    sample_weight=None,
    param_attr=None,
    bias_attr=None,
    num_neg_samples=None,
    name=None,
    sampler='uniform',
    custom_dist=None,
    seed=0,
    is_sparse=False
)
```

### 功能差异

#### 参数种类

TensorFlow：默认情况下采用对数均匀采样（Zipfian）

PaddlePaddle：默认采用均匀采样（uniform）

