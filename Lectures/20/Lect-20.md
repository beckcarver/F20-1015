# Lecture 20 - Tensor Flow Example

[TensorFlow First Example - https://youtu.be/rAQSkZ16GXo](https://youtu.be/rAQSkZ16GXo)<br>

From Amazon S3 - for download (same as youtube videos)

[TensorFlow First Example](http://uw-s20-2015.s3.amazonaws.com/1015-L-20-tensor-flow-pt1.mp4)<br>


## Applications of Machine Learning

[https://www.bbc.com/news/technology-54780460  Sars-Cov-2 (COVID-19) identified from sound of cough](https://www.bbc.com/news/technology-54780460)

Play a game:

[https://yanpanlau.github.io/2016/07/10/FlappyBird-Keras.html](https://yanpanlau.github.io/2016/07/10/FlappyBird-Keras.html)

Pay in AI:

[https://aipaygrad.es/](https://aipaygrad.es/)

$135k to $145k a year:

[https://spectrum.ieee.org/at-work/tech-careers/5-hot-engineering-jobs-for-grads](https://spectrum.ieee.org/at-work/tech-careers/5-hot-engineering-jobs-for-grads)

or $169k a year:

[https://medium.com/towards-artificial-intelligence/artificial-intelligence-salaries-heading-skyward-e41b2a7bba7d](https://medium.com/towards-artificial-intelligence/artificial-intelligence-salaries-heading-skyward-e41b2a7bba7d)

## TensorFlow

Hello World of Tensor Flow: from: [https://www.tensorflow.org/tutorials/quickstart/beginner](https://www.tensorflow.org/tutorials/quickstart/beginner)
There are also 2 YouTube videos to watch: [https://www.tensorflow.org/tutorials](https://www.tensorflow.org/tutorials)

```
# Download and install the TensorFlow 2 package. Import TensorFlow into your program:

from __future__ import absolute_import, division, print_function, unicode_literals

# Install TensorFlow

import tensorflow as tf

# Load and prepare the MNIST dataset. Convert the samples from integers to floating-point numbers:

mnist = tf.keras.datasets.mnist

(x_train, y_train), (x_test, y_test) = mnist.load_data()
x_train, x_test = x_train / 255.0, x_test / 255.0

# Build the tf.keras.Sequential model by stacking layers. Choose an optimizer and loss function for training:

model = tf.keras.models.Sequential([
  tf.keras.layers.Flatten(input_shape=(28, 28)),
  tf.keras.layers.Dense(128, activation='relu'),
  tf.keras.layers.Dropout(0.2),
  tf.keras.layers.Dense(10, activation='softmax')
])

model.compile(optimizer='adam',
              loss='sparse_categorical_crossentropy',
              metrics=['accuracy'])

# Train and evaluate the model:

model.fit(x_train, y_train, epochs=5)

model.evaluate(x_test,  y_test, verbose=2)

```

