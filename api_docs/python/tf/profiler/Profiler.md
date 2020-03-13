page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.profiler.Profiler


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L126-L306">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `Profiler`

TensorFlow multi-step profiler.



### Aliases:

* Class <a href="/api_docs/python/tf/profiler/Profiler"><code>tf.compat.v1.profiler.Profiler</code></a>


<!-- Placeholder for "Used in" -->

https://github.com/tensorflow/tensorflow/tree/master/tensorflow/core/profiler/README.md

```python
Typical use case:
  # Currently we are only allowed to create 1 profiler per process.
  profiler = Profiler(sess.graph)

  for i in xrange(total_steps):
    if i % 10000 == 0:
      run_meta = tf.compat.v1.RunMetadata()
      _ = sess.run(...,
                   options=tf.compat.v1.RunOptions(
                       trace_level=tf.RunOptions.FULL_TRACE),
                   run_metadata=run_meta)
      profiler.add_step(i, run_meta)

      # Profile the parameters of your model.
      profiler.profile_name_scope(options=(option_builder.ProfileOptionBuilder
          .trainable_variables_parameter()))

      # Or profile the timing of your model operations.
      opts = option_builder.ProfileOptionBuilder.time_and_memory()
      profiler.profile_operations(options=opts)

      # Or you can generate a timeline:
      opts = (option_builder.ProfileOptionBuilder(
              option_builder.ProfileOptionBuilder.time_and_memory())
              .with_step(i)
              .with_timeline_output(filename).build())
      profiler.profile_graph(options=opts)
    else:
      _ = sess.run(...)
  # Auto detect problems and generate advice.
  profiler.advise()
```

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L166-L184">View source</a>

``` python
__init__(
    graph=None,
    op_log=None
)
```

Constructor.


#### Args:


* <b>`graph`</b>: tf.Graph. If None and eager execution is not enabled, use
    default graph.
* <b>`op_log`</b>: optional. tensorflow::tfprof::OpLogProto proto. Used to define
    extra op types.



## Methods

<h3 id="add_step"><code>add_step</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L189-L205">View source</a>

``` python
add_step(
    step,
    run_meta
)
```

Add statistics of a step.


#### Args:


* <b>`step`</b>: int, An id used to group one or more different `run_meta` together.
    When profiling with the profile_xxx APIs, user can use the `step`
    id in the `options` to profile these `run_meta` together.
* <b>`run_meta`</b>: RunMetadata proto that contains statistics of a session run.

<h3 id="advise"><code>advise</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L279-L291">View source</a>

``` python
advise(options)
```

Automatically detect problems and generate reports.


#### Args:


* <b>`options`</b>: A dict of options. See ALL_ADVICE example above.

#### Returns:

A Advise proto that conains the reports from all checkers.


<h3 id="profile_graph"><code>profile_graph</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L262-L277">View source</a>

``` python
profile_graph(options)
```

Profile the statistics of graph nodes, organized by dataflow graph.


#### Args:


* <b>`options`</b>: A dict of options. See core/profiler/g3doc/options.md.

#### Returns:

a GraphNodeProto that records the results.


<h3 id="profile_name_scope"><code>profile_name_scope</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L245-L260">View source</a>

``` python
profile_name_scope(options)
```

Profile the statistics of graph nodes, organized by name scope.


#### Args:


* <b>`options`</b>: A dict of options. See core/profiler/g3doc/options.md.

#### Returns:

a GraphNodeProto that records the results.


<h3 id="profile_operations"><code>profile_operations</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L228-L243">View source</a>

``` python
profile_operations(options)
```

Profile the statistics of the Operation types (e.g. MatMul, Conv2D).


#### Args:


* <b>`options`</b>: A dict of options. See core/profiler/g3doc/options.md.

#### Returns:

a MultiGraphNodeProto that records the results.


<h3 id="profile_python"><code>profile_python</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L207-L226">View source</a>

``` python
profile_python(options)
```

Profile the statistics of the Python codes.

  By default, it shows the call stack from root. To avoid
  redundant output, you may use options to filter as below
    options['show_name_regexes'] = ['.*my_code.py.*']

#### Args:


* <b>`options`</b>: A dict of options. See core/profiler/g3doc/options.md.

#### Returns:

a MultiGraphNodeProto that records the results.


<h3 id="serialize_to_string"><code>serialize_to_string</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/profiler/model_analyzer.py#L293-L302">View source</a>

``` python
serialize_to_string()
```

Serialize the ProfileProto to a binary string.

  Users can write it to file for offline analysis by tfprof commandline
  or graphical interface.

#### Returns:

ProfileProto binary string.
