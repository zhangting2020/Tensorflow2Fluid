## tf.metrics.precision

### [tf.metrics.precision](https://www.tensorflow.org/api_docs/python/tf/metrics/precision)

```python
tf.metrics.precision(
    labels,
    predictions,
    weights=None,
    metrics_collections=None,
    updates_collections=None,
    name=None
)
```

### [paddle.fluid.metrics.Precision](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/metrics_cn.html#precision)

```python
paddle.fluid.metrics.Precision(
    name=None
)
```

### 功能差异

#### 使用方式

TensorFlow：采用函数调用形式，将标签label和预测值predictions传入

PaddlePaddle：采用类对象定义形式，使用update方法更新true_positives和false_positives变量，eval方法计算precision。

#### 参数种类

TenorsFlow：具有weights参数，通过weights中相应的值对每个prediction进行加权。

PaddlePaddle：没有weights参数

#### 返回值

TensorFlow：返回precision值与update_op，update_op是更新true_positives和false_positives变量的操作

PaddlePaddle：通过eval方法，返回precision值

