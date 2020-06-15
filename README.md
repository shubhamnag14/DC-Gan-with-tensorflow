![Image](https://www.tensorflow.org/images/gan/dcgan.gif)

# DC-Gan-with-tensorflow
Deep Convolutional Generative Network (DCGAN)is one of the most popular also the most successful implementation of GAN. It is composed of ConvNets in place of multi-layer perceptrons. The ConvNets are implemented without max pooling, which is in fact replaced by convolutional stride...

# Generator

The generator synthesizes fake images. In Figure 2, the fake image is generated from a 100-dimensional noise (uniform distribution between -1.0 to 1.0) using the inverse of convolution, called transposed convolution. Instead of fractionally-strided convolution as suggested in DCGAN, upsampling between the first three layers is used since it synthesizes more realistic handwriting images. In between layers, batch normalization stabilizes learning. The activation function after each layer is a ReLU. The output of the sigmoid at the last layer produces the fake image. Dropout of between 0.3 and 0.5 at the first layer prevents overfitting. Listing 2 shows the implementation in Keras...

![Image](https://www.tensorflow.org/tutorials/generative/dcgan_files/output_gl7jcC7TdPTG_1.png)
                                     (center)         Generator output
