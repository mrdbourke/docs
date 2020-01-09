page_type: reference
<style>{% include "site-assets/css/style.css" %}</style>

<!-- DO NOT EDIT! Automatically generated file. -->

# tf.nn.moments


<table class="tfo-notebook-buttons tfo-api" align="left">

<td>
  <a target="_blank" href="/api_docs/python/tf/nn/moments">
  <img src="https://www.tensorflow.org/images/tf_logo_32px.png" />
  TensorFlow 2 version</a>
</td>

<td>
  <a target="_blank" href="https://github.com/tensorflow/tensorflow/blob/r1.15/tensorflow/python/ops/nn_impl.py#L1171-L1233">
    <img src="https://www.tensorflow.org/images/GitHub-Mark-32px.png" />
    View source on GitHub
  </a>
</td></table>



Calculate the mean and variance of `x`.

### Aliases:

* <a href="/api_docs/python/tf/nn/moments"><code>tf.compat.v1.nn.moments</code></a>


``` python
tf.nn.moments(
    x,
    axes,
    shift=None,
    name=None,
    keep_dims=None,
    keepdims=None
)
```



<!-- Placeholder for "Used in" -->

The mean and variance are calculated by aggregating the contents of `x`
across `axes`.  If `x` is 1-D and `axes = [0]` this is just the mean
and variance of a vector.

Note: shift is currently not used; the true mean is computed and used.

When using these moments for batch normalization (see
<a href="../../tf/nn/batch_normalization"><code>tf.nn.batch_normalization</code></a>):

 * for so-called "global normalization", used with convolutional filters with
   shape `[batch, height, width, depth]`, pass `axes=[0, 1, 2]`.
 * for simple batch normalization pass `axes=[0]` (batch only).

#### Args:


* <b>`x`</b>: A `Tensor`.
* <b>`axes`</b>: Array of ints.  Axes along which to compute mean and
  variance.
* <b>`shift`</b>: Not used in the current implementation
* <b>`name`</b>: Name used to scope the operations that compute the moments.
* <b>`keep_dims`</b>: produce moments with the same dimensionality as the input.
* <b>`keepdims`</b>: Alias to keep_dims.


#### Returns:

Two `Tensor` objects: `mean` and `variance`.