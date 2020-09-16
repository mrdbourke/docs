description: Assert the condition x > 0 holds element-wise.

<div itemscope itemtype="http://developers.google.com/ReferenceObject">
<meta itemprop="name" content="tf.debugging.assert_positive" />
<meta itemprop="path" content="Stable" />
</div>

# tf.debugging.assert_positive

<!-- Insert buttons and diff -->

<table class="tfo-notebook-buttons tfo-api nocontent" align="left">
<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r2.2/tensorflow/python/ops/check_ops.py#L458-L487">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td>
</table>



Assert the condition `x > 0` holds element-wise.

<pre class="devsite-click-to-copy prettyprint lang-py tfo-signature-link">
<code>tf.debugging.assert_positive(
    x, message=None, summarize=None, name=None
)
</code></pre>



<!-- Placeholder for "Used in" -->

This Op checks that `x[i] > 0` holds for every element of `x`. If `x` is
empty, this is trivially satisfied.

If `x` is not positive everywhere, `message`, as well as the first `summarize`
entries of `x` are printed, and `InvalidArgumentError` is raised.

<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Args</h2></th></tr>

<tr>
<td>
`x`
</td>
<td>
Numeric `Tensor`.
</td>
</tr><tr>
<td>
`message`
</td>
<td>
A string to prefix to the default message.
</td>
</tr><tr>
<td>
`summarize`
</td>
<td>
Print this many entries of each tensor.
</td>
</tr><tr>
<td>
`name`
</td>
<td>
A name for this operation (optional). Defaults to "assert_positive".
</td>
</tr>
</table>



<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Returns</h2></th></tr>
<tr class="alt">
<td colspan="2">
Op raising `InvalidArgumentError` unless `x` is all positive. This can be
used with <a href="../../tf/control_dependencies.md"><code>tf.control_dependencies</code></a> inside of <a href="../../tf/function.md"><code>tf.function</code></a>s to block
followup computation until the check has executed.
</td>
</tr>

</table>



<!-- Tabular view -->
 <table class="responsive fixed orange">
<colgroup><col width="214px"><col></colgroup>
<tr><th colspan="2"><h2 class="add-link">Raises</h2></th></tr>

<tr>
<td>
`InvalidArgumentError`
</td>
<td>
if the check can be performed immediately and
`x[i] > 0` is False. The check can be performed immediately during eager
execution or if `x` is statically known.
</td>
</tr>
</table>



#### Eager Compatibility
returns None
