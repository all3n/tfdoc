page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>
<script src="/_static/js/managed/mathjax/MathJax.js?config=TeX-AMS-MML_SVG"></script>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.io.decode_gif


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/io/decode_gif">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>
</table>

Defined in generated file: `python/ops/gen_image_ops.py`



Decode the frame(s) of a GIF-encoded image to a uint8 tensor.

### Aliases:

* <a href="/api_docs/python/tf/io/decode_gif"><code>tf.compat.v1.image.decode_gif</code></a>
* <a href="/api_docs/python/tf/io/decode_gif"><code>tf.compat.v1.io.decode_gif</code></a>
* <a href="/api_docs/python/tf/io/decode_gif"><code>tf.compat.v2.image.decode_gif</code></a>
* <a href="/api_docs/python/tf/io/decode_gif"><code>tf.compat.v2.io.decode_gif</code></a>
* <a href="/api_docs/python/tf/io/decode_gif"><code>tf.image.decode_gif</code></a>


``` python
tf.io.decode_gif(
    contents,
    name=None
)
```



<!-- Placeholder for "Used in" -->

GIF images with frame or transparency compression are not supported.
On Linux and MacOS systems, convert animated GIFs from compressed to
uncompressed by running:

    convert $src.gif -coalesce $dst.gif

This op also supports decoding JPEGs and PNGs, though it is cleaner to use
<a href="../../tf/io/decode_image"><code>tf.image.decode_image</code></a>.

#### Args:


* <b>`contents`</b>: A `Tensor` of type `string`. 0-D.  The GIF-encoded image.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

A `Tensor` of type `uint8`.
