<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.contrib.gan.losses.stargan_generator_loss_wrapper" />
<meta itemprop="path" content="Stable" />
</div>

# tf.contrib.gan.losses.stargan_generator_loss_wrapper

``` python
tf.contrib.gan.losses.stargan_generator_loss_wrapper(loss_fn)
```

Convert a generator loss function to take a StarGANModel.

The new function has the same name as the original one.

#### Args:

* <b>`loss_fn`</b>: A python function taking Discriminator's real/fake prediction for
    generated data.


#### Returns:

A new function that takes a StarGANModel namedtuple and returns the same
loss.