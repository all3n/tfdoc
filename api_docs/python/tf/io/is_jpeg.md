page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.io.is_jpeg


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/io/is_jpeg">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/image_ops_impl.py#L2129-L2146">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Convenience function to check if the 'contents' encodes a JPEG image.

### Aliases:

* <a href="/api_docs/python/tf/io/is_jpeg"><code>tf.compat.v1.image.is_jpeg</code></a>
* <a href="/api_docs/python/tf/io/is_jpeg"><code>tf.compat.v1.io.is_jpeg</code></a>
* <a href="/api_docs/python/tf/io/is_jpeg"><code>tf.compat.v2.image.is_jpeg</code></a>
* <a href="/api_docs/python/tf/io/is_jpeg"><code>tf.compat.v2.io.is_jpeg</code></a>
* <a href="/api_docs/python/tf/io/is_jpeg"><code>tf.image.is_jpeg</code></a>


``` python
tf.io.is_jpeg(
    contents,
    name=None
)
```



<!-- Placeholder for "Used in" -->


#### Args:


* <b>`contents`</b>: 0-D `string`. The encoded image bytes.
* <b>`name`</b>: A name for the operation (optional)


#### Returns:

A scalar boolean tensor indicating if 'contents' may be a JPEG image.
is_jpeg is susceptible to false positives.
