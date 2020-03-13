page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.framework.load_linear_multiclass_bias_initializer


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/framework/python/ops/checkpoint_ops.py#L32-L86">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Loads pre-trained multi-class biases for linear models from checkpoint.

``` python
tf.contrib.framework.load_linear_multiclass_bias_initializer(
    ckpt_path,
    bias_tensor_name,
    new_class_vocab_size,
    old_class_vocab_file,
    new_class_vocab_file,
    num_class_oov_buckets=0,
    initializer=None,
    max_rows_in_memory=-1
)
```



<!-- Placeholder for "Used in" -->

Wrapper around `load_and_remap_matrix_initializer()` specialized for loading
multi-class bias and remapping according to the provided vocab files. See docs
for `load_and_remap_matrix_initializer()` for more details. In this case, the
provided row_vocab is the class vocabulary, and the expected shape is
`[new_class_vocab_size, 1]`.

#### Args:


* <b>`ckpt_path`</b>: Path to the TensorFlow checkpoint (version 2, `TensorBundle`)
  from which the old matrix `Tensor` will be loaded.
* <b>`bias_tensor_name`</b>: Tensor name to load from in the checkpoints.
* <b>`new_class_vocab_size`</b>: Number of entries in the new class vocab.
* <b>`old_class_vocab_file`</b>: A scalar `Tensor` of type `string` containing the
  path to the old class vocabulary file.
* <b>`new_class_vocab_file`</b>: A scalar `Tensor` of type `string` containing the
  path to the new class vocabulary file.
* <b>`num_class_oov_buckets`</b>: `int` specifying the number of out-of-vocabulary
  buckets to use for the classes. Must be >= 0.
* <b>`initializer`</b>: Initializer function that accepts a 1-D tensor as the arg to
  specify the shape of the returned tensor. If `None`, defaults to using
  `zeros_initializer()`.
* <b>`max_rows_in_memory`</b>: `int` specifying the maximum number of rows to load from
  the checkpoint at once. If less than or equal to 0, the entire matrix will
  be loaded into memory. Setting this arg trades increased disk reads for
  lower memory usage.


#### Returns:

A variable initializer function.