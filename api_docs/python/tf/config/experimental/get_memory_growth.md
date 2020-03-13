page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.config.experimental.get_memory_growth


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/config/experimental/get_memory_growth">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/framework/config.py#L409-L431">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Get if memory growth is enabled for a PhysicalDevice.

### Aliases:

* <a href="/api_docs/python/tf/config/experimental/get_memory_growth"><code>tf.compat.v1.config.experimental.get_memory_growth</code></a>
* <a href="/api_docs/python/tf/config/experimental/get_memory_growth"><code>tf.compat.v2.config.experimental.get_memory_growth</code></a>


``` python
tf.config.experimental.get_memory_growth(device)
```



<!-- Placeholder for "Used in" -->

A PhysicalDevice with memory growth set will not allocate all memory on the
device upfront.

#### For example:



```python
physical_devices = config.experimental.list_physical_devices('GPU')
assert len(physical_devices) > 0, "Not enough GPU hardware devices available"
tf.config.experimental.set_memory_growth(physical_devices[0], True)
assert tf.config.experimental.get_memory_growth(physical_devices[0]) == True
```

#### Args:


* <b>`device`</b>: PhysicalDevice to query


#### Returns:

Current memory growth setting.
