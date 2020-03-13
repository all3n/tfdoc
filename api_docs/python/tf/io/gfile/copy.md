page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.io.gfile.copy


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/io/gfile/copy">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/lib/io/file_io.py#L472-L486">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Copies data from `src` to `dst`.

### Aliases:

* <a href="/api_docs/python/tf/io/gfile/copy"><code>tf.compat.v1.io.gfile.copy</code></a>
* <a href="/api_docs/python/tf/io/gfile/copy"><code>tf.compat.v2.io.gfile.copy</code></a>


``` python
tf.io.gfile.copy(
    src,
    dst,
    overwrite=False
)
```



<!-- Placeholder for "Used in" -->


#### Args:


* <b>`src`</b>: string, name of the file whose contents need to be copied
* <b>`dst`</b>: string, name of the file to which to copy to
* <b>`overwrite`</b>: boolean, if false it's an error for `dst` to be occupied by an
  existing file.


#### Raises:


* <b><a href="/api_docs/python/tf/errors/OpError"><code>errors.OpError</code></a></b>: If the operation fails.
