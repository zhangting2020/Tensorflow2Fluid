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

#### 实现方式

TensorFlow：默认情况下采用对数均匀分布采样（Zipfian）

PaddlePaddle：默认采用均匀分布采样（uniform）

#### 参数种类

TensorFlow：

- weight：类嵌入。shape为[num_classes, dim]的tensor；或者是Tensor对象列表，其沿着维度0被concat，shape为 [num_classes, dim]。
- bias：类偏差。shape为[num_classes]的tensor。
- inputs：输入网络的正向激活。shape为[batch_size, K]的tensor。
- labels：目标类。shape为[batch_size, num_true]的tensor。
- num_sampled：int，每批随机抽样的负类数目。
- num_classes：int，可能的类别数目。
- num_true：int，每个训练示例的目标类数目。
- sampled_values：由`* _candidate_sampler`函数返回的元组(sampled_candidates, true_expected_count, sampled_expected_count)。(如果是None，默认为log_uniform_candidate_sampler)。
- remove_accidental_hits：bool。如果采样类等于其中一个目标类，是否删除。如果设置为True,则这是“Sampled Logistic”损失，而不是NCE。默认值为False.
- partition_strategy：指定分区策略的字符串，如果len(weights) > 1则相关。目前支持"div"和"mod"，默认是"mod"。

PaddlePaddle：
下面的参数描述来源于官方文档。

- input (Variable) ：输入变量
- label (Variable) - 标签
- num_total_classes (int) - 所有样本中的类别的总数。（应该等同于TF的num_classes参数）
- sample_weight (Variable|None) - 存储每个样本权重，shape为[batch_size, 1]存储每个样本的权重。每个样本的默认权重为1.0
- param_attr (ParamAttr|None) - 可学习参数/nce权重可学习参数/nce权重 的参数属性。如果它没有被设置为ParamAttr的一个属性，nce将创建ParamAttr为param_attr。如没有设置param_attr的初始化器，那么参数将用Xavier初始化。默认值:None
- bias_attr (ParamAttr|bool|None) - nce偏置的参数属性。如果设置为False，则不会向输出添加偏置（bias）。如果值为None或ParamAttr的一个属性，则bias_attr=ParamAtt。如果没有设置bias_attr的初始化器，偏置将被初始化为零。默认值:None
- num_neg_samples (int) - 负样例的数量。默认值是10。（应该等同于TF的num_sampled）
- sampler (str) – 取样器，用于从负类别中进行取样。可以是 ‘uniform’, ‘log_uniform’ 或 ‘custom_dist’。 默认 ‘uniform’
- custom_dist (float[]) – 一个 float[] 并且它的长度为 `num_total_classes` 。 如果取样器类别为‘custom_dist’，则使用此参数。 custom_dist[i] 是第i个类别被取样的概率。默认为 None
- seed (int) – 取样器使用的seed。默认为0
- is_sparse (bool) – 标志位，指明是否使用稀疏更新, weight@GRADweight@GRAD 和 bias@GRADbias@GRAD 会变为 SelectedRows

