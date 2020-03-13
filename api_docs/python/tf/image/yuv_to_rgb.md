page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.image.yuv_to_rgb


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/image/yuv_to_rgb">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/image_ops_impl.py#L2937-L2957">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Converts one or more images from YUV to RGB.

### Aliases:

* <a href="/api_docs/python/tf/image/yuv_to_rgb"><code>tf.compat.v1.image.yuv_to_rgb</code></a>
* <a href="/api_docs/python/tf/image/yuv_to_rgb"><code>tf.compat.v2.image.yuv_to_rgb</code></a>


``` python
tf.image.yuv_to_rgb(images)
```



<!-- Placeholder for "Used in" -->

Outputs a tensor of the same shape as the `images` tensor, containing the RGB
value of the pixels.
The output is only well defined if the Y value in images are in [0,1],
U and V value are in [-0.5,0.5].

#### Args:


* <b>`images`</b>: 2-D or higher rank. Image data to convert. Last dimension must be
  size 3.


#### Returns:


* <b>`images`</b>: tensor with the same shape as `images`.
