description: A LearningRateSchedule that uses a polynomial decay schedule.

<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.keras.optimizers.schedules.PolynomialDecay" />
<meta itemprop="path" content="Stable" />
<meta itemprop="property" content="__call__"/>
<meta itemprop="property" content="__init__"/>
<meta itemprop="property" content="from_config"/>
<meta itemprop="property" content="get_config"/>
</div>

# tf.keras.optimizers.schedules.PolynomialDecay

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api nocontent" align="left">
<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r2.2/tensorflow/python/keras/optimizer_v2/learning_rate_schedule.py#L267-L406">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td>
</table>



A LearningRateSchedule that uses a polynomial decay schedule.

Inherits From: [`LearningRateSchedule`](../../../../tf/keras/optimizers/schedules/LearningRateSchedule.md)

<section class="expandable">
  <h4 class="showalways">View aliases</h4>
  <p>
<b>Main aliases</b>
<p>`tf.optimizers.schedules.PolynomialDecay`</p>

<b>Compat aliases for migration</b>
<p>See
<a href="https://www.tensorflow.org/guide/migrate">Migration guide</a> for
more details.</p>
<p>`tf.compat.v1.keras.optimizers.schedules.PolynomialDecay`</p>
</p>
</section>

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>tf.keras.optimizers.schedules.PolynomialDecay(
    initial_learning_rate, decay_steps, end_learning_rate=0.0001, power=1.0,
    cycle=(False), name=None
)
</code></pre>



<!-- Placeholder for "Used in" -->


<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Args</h2></th></tr>

<tr>
<td>
`initial_learning_rate`
</td>
<td>
A scalar `float32` or `float64` `Tensor` or a
Python number.  The initial learning rate.
</td>
</tr><tr>
<td>
`decay_steps`
</td>
<td>
A scalar `int32` or `int64` `Tensor` or a Python number.
Must be positive.  See the decay computation above.
</td>
</tr><tr>
<td>
`end_learning_rate`
</td>
<td>
A scalar `float32` or `float64` `Tensor` or a
Python number.  The minimal end learning rate.
</td>
</tr><tr>
<td>
`power`
</td>
<td>
A scalar `float32` or `float64` `Tensor` or a
Python number.  The power of the polynomial. Defaults to linear, 1.0.
</td>
</tr><tr>
<td>
`cycle`
</td>
<td>
A boolean, whether or not it should cycle beyond decay_steps.
</td>
</tr><tr>
<td>
`name`
</td>
<td>
String.  Optional name of the operation. Defaults to
'PolynomialDecay'.
</td>
</tr>
</table>



## Methods

<h3 id="from_config"><code>from_config</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r2.2/tensorflow/python/keras/optimizer_v2/learning_rate_schedule.py#L50-L60">View source</a>

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>@classmethod</code>
<code>from_config(
    config
)
</code></pre>

Instantiates a `LearningRateSchedule` from its config.


<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2">Args</th></tr>

<tr>
<td>
`config`
</td>
<td>
Output of `get_config()`.
</td>
</tr>
</table>



<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2">Returns</th></tr>
<tr class="alt">
<td colspan="2">
A `LearningRateSchedule` instance.
</td>
</tr>

</table>



<h3 id="get_config"><code>get_config</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r2.2/tensorflow/python/keras/optimizer_v2/learning_rate_schedule.py#L398-L406">View source</a>

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>get_config()
</code></pre>




<h3 id="__call__"><code>__call__</code></h3>

<a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r2.2/tensorflow/python/keras/optimizer_v2/learning_rate_schedule.py#L369-L396">View source</a>

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>__call__(
    step
)
</code></pre>

Call self as a function.



