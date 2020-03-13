page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.cosh


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/math/cosh">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>
</table>

Defined in generated file: `python/ops/gen_math_ops.py`



Computes hyperbolic cosine of x element-wise.

### Aliases:

* <a href="/api_docs/python/tf/math/cosh"><code>tf.compat.v1.cosh</code></a>
* <a href="/api_docs/python/tf/math/cosh"><code>tf.compat.v1.math.cosh</code></a>
* <a href="/api_docs/python/tf/math/cosh"><code>tf.compat.v2.cosh</code></a>
* <a href="/api_docs/python/tf/math/cosh"><code>tf.compat.v2.math.cosh</code></a>
* <a href="/api_docs/python/tf/math/cosh"><code>tf.cosh</code></a>


``` python
tf.math.cosh(
    x,
    name=None
)
```



<!-- Placeholder for "Used in" -->

  Given an input tensor, this function computes hyperbolic cosine of every
  element in the tensor. Input range is `[-inf, inf]` and output range
  is `[1, inf]`.

>     x = tf.constant([-float("inf"), -9, -0.5, 1, 1.2, 2, 10, float("inf")])
>     tf.math.cosh(x) ==> [inf 4.0515420e+03 1.1276259e+00 1.5430807e+00 1.8106556e+00 3.7621956e+00 1.1013233e+04 inf]

#### Args:


* <b>`x`</b>: A `Tensor`. Must be one of the following types: `bfloat16`, `half`, `float32`, `float64`, `complex64`, `complex128`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `x`.
