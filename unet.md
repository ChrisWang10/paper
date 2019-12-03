# Unet

Convolutional Networks for Biomedical Image Segmentation 

**Abstract**

Successful training of DNN needs many training samples. This paper presents a **network** and **training strategy** that relies on data augmentation to use available samples more efficient.



**Introduction**

 biomedical tasks requires pixel-wise classification.  Ciresan et al  present a network in a sliding-window way to predict the class of each pixel by providing a local region around that pixel.

But if the generated region is small, it needs more computation which slags speed, while larger region reduce accuracy.

More recent approaches proposed a network that takes into account the features of **multiple-layers** 



