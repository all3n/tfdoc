page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.train.SessionRunContext


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/training/session_run_hook.py#L215-L263">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `SessionRunContext`

Provides information about the `session.run()` call being made.



### Aliases:

* Class <a href="/api_docs/python/tf/train/SessionRunContext"><code>tf.compat.v1.estimator.SessionRunContext</code></a>
* Class <a href="/api_docs/python/tf/train/SessionRunContext"><code>tf.compat.v1.train.SessionRunContext</code></a>
* Class <a href="/api_docs/python/tf/train/SessionRunContext"><code>tf.compat.v2.estimator.SessionRunContext</code></a>
* Class <a href="/api_docs/python/tf/train/SessionRunContext"><code>tf.estimator.SessionRunContext</code></a>


<!-- Placeholder for "Used in" -->

Provides information about original request to `Session.Run()` function.
SessionRunHook objects can stop the loop by calling `request_stop()` of
`run_context`. In the future we may use this object to add more information
about run without changing the Hook API.

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/training/session_run_hook.py#L224-L228">View source</a>

``` python
__init__(
    original_args,
    session
)
```

Initializes SessionRunContext.




## Properties

<h3 id="original_args"><code>original_args</code></h3>

A `SessionRunArgs` object holding the original arguments of `run()`.

If user called <a href="../../tf/train/MonitoredSession#run"><code>MonitoredSession.run(fetches=a, feed_dict=b)</code></a>, then this
field is equal to SessionRunArgs(a, b).

#### Returns:

A `SessionRunArgs` object


<h3 id="session"><code>session</code></h3>

A TensorFlow session object which will execute the `run`.


<h3 id="stop_requested"><code>stop_requested</code></h3>

Returns whether a stop is requested or not.

If true, `MonitoredSession` stops iterations.
Returns:
  A `bool`



## Methods

<h3 id="request_stop"><code>request_stop</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/training/session_run_hook.py#L257-L263">View source</a>

``` python
request_stop()
```

Sets stop requested field.

Hooks can use this function to request stop of iterations.
`MonitoredSession` checks whether this is called or not.
