page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.contrib.eager.metrics.SparseAccuracy


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L502-L547">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



## Class `SparseAccuracy`

Calculates how often `predictions` matches `labels`.

Inherits From: [`Mean`](../../../../tf/contrib/eager/metrics/Mean)

<!-- Placeholder for "Used in" -->

This class is compatible with
<a href="../../../../tf/keras/losses/sparse_categorical_crossentropy"><code>tf.keras.losses.sparse_categorical_crossentropy</code></a>,
<a href="../../../../tf/nn/sparse_softmax_cross_entropy_with_logits"><code>tf.nn.sparse_softmax_cross_entropy_with_logits</code></a>,
<a href="../../../../tf/losses/sparse_softmax_cross_entropy"><code>tf.compat.v1.losses.sparse_softmax_cross_entropy</code></a>.

#### Attributes:


* <b>`name`</b>: name of the accuracy object
* <b>`dtype`</b>: data type of tensor.

<h2 id="__init__"><code>__init__</code></h2>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L515-L518">View source</a>

``` python
__init__(
    name=None,
    dtype=tf.dtypes.double
)
```

Inits SparseAccuracy with name and dtype.




## Properties

<h3 id="name"><code>name</code></h3>




<h3 id="variables"><code>variables</code></h3>






## Methods

<h3 id="__call__"><code>__call__</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L135-L150">View source</a>

``` python
__call__(
    *args,
    **kwargs
)
```

Returns op to execute to update this metric for these inputs.

Returns None if eager execution is enabled.
Returns a graph-mode function if graph execution is enabled.

#### Args:


* <b>`*args`</b>: * <b>`**kwargs`</b>: A mini-batch of inputs to the Metric, passed on to `call()`.

<h3 id="add_variable"><code>add_variable</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L260-L290">View source</a>

``` python
add_variable(
    name,
    shape=None,
    dtype=None,
    initializer=None
)
```

***Only for use by descendants of Metric***.


<h3 id="aggregate"><code>aggregate</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L237-L256">View source</a>

``` python
aggregate(metrics)
```

Adds in the state from a list of metrics.

Default implementation sums all the metric variables.

#### Args:


* <b>`metrics`</b>: A list of metrics with the same type as `self`.


#### Raises:


* <b>`ValueError`</b>: If metrics contains invalid data.

<h3 id="build"><code>build</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L302-L311">View source</a>

``` python
build(
    *args,
    **kwargs
)
```

Method to create variables.

Called by `__call__()` before `call()` for the first time.

#### Args:


* <b>`*args`</b>: * <b>`**kwargs`</b>: The arguments to the first invocation of `__call__()`.
 `build()` may use the shape and/or dtype of these arguments
 when deciding how to create variables.

<h3 id="call"><code>call</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L520-L547">View source</a>

``` python
call(
    labels,
    predictions,
    weights=None
)
```

Accumulate accuracy statistics.

`labels` and `predictions` should have the same shape except the
predictions must have one additional trailing dimension equal to the
number of classes(you want to predict).

Type of labels and predictions can be different.

#### Args:


* <b>`labels`</b>: Tensor of shape (batch_size, ) containing integers
* <b>`predictions`</b>: Tensor with the logits or probabilities for each example.
* <b>`weights`</b>: Optional weighting of each example. Defaults to 1.


#### Returns:

The arguments, for easy chaining.


<h3 id="init_variables"><code>init_variables</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L160-L177">View source</a>

``` python
init_variables()
```

Initializes this Metric's variables.

Should be called after variables are created in the first execution
of `__call__()`. If using graph execution, the return value should be
`run()` in a session before running the op returned by `__call__()`.
(See example above.)

#### Returns:

If using graph execution, this returns an op to perform the
initialization. Under eager execution, the variables are reset to their
initial values as a side effect and this function returns None.


<h3 id="result"><code>result</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L340-L362">View source</a>

``` python
result(write_summary=True)
```

Returns the result of the Metric.


#### Args:


* <b>`write_summary`</b>: bool indicating whether to feed the result to the summary
  before returning.

#### Returns:

aggregated metric as float.


#### Raises:


* <b>`ValueError`</b>: if the optional argument is not bool

<h3 id="value"><code>value</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/contrib/eager/python/metrics_impl.py#L217-L222">View source</a>

``` python
value()
```

In graph mode returns the result Tensor while in eager the callable.