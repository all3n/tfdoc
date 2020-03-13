page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.summary.import_event


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/summary_ops_v2.py#L888-L904">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Writes a <a href="../../../tf/Event"><code>tf.compat.v1.Event</code></a> binary proto.

``` python
tf.contrib.summary.import_event(
    tensor,
    name=None
)
```



<!-- Placeholder for "Used in" -->

This can be used to import existing event logs into a new summary writer sink.
Please note that this is lower level than the other summary functions and
will ignore the `tf.summary.should_record_summaries` setting.

#### Args:


* <b>`tensor`</b>: A <a href="../../../tf/Tensor"><code>tf.Tensor</code></a> of type `string` containing a serialized
  <a href="../../../tf/Event"><code>tf.compat.v1.Event</code></a> proto.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

The created <a href="../../../tf/Operation"><code>tf.Operation</code></a>.
