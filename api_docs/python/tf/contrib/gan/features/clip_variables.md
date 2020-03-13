<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.contrib.gan.features.clip_variables" />
<meta itemprop="path" content="Stable" />
</div>

# tf.contrib.gan.features.clip_variables

``` python
tf.contrib.gan.features.clip_variables(
    optimizer,
    variables,
    weight_clip
)
```

Modifies an optimizer so it clips weights to a certain value.

#### Args:

* <b>`optimizer`</b>: An optimizer to perform variable weight clipping.
* <b>`variables`</b>: A list of TensorFlow variables.
* <b>`weight_clip`</b>: Positive python float to clip discriminator weights. Used to
    enforce a K-lipschitz condition, which is useful for some GAN training
    schemes (ex WGAN: https://arxiv.org/pdf/1701.07875).


#### Returns:

An optimizer to perform weight clipping after updates.


#### Raises:

* <b>`ValueError`</b>: If `weight_clip` is less than 0.