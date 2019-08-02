# tf.metrics.recall

### [tf.metrics.recall](https://www.tensorflow.org/api_docs/python/tf/metrics/recall)

```python
tf.metrics.recall(
    labels,
    predictions,
    weights=None,
    metrics_collections=None,
    updates_collections=None,
    name=None
)
```

### [paddle.fluid.metrics.Recall](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/metrics_cn.html#Recall)

```python
paddle.fluid.metrics.Recall(
    name=None
)
```

### 功能差异

#### 使用方式

TensorFlow：采用函数调用形式，将标签label和预测值predictions传入

PaddlePaddle：采用类对象定义形式，使用update方法更新true_positives和false_negtive变量，eval方法计算recall。

#### 参数种类

TenorsFlow：具有weights参数，通过weights中相应的值对每个prediction进行加权。

PaddlePaddle：没有weights参数

#### 返回值

TensorFlow：返回recall值与update_op，update_op是更新true_positives和false_positives变量的操作

PaddlePaddle：通过eval方法，返回recall值

