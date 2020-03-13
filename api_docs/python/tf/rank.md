page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.rank


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/rank">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/array_ops.py#L575-L606">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Returns the rank of a tensor.

### Aliases:

* <a href="/api_docs/python/tf/rank"><code>tf.compat.v1.rank</code></a>
* <a href="/api_docs/python/tf/rank"><code>tf.compat.v2.rank</code></a>


``` python
tf.rank(
    input,
    name=None
)
```



<!-- Placeholder for "Used in" -->

Returns a 0-D `int32` `Tensor` representing the rank of `input`.

#### For example:



```python
# shape of tensor 't' is [2, 2, 3]
t = tf.constant([[[1, 1, 1], [2, 2, 2]], [[3, 3, 3], [4, 4, 4]]])
tf.rank(t)  # 3
```

**Note**: The rank of a tensor is not the same as the rank of a matrix. The
rank of a tensor is the number of indices required to uniquely select each
element of the tensor. Rank is also known as "order", "degree", or "ndims."

#### Args:


* <b>`input`</b>: A `Tensor` or `SparseTensor`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor` of type `int32`.




#### Numpy Compatibility
Equivalent to np.ndim
