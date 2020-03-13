page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.distribute.in_cross_replica_context


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/distribute/in_cross_replica_context">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/distribute/distribution_strategy_context.py#L154-L176">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Returns `True` if in a cross-replica context.

### Aliases:

* <a href="/api_docs/python/tf/distribute/in_cross_replica_context"><code>tf.compat.v1.distribute.in_cross_replica_context</code></a>
* <a href="/api_docs/python/tf/distribute/in_cross_replica_context"><code>tf.compat.v2.distribute.in_cross_replica_context</code></a>
* <a href="/api_docs/python/tf/distribute/in_cross_replica_context"><code>tf.contrib.distribute.in_cross_replica_context</code></a>


``` python
tf.distribute.in_cross_replica_context()
```



<!-- Placeholder for "Used in" -->

See <a href="../../tf/distribute/get_replica_context"><code>tf.distribute.get_replica_context</code></a> for details.

```
assert not tf.distribute.in_cross_replica_context()
with strategy.scope():
  assert tf.distribute.in_cross_replica_context()

  def f():
    assert not tf.distribute.in_cross_replica_context()

  strategy.experimental_run_v2(f)
```

#### Returns:

`True` if in a cross-replica context (`get_replica_context()` returns
`None`), or `False` if in a replica context (`get_replica_context()` returns
non-`None`).
