page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.accumulate_n


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/math/accumulate_n">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/math_ops.py#L3010-L3091">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Returns the element-wise sum of a list of tensors.

### Aliases:

* <a href="/api_docs/python/tf/math/accumulate_n"><code>tf.accumulate_n</code></a>
* <a href="/api_docs/python/tf/math/accumulate_n"><code>tf.compat.v1.accumulate_n</code></a>
* <a href="/api_docs/python/tf/math/accumulate_n"><code>tf.compat.v1.math.accumulate_n</code></a>
* <a href="/api_docs/python/tf/math/accumulate_n"><code>tf.compat.v2.math.accumulate_n</code></a>


``` python
tf.math.accumulate_n(
    inputs,
    shape=None,
    tensor_dtype=None,
    name=None
)
```



<!-- Placeholder for "Used in" -->

Optionally, pass `shape` and `tensor_dtype` for shape and type checking,
otherwise, these are inferred.

`accumulate_n` performs the same operation as <a href="../../tf/math/add_n"><code>tf.math.add_n</code></a>, but
does not wait for all of its inputs to be ready before beginning to sum.
This approach can save memory if inputs are ready at different times, since
minimum temporary storage is proportional to the output size rather than the
inputs' size.

`accumulate_n` is differentiable (but wasn't previous to TensorFlow 1.7).

#### For example:



```python
a = tf.constant([[1, 2], [3, 4]])
b = tf.constant([[5, 0], [0, 6]])
tf.math.accumulate_n([a, b, a])  # [[7, 4], [6, 14]]

# Explicitly pass shape and type
tf.math.accumulate_n([a, b, a], shape=[2, 2], tensor_dtype=tf.int32)
                                                               # [[7,  4],
                                                               #  [6, 14]]
```

#### Args:


* <b>`inputs`</b>: A list of `Tensor` objects, each with same shape and type.
* <b>`shape`</b>: Expected shape of elements of `inputs` (optional). Also controls the
  output shape of this op, which may affect type inference in other ops. A
  value of `None` means "infer the input shape from the shapes in `inputs`".
* <b>`tensor_dtype`</b>: Expected data type of `inputs` (optional). A value of `None`
  means "infer the input dtype from `inputs[0]`".
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor` of same shape and type as the elements of `inputs`.



#### Raises:


* <b>`ValueError`</b>: If `inputs` don't all have same shape and dtype or the shape
cannot be inferred.
