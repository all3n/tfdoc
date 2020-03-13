<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.contrib.summary.SummaryWriter" />
<meta itemprop="path" content="Stable" />
<meta itemprop="property" content="__init__"/>
<meta itemprop="property" content="as_default"/>
<meta itemprop="property" content="close"/>
<meta itemprop="property" content="flush"/>
<meta itemprop="property" content="init"/>
<meta itemprop="property" content="set_as_default"/>
</div>

# tf.contrib.summary.SummaryWriter

## Class `SummaryWriter`



Encapsulates a stateful summary writer resource.

See also:
- `tf.summary.create_file_writer`
- `tf.summary.create_db_writer`

<h2 id="__init__"><code>__init__</code></h2>

``` python
__init__(
    resource,
    init_op_fn
)
```

Initialize self.  See help(type(self)) for accurate signature.



## Methods

<h3 id="as_default"><code>as_default</code></h3>

``` python
as_default()
```

Enables summary writing within a `with` block.

<h3 id="close"><code>close</code></h3>

``` python
close()
```

Operation to flush and close the summary writer resource.

<h3 id="flush"><code>flush</code></h3>

``` python
flush()
```

Operation to force the summary writer to flush any buffered data.

<h3 id="init"><code>init</code></h3>

``` python
init()
```

Operation to initialize the summary writer resource.

<h3 id="set_as_default"><code>set_as_default</code></h3>

``` python
set_as_default()
```

Enables this summary writer for the current thread.



