## tf.io.read_file

### [tf.io.read_file](https://www.tensorflow.org/api_docs/python/tf/io/read_file)

```python
tf.io.read_file(
    filename,
    name=None
)
```

### [paddle.fluid.layers.read_file](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/io_cn.html#read-file)

```python
paddle.fluid.layers.read_file(
    reader
)
```

### 功能差异

#### 参数类型

TensorFlow：输入的filename是一个string类型，表示文件的路径

PaddlePaddle：输入的是reader变量，是一个生成器

