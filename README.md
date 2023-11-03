# Convolutional-Neural-Networks
CNN uses complex algorithms and artificial neural networks to train machines/computers so that they can learn from experience, classify and recognize data/images just like a human brain does.

Convolutional Neural Networks (CNN) tend to be multi-dimensional and contain some special layers, unsurprisingly called Convolutional layers. Moreover, Convolutional layers are often accompanied by Pooling layers (Max or Average), which help reduce the size of convolved features.

Traditional Neural Networks use dense layers with neurons while convolutional layers use filters to create feature maps that extract the main features of the images. 

Convolutional layer

It is worth highlighting that we can have Convolutional layers of different dimensions:

•	One-dimensional (Conv1D) — suitable for text embeddings, time-series or other sequences.
•	Two-dimensional (Conv2D) — typical choice for images.
•	Three-dimensional (Conv3D) — can be used for videos, which are essentially just sequences of images, or for 3D images such as MRI scans.

Kernel K, which is a feature detector is equivalent of the flashlight on image I, and we are trying to detect features and create multiple feature maps to help us identify or classify the image.
Kernel K  can be define as a window by which we examine a subset of the image, and subsequently scans the entire image looking through this window creating feature maps. 
We have multiple feature detector to help with things like edge detection, identifying different shapes, bends or different colors etc.
Feature maps can help to reduce the dimensionality of the input data, making it easier and faster to process and analyze. By using multiple layers of feature maps, a CNN can capture complex and hierarchical relationships between different features in the input data, leading to more accurate and robust predictions.
The conjunction of multiple feature maps it is what creates a convolutional layer. 

We have multiple feature Maps that help with things like edge detection, identifying different shapes, bends or different colors etc.

We can also specify how many filters we want to have in the Convolutional layer. Having multiple filters lets us extract a broader range of features from the image.

It is often beneficial to set up multiple Convolutional layers to improve the network. The benefits arise from subsequent Convolutional layers identifying extra complexity within the image.

The first layer in a Deep Convolutional Network (DCN) tends to find low-level features (e.g., vertical, horizontal, diagonal lines…). Meanwhile, the deeper layers can identify higher-level characteristics, such as more complex shapes, representing real-world elements like eyes, nose, ears etc.

There are a couple more options for us to tweak when setting up a Convolutional layer:

• Filters: The number of feature maps we want to have in a convolution layer. 

• kernel_size : specifying the height and width of the 2D convolution window. Creates the feature maps. 

•	Padding : in some scenarios, we may wish for the output to be the same size as the input. We can achieve that by adding some padding. At the same time, it may make it easier for the model to capture essential features residing at the edges of an image.

•	Stride : if we have large images, then we may want to use larger strides, i.e., shifting a filter by multiple pixels at a time. While it does help to reduce the size of the output, larger strides may result in some features being missed.

Depending on the size and complexity of your data, you may want to have multiple pairs of Convolutional and Pooling layers followed by multiple Dense Layers, making your network “Deep.”
