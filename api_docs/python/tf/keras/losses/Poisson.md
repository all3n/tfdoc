page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.losses.Poisson


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/keras/losses/Poisson">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L624-L646">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `Poisson`

Computes the Poisson loss between `y_true` and `y_pred`.



### Aliases:

* Class <a href="/api_docs/python/tf/keras/losses/Poisson"><code>tf.compat.v1.keras.losses.Poisson</code></a>
* Class <a href="/api_docs/python/tf/keras/losses/Poisson"><code>tf.compat.v2.keras.losses.Poisson</code></a>
* Class <a href="/api_docs/python/tf/keras/losses/Poisson"><code>tf.compat.v2.losses.Poisson</code></a>


<!-- Placeholder for "Used in" -->

`loss = y_pred - y_true * log(y_pred)`

#### Usage:



```python
p = tf.keras.losses.Poisson()
loss = p([1., 9., 2.], [4., 8., 12.])
print('Loss: ', loss.numpy())  # Loss: -0.35702705
```

Usage with the `compile` API:

```python
model = tf.keras.Model(inputs, outputs)
model.compile('sgd', loss=tf.keras.losses.Poisson())
```

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L645-L646">View source</a>

``` python
__init__(
    reduction=losses_utils.ReductionV2.AUTO,
    name='poisson'
)
```

Initialize self.  See help(type(self)) for accurate signature.




## Methods

<h3 id="__call__"><code>__call__</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L94-L126">View source</a>

``` python
__call__(
    y_true,
    y_pred,
    sample_weight=None
)
```

Invokes the `Loss` instance.


#### Args:


* <b>`y_true`</b>: Ground truth values. shape = `[batch_size, d0, .. dN]`
* <b>`y_pred`</b>: The predicted values. shape = `[batch_size, d0, .. dN]`
* <b>`sample_weight`</b>: Optional `sample_weight` acts as a
  coefficient for the loss. If a scalar is provided, then the loss is
  simply scaled by the given value. If `sample_weight` is a tensor of size
  `[batch_size]`, then the total loss for each sample of the batch is
  rescaled by the corresponding element in the `sample_weight` vector. If
  the shape of `sample_weight` is `[batch_size, d0, .. dN-1]` (or can be
  broadcasted to this shape), then each loss element of `y_pred` is scaled
  by the corresponding value of `sample_weight`. (Note on`dN-1`: all loss
  functions reduce by 1 dimension, usually axis=-1.)


#### Returns:

Weighted loss float `Tensor`. If `reduction` is `NONE`, this has
  shape `[batch_size, d0, .. dN-1]`; otherwise, it is scalar. (Note `dN-1`
  because all loss functions reduce by 1 dimension, usually axis=-1.)



#### Raises:


* <b>`ValueError`</b>: If the shape of `sample_weight` is invalid.

<h3 id="from_config"><code>from_config</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L128-L138">View source</a>

``` python
from_config(
    cls,
    config
)
```

Instantiates a `Loss` from its config (output of `get_config()`).


#### Args:


* <b>`config`</b>: Output of `get_config()`.


#### Returns:

A `Loss` instance.


<h3 id="get_config"><code>get_config</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L218-L223">View source</a>

``` python
get_config()
```
