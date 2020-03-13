page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.quantize.experimental_create_eval_graph


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/quantize/python/quantize_graph.py#L208-L249">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Rewrites an eval input_graph in place for simulated quantization.

``` python
tf.contrib.quantize.experimental_create_eval_graph(
    input_graph=None,
    weight_bits=8,
    activation_bits=8,
    symmetric=False,
    quant_delay=None,
    scope=None
)
```



<!-- Placeholder for "Used in" -->

Variables added by the rewrite get added to the global variables collection.

This function has additional experimental options not (yet) available to
create_eval_graph. The resulting behavior may be undefined.

The graph has fake quantization ops inserted to simulate the error
introduced by quantization. Since the graph is transformed in place,
the expected behavior of previously held references to nodes and tensors may
change.

#### Args:


* <b>`input_graph`</b>: The tf.Graph to be transformed, if None then defaults to the
  default graph.
* <b>`weight_bits`</b>: Number of bits to use for quantizing weights.
* <b>`activation_bits`</b>: Number of bits to use for quantizing activations.
* <b>`symmetric`</b>: If true, use symmetric quantization limits instead of training
  the minimum and maximum of each quantization range separately.
* <b>`quant_delay`</b>: Number of steps after which weights and activations are
  quantized during eval.
* <b>`scope`</b>: The scope to be transformed. If it's not None, only the ops which
  are in this scope will be transformed.


#### Raises:


* <b>`ValueError`</b>: If elements contains an element that isn't a tf.Tensor or
  tf.Operation.
