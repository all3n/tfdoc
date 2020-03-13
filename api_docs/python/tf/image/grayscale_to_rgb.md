page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.image.grayscale_to_rgb


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/image/grayscale_to_rgb">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/image_ops_impl.py#L1851-L1876">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Converts one or more images from Grayscale to RGB.

### Aliases:

* <a href="/api_docs/python/tf/image/grayscale_to_rgb"><code>tf.compat.v1.image.grayscale_to_rgb</code></a>
* <a href="/api_docs/python/tf/image/grayscale_to_rgb"><code>tf.compat.v2.image.grayscale_to_rgb</code></a>


``` python
tf.image.grayscale_to_rgb(
    images,
    name=None
)
```



<!-- Placeholder for "Used in" -->

Outputs a tensor of the same `DType` and rank as `images`.  The size of the
last dimension of the output is 3, containing the RGB value of the pixels.
The input images' last dimension must be size 1.

#### Args:


* <b>`images`</b>: The Grayscale tensor to convert. Last dimension must be size 1.
* <b>`name`</b>: A name for the operation (optional).


#### Returns:

The converted grayscale image(s).
