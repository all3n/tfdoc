page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# Module: tf.contrib.constrained_optimization


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/constrained_optimization/__init__.py">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



A library for performing constrained optimization in TensorFlow.

<!-- Placeholder for "Used in" -->


## Classes

[`class AdditiveExternalRegretOptimizer`](../../tf/contrib/constrained_optimization/AdditiveExternalRegretOptimizer): A `ConstrainedOptimizer` based on external-regret minimization.

[`class AdditiveSwapRegretOptimizer`](../../tf/contrib/constrained_optimization/AdditiveSwapRegretOptimizer): A `ConstrainedOptimizer` based on swap-regret minimization.

[`class ConstrainedMinimizationProblem`](../../tf/contrib/constrained_optimization/ConstrainedMinimizationProblem): Abstract class representing a `ConstrainedMinimizationProblem`.

[`class ConstrainedOptimizer`](../../tf/contrib/constrained_optimization/ConstrainedOptimizer): Base class representing a constrained optimizer.

[`class MultiplicativeSwapRegretOptimizer`](../../tf/contrib/constrained_optimization/MultiplicativeSwapRegretOptimizer): A `ConstrainedOptimizer` based on swap-regret minimization.

## Functions

[`find_best_candidate_distribution(...)`](../../tf/contrib/constrained_optimization/find_best_candidate_distribution): Finds a distribution minimizing an objective subject to constraints.

[`find_best_candidate_index(...)`](../../tf/contrib/constrained_optimization/find_best_candidate_index): Heuristically finds the best candidate solution to a constrained problem.
