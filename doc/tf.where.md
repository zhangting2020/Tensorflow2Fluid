## tf.where

### [tf.where](https://www.tensorflow.org/api_docs/python/tf/where)

```python
tf.where(
    condition,
    x=None,
    y=None,
    name=None
)
```

### [paddle.fluid.layers.where](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/nn_cn.html#where)

```python
paddle.fluid.layers.where(
    condition
)
```

### 功能差异

#### 参数种类

TensorFlow：多了x和y两个参数，可以拥有更丰富的功能。

- 当仅传入condition参数时，与PaddlePaddle功能一致，都是返回condition中元素为True对应的索引：

  ```python
  condition = [[True,False,False],
               [False,True,True]]   
  结果:
   [[0 0]
    [1 1]
    [1 2]]
  ```
  
- 同时传入condition、 x和 y3个参数，且3个参数具有相同shape。返回值遵循规则：condition中元素为True的元素替换为x中的元素，为False的元素替换为y中对应元素。返回值与输入的参数具有相同shape。

  ```python
  x = [[1,2,3],[4,5,6]]
  y = [[7,8,9],[10,11,12]]
  condition3 = [[True,False,False],
               [False,True,True]]
  结果：
  [[ 1  8  9]
   [10  5  6]]
  ```

PaddlePaddle：只包含TensorFlow相应API中的第一条功能。