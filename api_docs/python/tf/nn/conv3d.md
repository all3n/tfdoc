page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.nn.conv3d


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/nn/conv3d">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/nn_ops.py#L2449-L2461">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Computes a 3-D convolution given 5-D `input` and `filter` tensors.

### Aliases:

* <a href="/api_docs/python/tf/nn/conv3d"><code>tf.compat.v1.nn.conv3d</code></a>


``` python
tf.nn.conv3d(
    input,
    filter=None,
    strides=None,
    padding=None,
    data_format='NDHWC',
    dilations=[1, 1, 1, 1, 1],
    name=None,
    filters=None
)
```



<!-- Placeholder for "Used in" -->

In signal processing, cross-correlation is a measure of similarity of
two waveforms as a function of a time-lag applied to one of them. This
is also known as a sliding dot product or sliding inner-product.

Our Conv3D implements a form of cross-correlation.

#### Args:


* <b>`input`</b>: A `Tensor`. Must be one of the following types: `half`, `bfloat16`, `float32`, `float64`.
  Shape `[batch, in_depth, in_height, in_width, in_channels]`.
* <b>`filter`</b>: A `Tensor`. Must have the same type as `input`.
  Shape `[filter_depth, filter_height, filter_width, in_channels,
  out_channels]`. `in_channels` must match between `input` and `filter`.
* <b>`strides`</b>: A list of `ints` that has length `>= 5`.
  1-D tensor of length 5. The stride of the sliding window for each
  dimension of `input`. Must have `strides[0] = strides[4] = 1`.
* <b>`padding`</b>: A `string` from: `"SAME", "VALID"`.
  The type of padding algorithm to use.
* <b>`data_format`</b>: An optional `string` from: `"NDHWC", "NCDHW"`. Defaults to `"NDHWC"`.
  The data format of the input and output data. With the
  default format "NDHWC", the data is stored in the order of:
      [batch, in_depth, in_height, in_width, in_channels].
  Alternatively, the format could be "NCDHW", the data storage order is:
      [batch, in_channels, in_depth, in_height, in_width].
* <b>`dilations`</b>: An optional list of `ints`. Defaults to `[1, 1, 1, 1, 1]`.
  1-D tensor of length 5.  The dilation factor for each dimension of
  `input`. If set to k > 1, there will be k-1 skipped cells between each
  filter element on that dimension. The dimension order is determined by the
  value of `data_format`, see above for details. Dilations in the batch and
  depth dimensions must be 1.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor`. Has the same type as `input`.