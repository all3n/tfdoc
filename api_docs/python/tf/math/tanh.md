page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.tanh


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/math/tanh">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>
</table>

Defined in generated file: `python/ops/gen_math_ops.py`



Computes hyperbolic tangent of `x` element-wise.

### Aliases:

* <a href="/api_docs/python/tf/math/tanh"><code>tf.compat.v1.math.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.compat.v1.nn.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.compat.v1.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.compat.v2.math.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.compat.v2.nn.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.compat.v2.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.nn.tanh</code></a>
* <a href="/api_docs/python/tf/math/tanh"><code>tf.tanh</code></a>


``` python
tf.math.tanh(
    x,
    name=None
)
```



<!-- Placeholder for "Used in" -->

  Given an input tensor, this function computes hyperbolic tangent of every
  element in the tensor. Input range is `[-inf, inf]` and
  output range is `[-1,1]`.

>     x = tf.constant([-float("inf"), -5, -0.5, 1, 1.2, 2, 3, float("inf")])
>     tf.math.tanh(x) ==> [-1. -0.99990916 -0.46211717 0.7615942 0.8336547 0.9640276 0.9950547 1.]

#### Args:


* <b>`x`</b>: A `Tensor`. Must be one of the following types: `bfloat16`, `half`, `float32`, `float64`, `complex64`, `complex128`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `x`.

If `x` is a `SparseTensor`, returns
`SparseTensor(x.indices, tf.math.tanh(x.values, ...), x.dense_shape)`
