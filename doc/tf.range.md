## tf.range

### [tf.range](https://www.tensorflow.org/api_docs/python/tf/range)

```python
tf.range(
    limit,
    delta=1,
    dtype=None,
    name='range'
)

tf.range(
    start,
    limit,
    delta=1,
    dtype=None,
    name='range'
)
```

### [paddle.fluid.layers.range](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/tensor_cn.html#range)

```python
paddle.fluid.layers.range(
    start,
    end,
    step,
    dtype
)
```

### 功能差异

### 使用方式

TensorFlow：支持更丰富的使用方式

- 用户可以不指定start，仅指定limit设置range的上限，默认的delta为1。这种方式下，range可以接受1个参数。

  ```python
  limit = 5
  tf.range(limit)  # [0, 1, 2, 3, 4]
  ```

  

- 用户需同时指定start、limit，默认的delta为1，可以自行设置delta的值。这种方式下，range可接受2个及以上参数。

  ```python
  start = 1.0
  limit = 3.0
  tf.range(start, limit)  # [1., 2.]
  
  start = 3.0
  limit = 18.0
  delta = 3.0
  tf.range(start, limit, delta)  # [3.0, 6.0, 9.0, 12.0, 15.0]
  ```

  

PaddlePaddle：必须同时指定4个参数，缺一不可。