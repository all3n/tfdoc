page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.layers.LeakyReLU


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/keras/layers/LeakyReLU">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/layers/advanced_activations.py#L33-L68">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `LeakyReLU`

Leaky version of a Rectified Linear Unit.

Inherits From: [`Layer`](../../../tf/keras/layers/Layer)

### Aliases:

* Class <a href="/api_docs/python/tf/keras/layers/LeakyReLU"><code>tf.compat.v1.keras.layers.LeakyReLU</code></a>
* Class <a href="/api_docs/python/tf/keras/layers/LeakyReLU"><code>tf.compat.v2.keras.layers.LeakyReLU</code></a>


<!-- Placeholder for "Used in" -->

It allows a small gradient when the unit is not active:
`f(x) = alpha * x for x < 0`,
`f(x) = x for x >= 0`.

#### Input shape:

Arbitrary. Use the keyword argument `input_shape`
(tuple of integers, does not include the samples axis)
when using this layer as the first layer in a model.



#### Output shape:

Same shape as the input.



#### Arguments:


* <b>`alpha`</b>: Float >= 0. Negative slope coefficient.

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/layers/advanced_activations.py#L53-L56">View source</a>

``` python
__init__(
    alpha=0.3,
    **kwargs
)
```
