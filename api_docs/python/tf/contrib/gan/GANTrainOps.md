<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.contrib.gan.GANTrainOps" />
<meta itemprop="path" content="Stable" />
<meta itemprop="property" content="generator_train_op"/>
<meta itemprop="property" content="discriminator_train_op"/>
<meta itemprop="property" content="global_step_inc_op"/>
<meta itemprop="property" content="train_hooks"/>
<meta itemprop="property" content="__new__"/>
</div>

# tf.contrib.gan.GANTrainOps

## Class `GANTrainOps`



GANTrainOps contains the training ops.

#### Args:

* <b>`generator_train_op`</b>: Op that performs a generator update step.
* <b>`discriminator_train_op`</b>: Op that performs a discriminator update step.
* <b>`global_step_inc_op`</b>: Op that increments the shared global step.
* <b>`train_hooks`</b>: a list or tuple containing hooks related to training that need
    to be populated when training ops are instantiated. Used primarily for
    sync hooks.

<h2 id="__new__"><code>__new__</code></h2>

``` python
@staticmethod
__new__(
    cls,
    generator_train_op,
    discriminator_train_op,
    global_step_inc_op,
    train_hooks=()
)
```

Create new instance of GANTrainOps(generator_train_op, discriminator_train_op, global_step_inc_op, train_hooks)



## Properties

<h3 id="generator_train_op"><code>generator_train_op</code></h3>



<h3 id="discriminator_train_op"><code>discriminator_train_op</code></h3>



<h3 id="global_step_inc_op"><code>global_step_inc_op</code></h3>



<h3 id="train_hooks"><code>train_hooks</code></h3>





