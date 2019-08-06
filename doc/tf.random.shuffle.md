## tf.random.shuffle

### [tf.random.shuffle](https://www.tensorflow.org/api_docs/python/tf/random/shuffle)
```python
tf.random.shuffle(
    value,
    seed=None,
    name=None
)
```

### [fluid.layers.shuffle](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/io_cn.html#shuffle)
```python
paddle.fluid.layers.shuffle(
    reader,
    buffer_size
)
```

### 功能差异

#### 参数类型

TensorFlow：输入的value是待shuffle的Tensor

PaddlePaddle：输入的reader是一个读取器（callable）

#### 返回值类型

TensorFlow：返回的是与value具有相同shape的Tensor

PaddlePaddle：返回的是输出数据被shuffle的读取器（callable）

#### 参数种类

TensorFlow：具有seed参数，可设置随机种子

PaddlePaddle：没有seed参数

