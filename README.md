# Visualizing Convnets

Visualizing the output of your machine learning model is a great way to see how its progressing, be it a tree-based model or a large neural network. I used the VGG16 model (pre-trained on ImageNet) available in Keras, on a cat image to see the output of some of the intermediate convolution and their corresponding activation layers. 

# Visualizing intermediate activations

Quoting François Chollet in his book "DEEP LEARNING with Python" (and I'll quote him a lot in this section):

Intermediate activations are "useful for understanding how successive convnet layers transform their input, and for getting a first idea of the meaning of individual convnet filters."

"The representations learned by convnets are highly amenable to visualization, in large part because they’re representations of visual concepts. Visualizing intermediate activations consists of displaying the feature maps that are output by various convolution and pooling layers in a network, given a certain input (the output of a layer is often called its activation, the output of the activation function). This gives a view into how an input is decomposed into the different filters learned by the network. Each channel encodes relatively independent features, so the proper way to visualize these feature maps is by independently plotting the contents of every channel as a 2D image."

Next, we’ll take an input image—a picture of a cat.

<img src="https://github.com/Muskan-goyal6/VisualizingConvnets/blob/master/images/cat.jpeg" width="350" height="300" />

"In order to extract the feature maps we want to look at, we’ll create a Keras model that takes batches of images as input, and outputs the activations of all convolution and pooling layers. To do this, we’ll use the Keras class VGG16 Model. A model is instantiated using two arguments: an input tensor (or list of input tensors) and an output tensor (or list of output tensors). The resulting class is a Keras model, just like the Sequential models, mapping the specified inputs to the specified outputs. What sets the Model class apart is that it allows for models with multiple outputs, unlike Sequential."

<!-- ![cat](https://github.com/Muskan-goyal6/VisualizingConvnets/blob/master/images/cat.jpeg| width=100 ) -->
![visualise1](https://github.com/Muskan-goyal6/VisualizingConvnets/blob/master/images/cat_inp.png)
![visualise2](https://github.com/Muskan-goyal6/VisualizingConvnets/blob/master/images/cat_act.png)

# Visualizing the filter patterns of layers

![visual3](https://github.com/Muskan-goyal6/VisualizingConvnets/blob/master/images/filters.png)
