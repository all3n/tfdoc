page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.metrics.mean_tensor


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/metrics_impl.py#L1326-L1408">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Computes the element-wise (weighted) mean of the given tensors.

### Aliases:

* <a href="/api_docs/python/tf/metrics/mean_tensor"><code>tf.compat.v1.metrics.mean_tensor</code></a>


``` python
tf.metrics.mean_tensor(
    values,
    weights=None,
    metrics_collections=None,
    updates_collections=None,
    name=None
)
```



<!-- Placeholder for "Used in" -->

In contrast to the `mean` function which returns a scalar with the
mean,  this function returns an average tensor with the same shape as the
input tensors.

The `mean_tensor` function creates two local variables,
`total_tensor` and `count_tensor` that are used to compute the average of
`values`. This average is ultimately returned as `mean` which is an idempotent
operation that simply divides `total` by `count`.

For estimation of the metric over a stream of data, the function creates an
`update_op` operation that updates these variables and returns the `mean`.
`update_op` increments `total` with the reduced sum of the product of `values`
and `weights`, and it increments `count` with the reduced sum of `weights`.

If `weights` is `None`, weights default to 1. Use weights of 0 to mask values.

#### Args:


* <b>`values`</b>: A `Tensor` of arbitrary dimensions.
* <b>`weights`</b>: Optional `Tensor` whose rank is either 0, or the same rank as
  `values`, and must be broadcastable to `values` (i.e., all dimensions must
  be either `1`, or the same as the corresponding `values` dimension).
* <b>`metrics_collections`</b>: An optional list of collections that `mean`
  should be added to.
* <b>`updates_collections`</b>: An optional list of collections that `update_op`
  should be added to.
* <b>`name`</b>: An optional variable_scope name.


#### Returns:


* <b>`mean`</b>: A float `Tensor` representing the current mean, the value of `total`
  divided by `count`.
* <b>`update_op`</b>: An operation that increments the `total` and `count` variables
  appropriately and whose value matches `mean_value`.


#### Raises:


* <b>`ValueError`</b>: If `weights` is not `None` and its shape doesn't match `values`,
  or if either `metrics_collections` or `updates_collections` are not a list
  or tuple.
* <b>`RuntimeError`</b>: If eager execution is enabled.
