<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.data.experimental.NestedStructure" />
<meta itemprop="path" content="Stable" />
<meta itemprop="property" content="__init__"/>
<meta itemprop="property" content="from_value"/>
<meta itemprop="property" content="is_compatible_with"/>
</div>

# tf.data.experimental.NestedStructure

## Class `NestedStructure`

Inherits From: [`Structure`](../../../tf/data/experimental/Structure.md)

Represents a nested structure in which each leaf is a `Structure`.

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(nested_structure)
```

Initialize self.  See help(type(self)) for accurate signature.



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


