page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.initializers.ones


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/init_ops.py#L122-L137">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `ones`

Initializer that generates tensors initialized to 1.

Inherits From: [`Initializer`](../../tf/keras/initializers/Initializer)

### Aliases:

* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.compat.v1.initializers.ones</code></a>
* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.compat.v1.keras.initializers.Ones</code></a>
* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.compat.v1.keras.initializers.ones</code></a>
* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.compat.v1.ones_initializer</code></a>
* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.keras.initializers.Ones</code></a>
* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.keras.initializers.ones</code></a>
* Class <a href="/api_docs/python/tf/initializers/ones"><code>tf.ones_initializer</code></a>


<!-- Placeholder for "Used in" -->


<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/init_ops.py#L125-L129">View source</a>

``` python
__init__(dtype=tf.dtypes.float32)
```

DEPRECATED FUNCTION ARGUMENTS

Warning: SOME ARGUMENTS ARE DEPRECATED: `(dtype)`. They will be removed in a future version.
Instructions for updating:
Call initializer instance with the dtype argument instead of passing it to the constructor



## Methods

<h3 id="__call__"><code>__call__</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/init_ops.py#L131-L134">View source</a>

``` python
__call__(
    shape,
    dtype=None,
    partition_info=None
)
```

Returns a tensor object initialized as specified by the initializer.


#### Args:


* <b>`shape`</b>: Shape of the tensor.
* <b>`dtype`</b>: Optional dtype of the tensor. If not provided use the initializer
  dtype.
* <b>`partition_info`</b>: Optional information about the possible partitioning of a
  tensor.

<h3 id="from_config"><code>from_config</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/init_ops.py#L78-L97">View source</a>

``` python
from_config(
    cls,
    config
)
```

Instantiates an initializer from a configuration dictionary.


#### Example:



```python
initializer = RandomUniform(-1, 1)
config = initializer.get_config()
initializer = RandomUniform.from_config(config)
```

#### Args:


* <b>`config`</b>: A Python dictionary. It will typically be the output of
  `get_config`.


#### Returns:

An Initializer instance.


<h3 id="get_config"><code>get_config</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/init_ops.py#L136-L137">View source</a>

``` python
get_config()
```

Returns the configuration of the initializer as a JSON-serializable dict.


#### Returns:

A JSON-serializable Python dict.
