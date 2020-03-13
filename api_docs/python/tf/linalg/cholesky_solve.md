page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.linalg.cholesky_solve


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/linalg/cholesky_solve">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/linalg_ops.py#L82-L124">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Solves systems of linear eqns `A X = RHS`, given Cholesky factorizations.

### Aliases:

* <a href="/api_docs/python/tf/linalg/cholesky_solve"><code>tf.cholesky_solve</code></a>
* <a href="/api_docs/python/tf/linalg/cholesky_solve"><code>tf.compat.v1.cholesky_solve</code></a>
* <a href="/api_docs/python/tf/linalg/cholesky_solve"><code>tf.compat.v1.linalg.cholesky_solve</code></a>
* <a href="/api_docs/python/tf/linalg/cholesky_solve"><code>tf.compat.v2.linalg.cholesky_solve</code></a>


``` python
tf.linalg.cholesky_solve(
    chol,
    rhs,
    name=None
)
```



<!-- Placeholder for "Used in" -->

```python
# Solve 10 separate 2x2 linear systems:
A = ... # shape 10 x 2 x 2
RHS = ... # shape 10 x 2 x 1
chol = tf.linalg.cholesky(A)  # shape 10 x 2 x 2
X = tf.linalg.cholesky_solve(chol, RHS)  # shape 10 x 2 x 1
# tf.matmul(A, X) ~ RHS
X[3, :, 0]  # Solution to the linear system A[3, :, :] x = RHS[3, :, 0]

# Solve five linear systems (K = 5) for every member of the length 10 batch.
A = ... # shape 10 x 2 x 2
RHS = ... # shape 10 x 2 x 5
...
X[3, :, 2]  # Solution to the linear system A[3, :, :] x = RHS[3, :, 2]
```

#### Args:


* <b>`chol`</b>:  A `Tensor`.  Must be `float32` or `float64`, shape is `[..., M, M]`.
  Cholesky factorization of `A`, e.g. `chol = tf.linalg.cholesky(A)`.
  For that reason, only the lower triangular parts (including the diagonal)
  of the last two dimensions of `chol` are used.  The strictly upper part is
  assumed to be zero and not accessed.
* <b>`rhs`</b>:  A `Tensor`, same type as `chol`, shape is `[..., M, K]`.
* <b>`name`</b>:  A name to give this `Op`.  Defaults to `cholesky_solve`.


#### Returns:

Solution to `A x = rhs`, shape `[..., M, K]`.
