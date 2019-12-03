# Unet

Convolutional Networks for Biomedical Image Segmentation 

**Abstract**

Successful training of DNN needs many training samples. This paper presents a **network** and **training strategy** that relies on data augmentation to use available samples more efficient.



**Introduction**

 biomedical tasks requires pixel-wise classification.  Ciresan et al  present a network in a sliding-window way to predict the class of each pixel by providing a local region around that pixel.

But if the generated region is small, it needs more computation which slags speed, while larger region reduce accuracy.

More recent approaches proposed a network that takes into account the features of **multiple-layers** features from shadow layers can provide more detail information, deeper layers information have larger receptive field.



**Network Architecture**

![]( https://github.com/ChrisWang10/paper/raw/master/img/unet_architecture.png )

We call the left side of this by contracting path and right side expansive path. Every step in the expansive path consists of an up-sampling of the feature map followed by a 2x2 convolution (up-convolution") that halves the number of feature channels then ***concatenate with the corresponding cropped feature map from contracting path***. Because of loss of border pixels in every convolution.



At final stage, the energy function is computed by a pixel-wise soft-max over the final feature map combined with the cross entropy loss function.



**Training**

Ideally the initial weights should be adapted such that each feature map in the network has approximately unit variance. **Otherwise, parts of the network might give excessive activations, while other parts
never contribute.** 



