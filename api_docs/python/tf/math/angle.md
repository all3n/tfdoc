page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>
<script src="/_static/js/managed/mathjax/MathJax.js?config=TeX-AMS-MML_SVG"></script>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.math.angle


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/math/angle">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/math_ops.py#L575-L612">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Returns the element-wise argument of a complex (or real) tensor.

### Aliases:

* <a href="/api_docs/python/tf/math/angle"><code>tf.angle</code></a>
* <a href="/api_docs/python/tf/math/angle"><code>tf.compat.v1.angle</code></a>
* <a href="/api_docs/python/tf/math/angle"><code>tf.compat.v1.math.angle</code></a>
* <a href="/api_docs/python/tf/math/angle"><code>tf.compat.v2.math.angle</code></a>


``` python
tf.math.angle(
    input,
    name=None
)
```



<!-- Placeholder for "Used in" -->

Given a tensor `input`, this operation returns a tensor of type `float` that
is the argument of each element in `input` considered as a complex number.

The elements in `input` are considered to be complex numbers of the form
\\(a + bj\\), where *a* is the real part and *b* is the imaginary part.
If `input` is real then *b* is zero by definition.

The argument returned by this function is of the form \\(atan2(b, a)\\).
If `input` is real, a tensor of all zeros is returned.

#### For example:



```
input = tf.constant([-2.25 + 4.75j, 3.25 + 5.75j], dtype=tf.complex64)
tf.math.angle(input).numpy()
# ==> array([2.0131705, 1.056345 ], dtype=float32)
```

#### Args:


* <b>`input`</b>: A `Tensor`. Must be one of the following types: `float`, `double`,
  `complex64`, `complex128`.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor` of type `float32` or `float64`.
