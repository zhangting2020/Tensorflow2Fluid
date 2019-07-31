## tf.math.floormod

### [tf.math.floormod](https://www.tensorflow.org/api_docs/python/tf/math/floormod)

```python
tf.math.floormod(
    x,
    y,
    name=None
)
```

### [paddle.fluid.layers.elementwise_mod](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#elementwise-mod)

```python
paddle.fluid.layers.elementwise_mod(
    x,
    y,
    axis=-1,
    act=None,
    name=None
)
```

### 功能差异

#### 计算方式

当x与y中的元素都为正数时，结果具有一致性。当x与y的符号不同时，计算结果具有差异：

TensorFlow：计算公式是取模运算，`mod(x, y) = x - floor(x/ y) * y`

PaddlePaddle：c++的底层实现，实际是取余（%），计算公式`mod(x,y) = x - fix(x/y) * y`。其中`fix`表示向0方向舍入。

#### 其他

TensorFlow支持双向的broadcasting，PaddlePaddle只支持单向的broadcasting。

