## tf.clip_by_value

### [tf.clip_by_value](https://www.tensorflow.org/api_docs/python/tf/clip_by_value)

```python
tf.clip_by_value(
    t,
    clip_value_min,
    clip_value_max,
    name=None
)
```

### [paddle.fluid.clip.GradientClipByValue](paddle.fluid.clip.``GradientClipByValue)

```python
paddle.fluid.clip.GradientClipByValue(
    max,
    min=None
)
```

### 功能差异

#### 使用方式

TensorFlow：采用函数调用形式，输入需要执行裁剪的tensor，返回裁剪后的结果；

PaddlePaddle：采用类对象定义形式，设置`GradientClipByNorm`对象为裁剪方式。