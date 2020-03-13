page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.losses.BinaryCrossentropy


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/keras/losses/BinaryCrossentropy">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L343-L401">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `BinaryCrossentropy`

Computes the cross-entropy loss between true labels and predicted labels.



### Aliases:

* Class <a href="/api_docs/python/tf/keras/losses/BinaryCrossentropy"><code>tf.compat.v1.keras.losses.BinaryCrossentropy</code></a>
* Class <a href="/api_docs/python/tf/keras/losses/BinaryCrossentropy"><code>tf.compat.v2.keras.losses.BinaryCrossentropy</code></a>
* Class <a href="/api_docs/python/tf/keras/losses/BinaryCrossentropy"><code>tf.compat.v2.losses.BinaryCrossentropy</code></a>


<!-- Placeholder for "Used in" -->

Use this cross-entropy loss when there are only two label classes (assumed to
be 0 and 1). For each example, there should be a single floating-point value
per prediction.

In the snippet below, each of the four examples has only a single
floating-pointing value, and both `y_pred` and `y_true` have the shape
`[batch_size]`.

#### Usage:



```python
bce = tf.keras.losses.BinaryCrossentropy()
loss = bce([0., 0., 1., 1.], [1., 1., 1., 0.])
print('Loss: ', loss.numpy())  # Loss: 11.522857
```

Usage with the <a href="../../../tf/keras"><code>tf.keras</code></a> API:

```python
model = tf.keras.Model(inputs, outputs)
model.compile('sgd', loss=tf.keras.losses.BinaryCrossentropy())
```

#### Args:


* <b>`from_logits`</b>: Whether to interpret `y_pred` as a tensor of
  [logit](https://en.wikipedia.org/wiki/Logit) values. By default, we assume
    that `y_pred` contains probabilities (i.e., values in [0, 1]).
  Note: Using from_logits=True may be more numerically stable.
* <b>`label_smoothing`</b>: Float in [0, 1]. When 0, no smoothing occurs. When > 0, we
  compute the loss between the predicted labels and a smoothed version of
  the true labels, where the smoothing squeezes the labels towards 0.5.
  Larger values of `label_smoothing` correspond to heavier smoothing.
* <b>`reduction`</b>: (Optional) Type of `tf.keras.losses.Reduction` to apply to loss.
  Default value is `AUTO`. `AUTO` indicates that the reduction option will
  be determined by the usage context. For almost all cases this defaults to
  `SUM_OVER_BATCH_SIZE`.
  When used with <a href="../../../tf/distribute/Strategy"><code>tf.distribute.Strategy</code></a>, outside of built-in training
  loops such as <a href="../../../tf/keras"><code>tf.keras</code></a> `compile` and `fit`, using `AUTO` or
  `SUM_OVER_BATCH_SIZE` will raise an error. Please see
  https://www.tensorflow.org/alpha/tutorials/distribute/training_loops
  for more details on this.
* <b>`name`</b>: (Optional) Name for the op.

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/losses.py#L390-L401">View source</a>

``` python
__init__(
    from_logits=False,
    label_smoothing=0,
    reduction=losses_utils.ReductionV2.AUTO,
    name='binary_crossentropy'
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
