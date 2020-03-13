page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.keras.backend.set_image_data_format


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/keras/backend/set_image_data_format">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/keras/backend_config.py#L110-L126">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Sets the value of the image data format convention.

### Aliases:

* <a href="/api_docs/python/tf/keras/backend/set_image_data_format"><code>tf.compat.v1.keras.backend.set_image_data_format</code></a>
* <a href="/api_docs/python/tf/keras/backend/set_image_data_format"><code>tf.compat.v2.keras.backend.set_image_data_format</code></a>


``` python
tf.keras.backend.set_image_data_format(data_format)
```



<!-- Placeholder for "Used in" -->


#### Arguments:


* <b>`data_format`</b>: string. `'channels_first'` or `'channels_last'`.
Example: ```python from keras import backend as K K.image_data_format() >>>
  'channels_first' K.set_image_data_format('channels_last')
  K.image_data_format() >>> 'channels_last' ```

#### Raises:


* <b>`ValueError`</b>: In case of invalid `data_format` value.
