page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.backend.all


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/keras/backend/all">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/backend.py#L2022-L2035">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Bitwise reduction (logical AND).

### Aliases:

* <a href="/api_docs/python/tf/keras/backend/all"><code>tf.compat.v1.keras.backend.all</code></a>
* <a href="/api_docs/python/tf/keras/backend/all"><code>tf.compat.v2.keras.backend.all</code></a>


``` python
tf.keras.backend.all(
    x,
    axis=None,
    keepdims=False
)
```



<!-- Placeholder for "Used in" -->


#### Arguments:


* <b>`x`</b>: Tensor or variable.
* <b>`axis`</b>: axis along which to perform the reduction.
* <b>`keepdims`</b>: whether the drop or broadcast the reduction axes.


#### Returns:

A uint8 tensor (0s and 1s).
