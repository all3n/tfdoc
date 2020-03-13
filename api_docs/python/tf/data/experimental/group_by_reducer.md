page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.data.experimental.group_by_reducer


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/data/experimental/group_by_reducer">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/data/experimental/ops/grouping.py#L37-L64">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



A transformation that groups elements and performs a reduction.

### Aliases:

* <a href="/api_docs/python/tf/data/experimental/group_by_reducer"><code>tf.compat.v1.data.experimental.group_by_reducer</code></a>
* <a href="/api_docs/python/tf/data/experimental/group_by_reducer"><code>tf.compat.v2.data.experimental.group_by_reducer</code></a>


``` python
tf.data.experimental.group_by_reducer(
    key_func,
    reducer
)
```



<!-- Placeholder for "Used in" -->

This transformation maps element of a dataset to a key using `key_func` and
groups the elements by key. The `reducer` is used to process each group; its
`init_func` is used to initialize state for each group when it is created, the
`reduce_func` is used to update the state every time an element is mapped to
the matching group, and the `finalize_func` is used to map the final state to
an output value.

#### Args:


* <b>`key_func`</b>: A function mapping a nested structure of tensors
  (having shapes and types defined by `self.output_shapes` and
  `self.output_types`) to a scalar <a href="../../../tf#int64"><code>tf.int64</code></a> tensor.
* <b>`reducer`</b>: An instance of `Reducer`, which captures the reduction logic using
  the `init_func`, `reduce_func`, and `finalize_func` functions.


#### Returns:

A `Dataset` transformation function, which can be passed to
<a href="../../../tf/data/Dataset#apply"><code>tf.data.Dataset.apply</code></a>.