## tf.zeros_like

### [tf.zeros_like](https://www.tensorflow.org/api_docs/python/tf/zeros_like)

```python
tf.zeros_like(
    tensor,
    dtype=None,
    name=None,
    optimize=True
)
```

### [paddle.fluid.layers.zeros_like](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/tensor_cn.html#zeros-like)

```python
paddle.fluid.layers.zeros_like(
    x,
    out=None
)
```

### 功能差异

#### 参数种类

TensorFlow：如果用户不主动设置dtype，返回值是与参数tensor同样类型和shape的全零张量。另外可以通过设置dtype改变返回的张量的类型。如果optimize参数设置为True，尝试去静态地决定`tensor` 的形状（shape）并将其编码为一个常量。默认为True。

PaddlePaddle：返回值的类型与输入的x一致，无法重新设置。没有optimize参数的设置。