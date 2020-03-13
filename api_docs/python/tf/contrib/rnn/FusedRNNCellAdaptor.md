page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.rnn.FusedRNNCellAdaptor


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/rnn/python/ops/fused_rnn_cell.py#L82-L130">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `FusedRNNCellAdaptor`

This is an adaptor for RNNCell classes to be used with `FusedRNNCell`.

Inherits From: [`FusedRNNCell`](../../../tf/contrib/rnn/FusedRNNCell)

<!-- Placeholder for "Used in" -->


<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/rnn/python/ops/fused_rnn_cell.py#L85-L93">View source</a>

``` python
__init__(
    cell,
    use_dynamic_rnn=False
)
```

Initialize the adaptor.


#### Args:


* <b>`cell`</b>: an instance of a subclass of a <a href="/api_docs/python/tf/nn/rnn_cell/RNNCell"><code>rnn_cell.RNNCell</code></a>.
* <b>`use_dynamic_rnn`</b>: whether to use dynamic (or static) RNN.



## Methods

<h3 id="__call__"><code>__call__</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/rnn/python/ops/fused_rnn_cell.py#L95-L130">View source</a>

``` python
__call__(
    inputs,
    initial_state=None,
    dtype=None,
    sequence_length=None,
    scope=None
)
```

Run this fused RNN on inputs, starting from the given state.


#### Args:


* <b>`inputs`</b>: `3-D` tensor with shape `[time_len x batch_size x input_size]`
  or a list of `time_len` tensors of shape `[batch_size x input_size]`.
* <b>`initial_state`</b>: either a tensor with shape `[batch_size x state_size]`
  or a tuple with shapes `[batch_size x s] for s in state_size`, if the
  cell takes tuples. If this is not provided, the cell is expected to
  create a zero initial state of type `dtype`.
* <b>`dtype`</b>: The data type for the initial state and expected output. Required
  if `initial_state` is not provided or RNN state has a heterogeneous
    dtype.
* <b>`sequence_length`</b>: Specifies the length of each sequence in inputs. An
  `int32` or `int64` vector (tensor) size `[batch_size]`, values in `[0,
  time_len)`.
  Defaults to `time_len` for each element.
* <b>`scope`</b>: `VariableScope` or `string` for the created subgraph; defaults to
  class name.


#### Returns:

A pair containing:

- Output: A `3-D` tensor of shape `[time_len x batch_size x output_size]`
  or a list of `time_len` tensors of shape `[batch_size x output_size]`,
  to match the type of the `inputs`.
- Final state: Either a single `2-D` tensor, or a tuple of tensors
  matching the arity and shapes of `initial_state`.
