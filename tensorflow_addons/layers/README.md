# Addons - Layers

## Contents
| Layer  | Reference                                     |
|:----------------------- |:-----------------------------|
| Maxout | https://arxiv.org/abs/1302.4389               |
| PoinareNormalize | https://arxiv.org/abs/1705.08039    |
| WeightNormalization | https://arxiv.org/abs/1602.07868 |


## Contribution Guidelines
#### Standard API
In order to conform with the current API standard, all layers
must:
 * Inherit from either `keras.layers.Layer` or its subclasses.
 * [Register as a keras global object](https://github.com/tensorflow/addons/blob/master/tensorflow_addons/utils/python/keras_utils.py)
  so it can be serialized properly.
 * Add the addon to the `py_library` in this sub-package's BUILD file.

#### Testing Requirements
 * Simple unittests that demonstrate the layer is behaving as expected.
 * When applicable, run all unittests with TensorFlow's
  `@run_all_in_graph_and_eager_modes` decorator.
 * Run `keras.testing_utils.layer_test` on the layer.
 * Add a `py_test` to this sub-package's BUILD file.

#### Documentation Requirements
 * Update the table of contents in the project's central README.
 * Update the table of contents in this sub-package's README.
