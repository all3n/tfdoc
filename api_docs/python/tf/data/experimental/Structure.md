<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.data.experimental.Structure" />
<meta itemprop="path" content="Stable" />
<meta itemprop="property" content="from_value"/>
<meta itemprop="property" content="is_compatible_with"/>
</div>

# tf.data.experimental.Structure

## Class `Structure`



Represents structural information, such as type and shape, about a value.

A `Structure` generalizes the <a href="../../../tf/Tensor.md#dtype"><code>tf.Tensor.dtype</code></a> and <a href="../../../tf/Tensor.md#shape"><code>tf.Tensor.shape</code></a>
properties, so that we can define generic containers of objects including:

* <a href="../../../tf/Tensor.md"><code>tf.Tensor</code></a>
* <a href="../../../tf/sparse/SparseTensor.md"><code>tf.SparseTensor</code></a>
* Nested structures of the above.

TODO(b/110122868): In the future, a single `Structure` will replace the
<a href="../../../tf/data/Dataset.md#output_types"><code>tf.data.Dataset.output_types</code></a>, <a href="../../../tf/data/Dataset.md#output_shapes"><code>tf.data.Dataset.output_shapes</code></a>,
and <a href="../../../tf/data/Dataset.md#output_classes"><code>tf.data.Dataset.output_classes</code></a>, and similar properties and arguments in
the <a href="../../../tf/data/Iterator.md"><code>tf.data.Iterator</code></a> and `Optional` classes.

## Methods

<h3 id="from_value"><code>from_value</code></h3>

``` python
@staticmethod
from_value(value)
```

Returns a `Structure` that represents the given `value`.

#### Args:

* <b>`value`</b>: A potentially structured value.


#### Returns:

A `Structure` that is compatible with `value`.


#### Raises:

* <b>`TypeError`</b>: If a structure cannot be built for `value`, because its type
    or one of its component types is not supported.

<h3 id="is_compatible_with"><code>is_compatible_with</code></h3>

``` python
is_compatible_with(other)
```

Returns `True` if `other` is compatible with this structure.

A structure `t` is a "subtype" of `s` if:

* `s` and `t` are instances of the same `Structure` subclass.
* The nested structures (if any) of `s` and `t` are the same, according to
  <a href="../../../tf/contrib/framework/nest/assert_same_structure.md"><code>tf.contrib.framework.nest.assert_same_structure</code></a>, and each nested
  structure of `t` is a "subtype" of the corresponding nested structure of
  `s`.
* Any <a href="../../../tf/dtypes/DType.md"><code>tf.DType</code></a> components of `t` are the same as the corresponding
  components in `s`.
* Any <a href="../../../tf/TensorShape.md"><code>tf.TensorShape</code></a> components of `t` are compatible with the
  corresponding components in `s`, according to
  <a href="../../../tf/TensorShape.md#is_compatible_with"><code>tf.TensorShape.is_compatible_with</code></a>.

#### Args:

* <b>`other`</b>: A `Structure`.


#### Returns:

`True` if `other` is a subtype of this structure, otherwise `False`.



