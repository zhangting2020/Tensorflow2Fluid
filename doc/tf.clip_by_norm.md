## tf.clip_by_norm

### [tf.clip_by_norm](https://www.tensorflow.org/api_docs/python/tf/clip_by_norm)

```python
tf.clip_by_norm(
    t,
    clip_norm,
    axes=None,
    name=None
)
```

### [paddle.fluid.clip.GradientClipByNorm](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/clip_cn.html#gradientclipbynorm)

```python
paddle.fluid.clip.GradientClipByNorm(
    clip_norm
)
```

### 功能差异

#### 使用方式

TensorFlow：采用函数调用形式，输入需要执行norm裁剪的tensor，返回裁剪后的结果；

PaddlePaddle：采用类对象定义形式，使用设置`GradientClipByNorm`对象为裁剪方式。

#### 参数种类

TensorFlow：axes参数是1-D的tensor，包含用于计算L2范数的维度。如果为None，则使用所有维度。

PaddlePaddle：没有此参数

