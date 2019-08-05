## tf.contrib.image.bipartite_match

### [tf.contrib.image.bipartite_match](https://www.tensorflow.org/api_docs/python/tf/contrib/image/bipartite_match)

```python
tf.contrib.image.bipartite_match(
    distance_mat,
    num_valid_rows,
    top_k=-1,
    name='bipartite_match'
)
```

### [paddle.fluid.layers.bipartite_match](https://www.paddlepaddle.org.cn/documentation/docs/zh/1.5/api_cn/layers_cn/detection_cn.html#bipartite-match)

```python
paddle.fluid.layers.bipartite_match(
    dist_matrix,
    match_type=None,
    dist_threshold=None,
    name=None
)
```

### 功能差异

####  参数差异

TensorFlow：需要指定num_valid_rows参数，该参数是一个标量或1-D张量，描述了对于二分匹配要考虑的distance_mat的有效行数。如果设置为负数，则使用所有行。top_k参数是一个标量，指定要检索的top-k匹配数。如果设置为负数，则采置`distance_mat`的最大匹配数设置。

PaddlePaddle：具有match_type参数，该参数设置匹配方法的类型，应为‘bipartite’或’per_prediction’，默认采用二分法。具有dist_threshold参数，如果match_type为’per_prediction’，则此阈值用于根据最大距离确定额外匹配的bbox，默认值为0.5

#### 实现方式

TensorFlow：该API用于获得与最小距离的匹配。

PaddlePaddle：该API用于获得与最大距离的匹配。

#### 返回值

TensorFlow：

- **row_to_col_match_indices**：长度为num_rows的向量，它是输入`distance_matrix`的行数。如果`row_to_col_match_indices[i]` 不是-1，则行`i`与列`row_to_col_match_indices[i]`匹配。
- **col_to_row_match_indices**：长度为num_columns的向量，它是输入`distance_matrix`的列数。如果`col_to_row_match_indices[j]`不是-1，则列`j`与行`col_to_row_match_indices[j]`匹配 。

PaddlePaddle：

返回一个包含两个元素的元组。第一个是匹配的索引（matched_indices），第二个是匹配的距离。

- **matched_indices** 是一个2-D Tensor，int类型的形状为`[N，M]`。` N`是批量大小。如果`match_indices[i][j]`为-1，则表示`B[j]`与第`i`个实例中的任何实体都不匹配。否则，这意味着在第`i`个实例中`B[j]`与行`match_indices[i][j]`匹配。第`i`个实例的行号保存在`match_indices[i][j]`中。

- **matched_distance** 是一个2-D Tensor，浮点型的形状为`[N，M]`。 `N`是批量大小。如果`match_indices[i][j]`为-1，则`match_distance[i][j]`也为-1.0。否则，假设`match_distance[i][j]=d`，并且每个实例的行偏移称为LoD。然后`match_distance[i][j]=dist_matrix[d]+ LoD[i]][j]`。

