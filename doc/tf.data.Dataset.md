:## tf.data.Dataset.batch

### [tf.data.Dataset.batch](https://www.tensorflow.org/api_docs/python/tf/data/Dataset#batch)

```python
batch(
    batch_size,
    drop_remainder=False
)
```

### [paddle.fluid.layers.batch](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/io_cn.html#batch)
```python
paddle.fluid.layers.batch(
    reader, 
    batch_size
)
```

### 功能差异

#### 输入参数

TensorFlow：具有可选参数`drop_remainder`，表示当最后一个batch元素少于`batch_size`时是否舍弃；  
PaddlePaddle：缺少参数`drop_remainder`。

#### 使用方式
TensorFlow：首先定义`Dataset`对象，然后调用`batch`函数；   
PaddlePaddle：提供op形式的调用接口，输入装饰有`batching`的`reader`变量，返回装饰有`batching`的`reader`变量。


